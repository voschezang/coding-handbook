# Domain-Driven Design

## Currency conversion

Two type-safe implementations using FP and OOP. 
Unit-tests are excluded for brevity.


1. The first FP example if brief and can easily be extended in case of future requirements.
	- It should be noted that the type conversion is a bit fuzzy. This part is language-dependent.
	- Alternatively the type `Money` could be a product type.


```python
# FP
type EUR = Int # alias
type USD = Int # alias
type Money = EUR | USD # union type
type Wallet = { dollars: USD, euros: EUR } # C-style record

def eurosToDollars(euros: EUR) -> USD:
	return euros * 1.0

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
 * For brevity all methods are public
 */
 
abstract class Money
{
	Int value;
}

class EUR extends Money {} // excl. constructor, getters, setters
class USD extends Money // excl. constructor, getters, setters
{
	add(USD dollars)
	{
		// violation of CQR separation
		self.value += dollars.value;
	}
}

class MoneyConverter // adapter pattern
{
	// adapter to reduce coupling between EUR and USD
	static USD toUSD(EUR euros) 
	{
		return euros.value * 1.0
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

		// alternatively, a one-line functional static method could be used
		// return USD.addTwo(self.dollars, Converter.toUSD(self.euros));
	}


	// excl. getters, setters
}
```

Because the two implementations are comparable, one could be used to generate the other.
For that reason I favour the shortest version.

