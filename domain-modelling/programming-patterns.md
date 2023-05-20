# Patterns & Principles

[toc]

This document contains patterns that show up in system and application architecture. Paradigms for programming langues can be found [here](../programming-paradigmes.md). See also [design patterns](https://learn.microsoft.com/en-us/azure/architecture/patterns/).

## Introduction

Although systems architecture and application architecture are different disciplines, design patterns are relevant to everything from high-level systems to low-level applications. They do however have different implications at different levels of scale. See also [functional programming patterns](../computer-language/programming-patterns-functional.md).

Note that applications with many components are also systems.

**Sidenote**
Patterns are *just* models that can be used as tools to understand a system. Note that:

> All models are wrong.

and

> Multiple models can be correct.

Patterns allow experience reuse, rather than code reuse. They provide a shared vocabulary. In addition, they are a necessary complement to OOP, which can grow overly complex quickly.

**Guidelines**
In general:

- Locality is easy: e.g. changes inside a single module or a single application.
- Systems can be specific and efficient, or generic and flexible.
- The connections between components can be more important than the components themselves.
- A property of many good patterns is that they have clear boundaries.

## Fundamental Patterns

These patterns are fundamental in the sense that they apply to single components (units) of a system.

**Command–query Separation**
Each function, method or API call should focus on [one task](https://en.wikipedia.org/wiki/Command%E2%80%93query_separation), i.e. be *either* an imperative command or a query.

**Unix Philosophy**
Design programs to be [minimalistic](https://en.wikipedia.org/wiki/Unix_philosophy) and light-weight. This makes them replaceable and reusable.

**Encapsulation**
Encapsulate the parts of a program that change often. Usually this is the domain (core). In addition, make any contextual components replaceable.

A few examples:

```java
// raw usage of a primitive type
int account = (int) 100;
// custom type
Account account = new Account(100);
// separated interface and implementation
Account account = new BankAccount(100);
// decouple constructor
Account account = open_account(100);
// decouple constructor further with an abstract factory
Account account = AccountFactory('bank').setBalance(100).build()
```

**Objects and Containers**
The ordering or [structure](https://en.wikipedia.org/wiki/AoS_and_SoA) of containers can be either: a *set* of objects or an object with arrays. E.g.

```python
class Agents:
  data = {Agent(), ...}
  
  def __getitem__(self, i):
    return data[i]

class Agents:
  names = []
  positions = []
  
 def __getitem__(self, i):
    return Agent(names[i], positions[i])
```

See also [flyweight](https://en.wikipedia.org/wiki/Flyweight_pattern).

### Interfaces

A first abstraction is the *interface-implementation*. This separates the *internal* and *external* view of a component, i.e. the the interface (public) and the implementation (private). This can reduce coupling and complexity. Specific interface patterns are given in a [later section](#Structural Patterns).

**Composition**
A `hasA` relationship. E.g. `object = {x: int, y: float}`.
This is a simple, "linear" way to compose data.

**Inheritance**
An `isA` relationship. Sub-typing, sub-classes. I.e. backwards compatibility with a previous interface. E.g. `Array` vs. `Sequence`.

Inheritance typically uses [overriding](https://en.wikipedia.org/wiki/Method_overriding) to extend the behaviour of another class. It is both powerful and complex, compared to composition.

Typical risks:

- Complexity. A network of objects that relate to each other. Ambiguity in overriden methods.
- An exponential growth in the number of classes. E.g. `Coffee, CoffeeWithSugar, CoffeeWithDoubleSugar, CoffeeWithMilkAndSugar`.

**Multiple Inheritance**
Real-world object relations are often intertwined. A typical complicated relation is the [diamond pattern](https://en.wikipedia.org/wiki/Multiple_inheritance#The_diamond_problem).

E.g. `Person` is a `Human` and a  `Customer` . A `Family` is a `Set<Human>` but can also be a `Customer`,

**Decorator**
Both an `isA` and a `hasA` relationship. They are typically chained together, to extend the behaviour of an original object. E.g. `coffee = WithSugar( WithMilk( Coffee ))`.

Unlike traditional inheritance, these objects can be defined dynamically, at runtime.

A few variants of this are the strategy pattern and the factory pattern.

**Hook**
Call a user-definable method before (or after) a given operation. Note that this introduces some coupling between the operation and the given method.

**Provider-consumer**
One-to-one (point-to-point) messaging, where a service is provided by one party and consumed by another one.

#### Data Compression

Two fundamental compression patterns.

- [Differencing](https://en.wikipedia.org/wiki/Data_differencing). Take a *baseline* or template structure and add a *custom* structure on top. A typical use case is to use the the median of the data as a baseline.
  - E.g. "The ~~duck~~ <u>dog</u> walks."
- [Dictionary coding](https://en.wikipedia.org/wiki/Dictionary_coder). Use a dictionary as a database. Describe each data entry by a sequence of keys, which act as references of original components. E.g.:
  - Given the objects `dog, tree` and the verbs `to bark, to walk`.
  - The phrase `object.1 verb.1 object.2` represents the sentence "*The dog barks to the tree*".

**Template**
A template is an abstract recipe or skeleton, that prescribes a basic structure. E.g.

- A pizza must contain the *components* dough and a topping.
- An iteration *algorithm* must contains the methods `next` and `hasNext`.

## System Patterns

Design patterns for applications and systems. See also [organization structure](../organization-structure.md) and [communication patterns](../communication-patterns.md).

### Integration styles

[Four](https://en.wikipedia.org/wiki/Enterprise_Integration_Patterns) standard categories:

- API/RPC calls. Share both data and process. Simple & intuitive (aka function calls).
  - Relatively slow, high communication overhead.
- Messaging. Fast, light-weight, non-blocking communication.
  - Defining the smallest event can be nontrivial, as it is shared by multiple systems. It has a steep learning curve.
  - Potential ownership problem. It requires a shared communication bus.
- FTP. Simple & universal. Just data, no commands.
  - Lacking synchronous communication. No consistency or timeline management.
- Shared DB. Single source of truth. Real-time access to latest data.
  - It is difficult to find uniform data model without compromises.
  - Noisy neighbour syndrome.
  - Performance can be an issue.

In addition, a provider of a service can expose client libraries and pipeline templates to consumers.

### Models

**Repository interface processor**

A domain-driven method to model a system.

- A <u>repository</u> service to store data. A persistency layer. The source of truth.
- An <u>interface</u> service to communicate with the repository layer.
- A <u>processor</u> service that covers the domain-logic. The *core* in [hexagonal architecture](https://en.wikipedia.org/wiki/Hexagonal_architecture_(software)).

**Model View Controller (MVC)**
[Consists](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller) of

- Model. Data layer. Responsible for data, logic and rules.
- View. Presentation layer.
  - Queries for data.
- Controller. Responsible for interaction (modification) of the model.
  - Commands

See also [CQRS](https://en.wikipedia.org/wiki/Command%E2%80%93query_separation#Command_Query_Responsibility_Separation).

### Structural Patterns

Standard structures

- **Interface-implementation**. This separates the *internal* and *external* view of a component, i.e. the the interface (public) and the implementation (private).
- **Frontend-backend**. The where the former usually has the role of a consumer of a service. These layers may be separated by several types of middleware.

**Adapter**
E.g. a power-plug.

- A method to simulate a *target* interface (the *adaptee*) by placing an *adapter* in front of it. This allows it to be used by a client that is expects the target interface.

  - The adapter can be implemented using either composition or inheritance.
  - Usually a one-to-one mapping.

  - *Two-way* adapter. An adapter where the *adapter* and *adaptee* roles are re-used.

**Adapter patterns**

For components:

- Interface. Hide complexity of implementation

- Decorator

  - Extend the functionality of one object by adding a wrapper around it.

  - This scopes down the responsibility of different objects.

  - The mapping is one-to-one, but there can be multiple decorators wrapped around a single object.

For systems:

- **Bridge**.
  - A decoupling layer between a backend and frontend.
  - Usually *many-to-many* mapping, where there are multiple clients and producers.
- **Facade** or Backend for frontend (**BFF**).
  - Simplify a complex backend using a user-centric layer (interface).

    - Usually *one-to-many* mapping.
- **Proxy**. An imperfect substitution. Limit access to the original.

**Other patterns**

- [Singleton](https://en.wikipedia.org/wiki/Singleton_pattern). A globally unique object that may be created lazily. Uniqueness is usually enforced at the language level.
  - Race conflicts in multithreaded code can be avoided by either: eager instantiation,  [synchronized methods](https://docs.oracle.com/javase/tutorial/essential/concurrency/syncmeth.html) or [synchronized statements](https://docs.oracle.com/javase/tutorial/essential/concurrency/locksync.html) (with [double checking](https://en.wikipedia.org/wiki/Double-checked_locking)).
- [Multiton](https://en.wikipedia.org/wiki/Multiton_pattern).

### Other Patterns (OOP)

- Creation
  - **Factory**.
    - An abstraction that "builds" an object based on (user) input, at runtime.
    - A specific `factory` can be passed to a function to control the "flavour" of the objects that are created.

- Design
  - **Strategy**.
    - An interchangeable and replaceable interface for algorithms, to model behaviour. It can be replaced even at runtime.

### Examples

##### Composition Inheritance Decorator

```py
class CompositionExample:
  x: int

class SubClass(SuperClass, OtherSuperclass):
  # Example of Inheritance
  pass
  
class DecoratorExample(SuperClass):
  x: int
  
  def getX(self):
    return self.x + self.SuperClass.x
  
```

##### Template Method

```py
# Using inheritance to overrride methods
class Template:
  def run(self, ..):
    self.intro()
    self.body()
    self.outro()

# using partial functions to override functions
def run(intro: F,
    body: F,
        outro: F):
  ..
```

### Anti-patterns

**Pre-mature standardization**
E.g. applying DRY too soon. Creating an interface before al the "clients" are known. This will cause integration issues.
