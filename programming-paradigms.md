# Programming Paradigms

## Language Design

* All modern languages (e.g. C, Java, Python, Haskell) are [equal](https://en.wikipedia.org/wiki/Turing_completeness) and allow for:
  1. encapsulation of _functionality_ using modules or components,
  2. encapsulation of _data_ using (local) scopes.

* In addition, many languages allow for composition of datastructures and methods a type of class system. E.g.:
  1. Type aliasses and union types.
      E.g. `union type A = B | C`, `alias type A = {b: B, c: C}`.
  2. Interfaces and base-classes (e.g. class implementation and extension).
  * This allows for domain-driven design.

* The major difference between object-oriented programming (OOP) and functional programming (FP):
    * OOP: coupling of data and methods, resulting in complex objects with an internal, hidden/private state.
    * FP: **de**coupling of data and methods, resulting in independent, stateless, deterministic functions. 
      This makes it trivial to parallelize.

* Properties such as data immutablility, overriding, overloading, static/dynamic/strong/weak/nominal/structural typing, are irrelevant.


## Language Complexity

* OOP is the most powerful paradigm because we represent our program as a distributed system and allow the program to behave as a network.
  * Designing classes is as easy as designing system architectures.

* Functional programming combines the flexibility and power of abstract mathematics with the intuitive clarity of abstract mathematics ([xkcd](https://xkcd.com/1270/))."

* The complexity of type/class-composition scales linearly but the complexity of a **network** scales non-linearly, due to the interactions between different components.
   * Naturally, the complexity of FP programs scales linearly as well.


## Language Usage

* Fortunately, there are many design patterns and principles that help you to counter the complexities and monstrosities typically entcountered in (enterprise) OOP codebases.

* In FP there are many equivalents to OOP design principles, for example SOLID:
   * The `Single-responsibility`, `Open-closed`, `Interface segregation`, and `Dependency inversion` princples are replaced by [_Pure Functions_](https://en.wikipedia.org/wiki/Pure_function)).
   * The `Liskov substitution principle` are replaced by a proper (i.e. algebraic, composable) _type system_ (e.g. type classes).

* In FP, design patterns are language-constructs.
  * E.g. `function composition, Maybe.andThen, List.map, fold, filter`.
  * Unfortunately, because of their importance they have been given technical names such as `Monad, Monoid, Functor`.

* In FP, you can do [event sourcing](https://martinfowler.com/eaaDev/EventSourcing.html) in one [line](https://wiki.haskell.org/Fold):
  `current = foldl(update, init, events)`, where
  * `current, init` have the type `State`,
  * `events` is a sequence that represent transactions or updates,
  * `update(State, Event) -> State` is a (pure) function.


## Tradeoff's

Tradeoff's for application structure.
The best choice is *context-dependent* (i.e. ambiguous).
Always assume a continuum when making **decisions**.

* In addition, consider the impact, and whether the decision is easily reversible (or adaptable).


### General
* Appliction architecture: coupled or decoupled components
  * E.g. monolithic, layered, CQRS, event-sourcing.
* System architecture: monolithic or microservice.
* Organization structure or workflow: waterfall, agile, or anarchy.
  * The latter is for example effective in R&D.
  * The more imporant question is: "How much upfront planning is required in advance of experimentation."
* Version control:
  * Multiple branches, but moving changes in one direction through environments (e.g. `dev -> test -> production`).
  * A single main branch (trunk), where each environment is checked out at a specific commit/state (e.g. using tags).


### Programming Language Design
* Default visibility of attributes and methods: `public` or `private`.
* Mutable or immutable data.
* Ordering or [structure](https://en.wikipedia.org/wiki/AoS_and_SoA) of data: a _set_ of objects or an object with arrays.
  * The former is readable and intuitive, the latter let's you do linear algebra



## Experimenal Design

* Collaborate & discuss & challenge your assumptions.
* Limit the scope of experiments and MVP's. Make sure that you have the ability to kill them.
* Consider the following ([tradoffs](https://twitter.com/johncutlefish/status/1400681664225837057)): 
  * Local - global
  * Flexible - rigid
  * Short duration - long duration
  * Short feedback loops - long feedback loops
  * Invitation - imposition
  * Minimal & compact - fully self-contained
  * Value in side-effects - risk in side-effects
  * Low threat to status quo - challenges status quo & conventions