# Language Specification

This is a language specification that starts with an Algebraic Type System and adds OOP concepts on top of it.

[toc]

## 1. Type Systems

### Values

* A **value** is immutable and is only equal to itself. Each **value** has a _Type_.
  * Special values are:
    * Void `0` or empty set `{}`
    * Unit `1`

* **Variables** are merely _references_ or pointers to either immutable values (constants) or other variables.
  * Hence variables do not necessarily have a value.

## Types

Note that [sets](https://en.wikipedia.org/wiki/Set_theory) can be combined in different fashions.

* `A | B` Disjoint union, Either. E.g. `yes` or `no`

* `A & B` Intersection. E.g. `here` and `now`

* `A x B` Outer product.

Types

* A **Type** is a [_set_](https://en.wikipedia.org/wiki/Set_theory) of values. A set is unordered and can be closed, open or clopen.
  1. It can be defined using a listing of all elements, e.g. `EvenInt = { 0, 2, 4, ... }`.
  2. Or using a property or equivalence relation, e.g. `MyFloat = { n where 0.1 < n < 1 or n > 10 }`
  * A more programmer-oriented method is to write it as `Bool = true | false`, where the right-hand values are mutually exclusive. This is known as a **sum-type**, or [disjoint union](https://en.wikipedia.org/wiki/Coproduct).
  * Types cannot use a previously undefined type in their definition. This means that Types cannot recursively call themselves.
    * This prevents the following contradiction `RusselsSet = { n where n not in RusselsSet }`

* A **Type-Class** is an [intersection](https://en.wikipedia.org/wiki/Intersection) of multiple types.
  * E.g. `PositiveEvenInt = PositiveInt & EvenInt`, where `|` denotes the logical _and_ operator.
  * A special case is _exclusion_. E.g. a [negatype](https://www.hillelwayne.com/negatypes/) `NotIterable = not Iterable`

* A **product-type** is _both_ one type _and_ another type. These form composite **datastructures**.

  1. A tuple:  `User = (Int, String)`
  2. A named tuple or record: `User = {id: Int, name: String}`
  3. An stream: `[ ... ]`

* Types can be parameterized.
  * E.g. `Result a = Success a | Error`

* **Patten-matching** allows datastructures to be used as types.

  * For example: `Tree = { x where x = (_, _, _) | none }` where `_` is used to denote a wildcard variable (i.e. any value).
  * Note that this is not a contradiction. It can be expanded to: `Tree = none | (x, none, none) | (x, (y, none, none), (z, none, none) ) | ...`
  * Another example would be a [Railway](https://fsharpforfunandprofit.com/rop/) pattern for error-handling.
  * Here, the following functions are applied to the input iff the input is not an `Error`.

```python
Result y = x.toResult().ifSuccess(f)
                       .ifSuccess(g)
                       .ifSuccess(h)
```

* **Pure Functions** are stateless, deterministic mappings from one type to another.
  * E.g. `add(a, b) =  a + b`, with the type signature `add(Int, Int) -> Int`
  * E.g. `div(a, b) = a / b`, with the signature `div(Int, NonZeroInt) -> Float`

### Properties

Note that functions, mappings and relations are similar.

#### Functions

[Commutativity](https://en.wikipedia.org/wiki/Commutative_property)  Resilience against ordering of operands

`f(x, y) = f(y, x)`

[Associativity](https://en.wikipedia.org/wiki/Associative_property)
`f( g( x ) ) = g( f( x ) )`

[Distributivity](https://en.wikipedia.org/wiki/Distributive_property)

`f( g(x, y)) = g(f(x), f(y))`

#### Rotation

Rotate `f`<sup>`n`</sup>`(x) = x` for a given number `n`.

[Double negation](https://en.wikipedia.org/wiki/Double_negation)

`f( f( x)) = x`

[Idempotence](https://en.wikipedia.org/wiki/Idempotence)

`f(x) = f( f( x) )`

#### Relations

Relations can be one-to-one, one-to-many, or many-to-many.

Instances of relationships can have attributes. E.g. the _date_ of a marriage between people.

**Properties & Restrictions**

Directional. `f(x, y)` does not imply that `f(y, x)`

[Transitive](https://en.wikipedia.org/wiki/Transitive_relation): If `f(x) = y` and `g(y) = z` then there exists `h` s.t.  `h(x) = z`

[Symmetric](https://en.wikipedia.org/wiki/Symmetric_relation): If `f(x) = y` then `f(y) = x`

Antisymmetric: If `f(x) = y` then `f(y) != x`

[Reflexive](https://en.wikipedia.org/wiki/Reflexive_relation): If there exists an `f` s..t `f(x) = x` for every `x`

Implication (composition). If `f(x, y)` and `f(y, z)` then `f(x, z)`

## 2. Object-Oriented Programming

Type systems can be extended with additional complexity.

* **Objects** are special variables (i.e. references to values). They are _actualized_ instances of a class.
  * E.g. `Tree = {id: Int, height: Int}`, with the syntactic sugar `Tree.grow()`

* **Methods** are functions that can have side-effects. They are associated with a class and can be:
 1. A command or side-effect, e.g. `Cache.clear()`.
 2. A query, e.g. `List.length() -> Int`.
 3. Both.

* **Interfaces** are just types that implement some behaviour. We can distinguish between two types of interfaces.
  * (1) Data-restrictions. The simplest interface-type is a record that specifies certain fields.
  * E.g. `Node = { generic_part | next: Node }`
  * (2) Behaviour-restrictions. This is done by defining (partial) functions.
  * Ideally, frequently-used interfaces are build into the language and do not have to be defined or implemented manually.
