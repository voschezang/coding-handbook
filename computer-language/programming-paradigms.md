# Programming Paradigms

[toc]

## Language Design

* All modern languages (e.g. C, Java, Python, Haskell) are [equal](https://en.wikipedia.org/wiki/Turing_completeness) and allow for:
  1. encapsulation of _functionality_ using modules or components,
  2. encapsulation of _data_ using (local) scopes.

* In addition, many languages allow for composition of data-structures and methods a type of class system. E.g.:
  1. Type aliases and union types. E.g. `union type A = B | C`, `alias type A = {b: B, c: C}`.
  2. Interfaces and base-classes (e.g. class implementation and extension).
  
* The major difference between object-oriented programming (OOP) and functional programming (FP):
  * OOP
    * Coupling of data and operations, which may result in complex objects with an internal, hidden/private state.
      * This allows for inheritance of behaviour.
    * Coupling of interfaces and implementations (e.g. `Iterator, Iterable`). This prevents the need to design a formal (mathematical) model.
  * FP
    * **De**coupling of operations and data and data, resulting in independent, stateless, deterministic functions. This makes it trivial to parallelize.
    * **De**coupling of types and implementations. All behaviour is explicit.

* Properties such as data immutablility, overriding, overloading, static/dynamic/strong/weak/nominal/structural typing, are irrelevant.

## Language Complexity

* "OOP is the most powerful paradigm because we represent our program as a distributed system and allow the program to behave as a network."
  * "Designing classes is as easy as designing system architectures."

* "Functional programming combines the flexibility and power of [abstract mathematics](https://en.wikipedia.org/wiki/Category_theory) with the intuitive clarity of abstract mathematics ([xkcd](https://xkcd.com/1270/))."

* The complexity of type/class-composition scales linearly but the complexity of a **network** scales non-linearly, due to the interactions between different components.
  * Naturally, the complexity of FP programs scales linearly as well.

## Language Usage

* Fortunately, there are many design patterns and principles that help you to counter the complexities and monstrosities typically entcountered in (enterprise) OOP codebases.
* In FP there are many equivalents to OOP design principles, for example SOLID:
  * The `Single-responsibility`, `Open-closed`, and `Interface segregation` principles are guaranteed for [_Pure Functions_](https://en.wikipedia.org/wiki/Pure_function).
  * The `Liskov substitution` and `Dependency inversion` principles are replaced by a proper (i.e. algebraic, composable) _type system_ (e.g. type classes).
* In FP, design patterns are language-constructs.
  * E.g. `function composition, Maybe.andThen, List.map, fold, filter`.
  * Unfortunately, because of their importance they have been given technical names such as `Monad, Monoid, Functor`.
  * Dependency injection is replaced by partial function application.
* In FP, you can do [event sourcing](https://martinfowler.com/eaaDev/EventSourcing.html) in one [line](https://wiki.haskell.org/Fold):
  `current = foldl(update, init, events)`, where
  * `current, init` have the type `State`,
  * `events` is a sequence that represent transactions or updates,
  * `update(State, Event) -> State` is a (pure) function.
