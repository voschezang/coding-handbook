# Programming Paradigms

## Language Design

* All modern languages (e.g. C, Java, Python, Haskell) allow for
  1. encapsulation of _functionality_ using modules or components
  2. encapsulation of _data_ using (local) scopes

* In addition, many languages allow for composition of datastructures and methods a type of class system. E.g.
  1. Type aliasses and union types.
    E.g. `union type A = B | C`, `alias type A = {b: B, c: C}`.
  2. Interfaces and base-classes (e.g. class implementation and extension)
  * This allows for domain-driven design.

* The major difference between object-oriented programming (OOP) and functional programming (FP):
    * OOP: coupling of data and methods, resulting in complex objects with an internal, hidden/private state.
    * FP: **de**coupling of data and methods, resulting in independent, stateless, deterministic functions. 
      This makes it trivial to parallelize.

* Properties such as data immutablility, overriding, overloading, static/dynamic/strong/weak/nominal/structural typing, are irrelevant.


## Language Complexity

* OOP is the most powerful paradigm because we represent our program as a distributed system and allow the program to behave as a network.
  * Designing classes is as easy as designing system architectures.

* The complexity of type/class-composition scales linearly but the complexity of a **network** scales non-linearly, due to the interactions between different components.
   * Naturally, the complexity of FP programs scales linearly as well.


## Language Usage

* Fortunately, there are many design patterns and principles that help you to counter the complexities and monstrosities typically entcountered in (enterprise) OOP codebases.

* In FP there are many equivalents to OOP design principles, for example SOLID:
   * The `Single-responsibility`, `Open-closed`, `Interface segregation`, and `Dependency inversion` princples are replaced by _Pure Functions).
   * The `Liskov substitution principle` are replaced by a proper (i.e. algebraic, composable) _type system_ (e.g. type classes).

* In FP, design patterns are language-constructs.
  * E.g. `function composition, Maybe.andThen, List.map, Function.map fold, filter`
  * Unfortunately, because of their importance they have been given technical names such as `Monad, Monoid, Functor`


## Tradeoff's

Tradeoff's for application structure. 
The best choice is context-dependent (i.e. ambiguous).

* Default visibility of attributes and methods: `public` or `private`.
* Mutable or immutable data.
* Ordering of data: _row_-major or _column_-major
   * The former is readable and intuitive, the latter let's you do linear algebra
* Appliction architecture: monolithic or microservice.
* Version control:
  * Multiple branches, but moving changes in one direction through environments (e.g. `dev -> test -> production`).
  * A single main branch (trunk), where each environment is checked out at a specific commit/state (e.g. using tags).

