# Domain-Driven Design

[toc]

## Overview

[Domain-driven design](https://en.wikipedia.org/wiki/Domain-driven_design) (DDD) embraces the uncertainty of business terminology. It is centered around domain objects, which are made as explicit as possible to minimize ambiguity. Domain objects are expected to change often, while adapters can be functionally static. Moreover, adapters are designed to be replaceable.

A typical example is to encapsulate strings. Instead of using raw strings, it's possible to define a custom type or class (e.g. `Username(string)`) which contains its own logic.



**Types, properties, relations**

- A *type* is a classification of an *instance* of an object.
- A *property* is a characteristic or quality of an object: either a type or an instance.
- Relations are properties that apply to multiple objects.

More about relations [here](relations.md).



### Ambiguity

In the real world, objects can be ambiguous.

- It is possible to have multiple **views** from the same object.  E.g. a person may be listed as an employee and as stockholder.
- The object (or its properties) can **change** in the real world.

In addition, there can be natural ambiguity. E.g a book can be a specific text or a physical copy.

Within a single system such ambiguity can go unnoticed, but problems can arise when integrating multiple systems. To avoid this, terms can be made more *specific*. This [increases the contrast](https://twitter.com/jarango/status/1562791028167299079) between terms. E.g. use the term `PersonalBankAccount` rather than `Account`. Such terms only have meaning inside a given (bounded) [context](https://www.martinfowler.com/bliki/BoundedContext.html).

In addition, some other concepts that relates to ambiguity are:

- Oneness. Dealing with identity. E.g. a team of which all members are replaced.
- Sameness. Dealing with equality.

**Identity**
This can be modeled using an identity function [`id`](https://docs.python.org/3.8/library/functions.html#id) where  `a = b` iff `id(a) == id(b)`. Identification can be done using either identifier or a relation w.r.t. other items.

**Equality**

- Reference-based. When two references refer to the same object.
- Value-based.
  - Direct equality. E.g. `eq(10$, 10£) == True`  (at a given date).
  - When values are considered to be synonyms. E.g. `1, one,`.
- Interpretation-based. Compare a transformation of a value.  E.g. a *bias* or lens. `eq("sky", "water", bias=is_blue) == True` .

**Generality**
Generality is the concept of referring to an arbitrary number of objects. E.g. "a typical citizen".



### Reality

> Databases model not reality itself, but how reality is processed by users

In addition to the inherent imperfection of models, the realism of data can be limited in other ways. Suppose there is a database filled with information. The information can be outdated, planned or falsified or completely fictional. Or the information can be limited by the knowledge of the author. Typical examples are empty database fields, or fields with a default value (e.g. `unknown`).

An information system is said to *support* a certain amount of data. This means that it can properly handle this data and enforces the relevant constraints. One way to obtain this enforcement implicitly is to use specific data structures. E.g. a set that can never contain duplicate elements, or an array that contains values of the same type.

See [functions and relationships](./relations.md).



## Examples



### IaC / Architecture

An example of the infrastructure configuration for a [CQRS](https://en.wikipedia.org/wiki/Command_Query_Responsibility_Segregation) system.

```yaml
domain: # model / behaviour
├── apps:
│   ├── identity: # identity management
│   │   └── start/stop/status.yml
│   ├── keyvault: # secret management
│   │   └── start/stop/status.yml
│   ├── command: # write service
│   │   └── start/stop/status.yml
│   └── query: # read service
│       └── start/stop/status.yml
├── components:
│   ├── storage
│   └── webserver
└── system:
    ├── start.yml
    ├── status.yml
    ├── stop.yml
    └── update.yml
ops: # user-interface
├── start.yml
├── status.yml
├── stop.yml
└── update.yml
inventory: # i.e. repository
├── acc
├── dev
├── prd
└── tst
roles: # adapters
├── firewall
├── identity
├── keyvault
└── router
```



### Web API

An example of a web service that stores customer data and addresses.

```yml
domain: # model
├── address
├── contract
└── customer
routes: # user-interface / API
├── address:
│   └── create.yml
├── contract:
│   └── create.yml
└── customer:
    └── create.yml
repository: # persistency layer
├── cassandra
└── postgresql
adapters:
└── cdn
```



### Web API (Java)

A  [hexagonal architecture](https://en.wikipedia.org/wiki/Hexagonal_architecture_(software)) is an intuitive approach to combine domain-driven design (DDD) into a real-world application.

A major component is the Adaptor pattern. All contextual logic is outsourced, allowing the inner code to focus on the core domain.

E.g.

```sh
App
├── CoreBusiness.java # Domain Logic
├── Adapters # Adapters for external dependencies (libraries or APIs)
│   ├── AnalyticsApp.java
│   └── PartnerAPI.java
├── Repository
│   ├── Repository.java # Abstraction for internal databases
│   └── Internal
│       ├── Inventory.java
│       ├── Order.java
│       └── UserAccount.java
└── Service # User-Centric APIs
    ├── ExternalRestAPI.java
    └── InternalRestAPI.java
```



### Currency Conversion

Two type-safe implementations using FP and OOP.
Unit-tests are excluded for brevity.

1. The first FP example if brief and can easily be extended in case of future requirements.

- It should be noted that the type conversion is a bit fuzzy. This part is language-dependent.

```python
# FP
type EUR = Int # alias
type USD = Int # alias
type Money = EUR | USD # union type
type Wallet = { dollars: USD, euros: EUR } # C-style record

def eurosToDollars(euros: EUR) -> USD:
 return euros * 2

def sumInUSD(wallet: Wallet) -> USD:
    return wallet.dollars + eurosToDollars(wallet.euros)
```

2. The second OOP version is longer and more complex;
 it uses a base-class, an adapter-class, a composite-class and it uses encapsulation to hide internal states.

- This implementation is not trivial. An alternative implementation could use an interface rather than an abstract base class.
- The developer has to take all of this into account when designing the classes.

```java
/**
 * OOP
 * For brevity all methods are public and constructors, getters and setters are omitted.
 */
 
abstract class Money
{
 Int value; // in units
}

class EUR extends Money {}
class USD extends Money
{
 add(USD dollars)
 {
  // violation of command-query separation
  self.value += dollars.value;
 }
}

class MoneyConverter // adapter pattern
{
 // adapter to reduce coupling between EUR and USD
 static USD toUSD(EUR euros) 
 {
  return euros.value * 2
 }
}

class Wallet // composite pattern
{
 USD dollars;
 EUR euros;

 Wallet(USD dollars, EUR euros) 
 {
  self.dollars = dollars;
  self.euros = euros;
 }

 USD sumInUSD() 
 { 
  // don't access encapsulated internal states
  USD result = new USD();
  result.add(self.dollars);
  result.add(Converter.toUSD(self.euros));
  return result;

  // alternatively, a one-liner with functional static methods could be used
  // return USD.addTwo(self.dollars, Converter.toUSD(self.euros));
 }
}
```

Because the two implementations are [comparable](https://en.wikipedia.org/wiki/Isomorphism), one could be used to generate the other.



## References

- W. Kent. *Data and Reality*
