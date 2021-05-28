# Language Specification

This is a language specification that starts with an Algebraic Type System and adds OOP concepts on top of it.

<hr>

## 1. Type Systems

* **Variables** are merely _references_ to either immutable values (constants) or other variables.
	- Hence variables do not necessarily have a value.

* Each **value** (written in lowercase) has a _Type_.

* A **Type** is a _set_ of values. A set is unordered and can be closed, open or clopen.
	1. It can be defined using a listing of all elements, e.g. `EvenInt = { 0, 2, 4, ... }`.
	2. Or using a property or equivalence relation, e.g. `MyFloat = { n where 0.1 < n < 1 or n > 10 }`
	- A more programmer-oriented method is to write it as `Bool = true | false`, where the right-hand values are mutually exclusive.
	- Type cannot be recursive. This prevents the following contradiction `RusselsSet = { n where n not in RusselsSet }`

* A **Type-Class** is an intersection of multiple types.
	- E.g. `PositiveEvenInt = PositiveInt & EvenInt`, where `&` denotes the logical _and_ operator.
	
*  There are 3 types of **datastructures**.
	1. A tuple:  `User = (Int, String)`
	2. A named tuple or record: `User = {id: Int, name: String}`
	3. An stream: `[ ... ]`

* **Patten-matching** allows datastructures to be used as types.
	- E.g. `Tree = { x where x = (_, _, _) | none }` where `_` is used to denote a wildcard variable (any value).
	- Note that this is not a contradiction. It can be expanded to: `Tree = none | (x, none, none) | (x, (y, none, none), (z, none, none) ) | ...`

* Types can be parameterized.
	- E.g. `Result a = Success a | Error`
	- This can be used in the typical fashion: 
	`x.ifSuccess(f).ifSuccess(g).ifSuccess(h)` where functions `f,g,h` are applied in succession to `x`.

* **Pure Functions** are stateless, deterministic mappings from one type to another.
	- E.g. `add(a, b) =  a + b`, with the type signature `add(Int, Int) -> Int`
	- E.g. `div(a, b) = a / b`, with the signature `div(Int, NonZeroInt) -> Float`

<hr>

## 2. Object-Oriented Programming

Type systems can be extended with additional complexity.

* **Objects** are special variables (i.e. references to values). They are _actualized_ instances of a class.
	- E.g. `Tree = {id: Int, height: Int}`, with the syntactic sugar `Tree.grow()`

* **Methods** are functions that can have side-effects. They are associated with a class and can be:
	1. A command or side-effect, e.g. `Cache.clear()`.
	2. A query, e.g. `List.length() -> Int`.
	3. Both.


* **Interfaces** are just types that implement some behaviour. We can distinguish between two types of interfaces.
	- (1) Data-restrictions. The simplest interface-type is a record that specifies certain fields. 
	- E.g. `Node = { generic_part | next: Node }`
	- (2) Behaviour-restrictions. This is done by defining (partial) functions.
	- Ideally, frequently-used interfaces are build into the language and do not have to be defined or implemented manually.
