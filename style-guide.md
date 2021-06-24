# Style Guide

* Never deviate from the following guidelines. If you do anyway, carefully consider the implications.
* These guidelines do not reflect the opinions of my past and future employers and employees.




## Specification

Twofold:

1. Describe behaviour of the system; how it reacts to inputs.
    - This part may be complex, but start with an high level, treating the internals as a black box.
2. Describe the boundaries of the system; list all inputs and outputs.

Avoid or resolve ambiguity.

* *Complicated* is just a euphemism for "scary to think about".



## Documentation

**Ordering**

Explanations can be top-down (high level first) or bottom-up (low level first).

- The first is intuitive, but requires the repeated use concepts that are not well-defined (yet).
    - Start with *What* and *Why* instead of the *How*.
- The second allows you to start from fundamental principles, but requires a bit up-front investment from the reader
    - There is a risk of missing the global point.



**Complexity**

Multiple levels of documentation, ordered by level of natural language (increasing).

1. Module level. 
    - Clean, clear, readable code. From high level to low level. E.g. self-explanatory variable- and file-names.
    - Inline comments and doc-strings.
    - Up-to-date, readable **tests** that act as a specification.
2. Application level. High cohesion.
    - Self-contained repositories with a readme.
3. System level. Relations between multiple components. E.g. a wiki.




## Design
- Code should not be clever. Designs should be as simple as possible, but not simpler.
  - Solutions may be [insightful](https://www.hillelwayne.com/post/cleverness/) but be careful with assumptions and constraints.
- First solve the problem (e.g. proof that specification is correct), then write code.
- Documentation should be written top-down rather than bottom-up. The latter requires a big upfront investment from the reader.
- *Low* level code changes more often than *high* level code.
  - E.g. a change in an interface requires a change in the implementation but not the vice versa.
- *Generic* code changes more frequently than *specific* code.
  - E.g. linear algebra libraries are unaffected by changes in customer preferences.
- Interfaces should be backwards compatible. Otherwise create a new interface. Only if that is not possible, break the interface and update all implementations.




## Variable names

* Variable (attribute) names should be self-explanatory. 
   * Don't use the type of a variable as its name. 
      E.g. `dataframe_list = list(DataFrame())`.
   * Don't prefix variables with nondescriptive terms such as `do, perform, execute, determine, compute, establish`.
   
* Don't use overly complex object names, especially if they cause error messages that overflow the terminal buffer.
  * E.g. `org.java.beans.beancontext.BeanContextServiceProviderBeanInfo`


## Classes & methods

* The average number of lines per function or method should be `5`.

* When writing Python, don't make it look like Java.
```diff
- if (obj.data.getSize() == 0) {
-     return apple.getWeight() + grapes.getFromIndex(0);
- }
+ if obj.data:
+     return apple.weight + grapes[0]
```

* Don't unnecessarily wrap functions in classes.

* When designing classes, use class-composition by default and class-inheritance otherwise.

* Using `GetType(obj)` is an indicator of poor OOP design.


## Formatting

* Use _language-specific_ autoformat.


## Data

Always consider the tradeoffs of `AoS` and `AoS` (array of structures, structure of arrays, e.g. in terms of usability, performance, scalability.
```py
class Agent  = {.name, .position, .velocity}
class Agents = {Agent(), ..}
```



```py
class Agents = {names = [], positions = [], velocities = []}
```

