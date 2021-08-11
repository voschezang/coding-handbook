# Programming Paradigms

[toc]

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

* "Functional programming combines the flexibility and power of [abstract mathematics](https://en.wikipedia.org/wiki/Category_theory) with the intuitive clarity of abstract mathematics ([xkcd](https://xkcd.com/1270/))."

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



# Patterns

Note, in general:

- Locality is easy: e.g. changes inside a single module or a single application.

- Systems can be specific and efficient, or generic and flexible.



## System & Application Architecture

Although systems architecture and application architecture are different disciplines, design patterns are relevant to everything from high-level systems to low-level applications. They do however have different implications at different levels of scale.

- Applications with many components are also systems. 



**Orchestration & Choreography**

Orchestration

- Centralized control. services are called explicitly using API's.
    - Using *Commands* that focus on the *future*. E.g. `doThis`.
    - Messages (data) are send to specific destinations (peer-to-peer).

Choreography

- Distributed control. applications are autonomous and react to messages.
    - Using *Events* that describe the *past*. E.g. `ThisHappened`.
    - Messages (data) are broadcasted.
    - See: [publisher-subscriber](https://en.wikipedia.org/wiki/Publish%E2%80%93subscribe_pattern) at the architecture level, [observer](https://en.wikipedia.org/wiki/Observer_pattern) at the application level.



**Pure Functions**
[Functions](https://en.wikipedia.org/wiki/Pure_function) that are stateless and deterministic. This makes them trivial to parallelize. 

**Command–query Separation**
Each function, method or API call should focus on [one task](https://en.wikipedia.org/wiki/Command%E2%80%93query_separation), i.e. be *either* an imperative command or a query. 

**Unix Philosophy**
Design programs to be [minimalistic](https://en.wikipedia.org/wiki/Unix_philosophy), light-weight and reusable.





