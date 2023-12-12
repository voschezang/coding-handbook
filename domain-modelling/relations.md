# Relations

Objects can be represented by symbols, names or exclusively by *relations* with other objects. E.g. the name "my birthday" or the relation "1 year *after* my birthday". A relation can be defined as the *reason* of an association. Note that relations can be chained together.

A relation can have [domains](https://en.wikipedia.org/wiki/Domain_of_a_function), similar to [functions](https://en.wikipedia.org/wiki/Function_(mathematics)). These can be named explicitly, using *roles*. E.g. an *interviewer* that interviews and *interviewee*. Here, both roles draw from the domain *persons*. In practice, relations may be recorded in a single direction. E.g. using a key-value map. Traversing relations in the "natural" direction is optimal, while the opposite direction can be performance-intensive.

Relations can be *one-to-one*, *one-to-many* (books and pages) or *many-to-many* (books and authors). In practice, a many-to-many relationship can be modeled by a one-to-one mapping which is complemented by a list of exceptions.

Instances of relationships can have attributes. E.g. the *date* of a marriage between people.



## Properties & Restrictions

Directional. `f(x, y)` does not imply that `f(y, x)`

[Transitive](https://en.wikipedia.org/wiki/Transitive_relation): If `f(x) = y` and `g(y) = z` then there exists `h` s.t.  `h(x) = z`

Implication (composition). If `f(x, y)` and `f(y, z)` then `f(x, z)`

[Symmetric](https://en.wikipedia.org/wiki/Symmetric_relation): If `f(x) = y` then `f(y) = x`

Antisymmetric: If `f(x) = y` then `f(y) != x`

[Reflexive](https://en.wikipedia.org/wiki/Reflexive_relation): If there exists an `f` s..t `f(x) = x` for every `x`



