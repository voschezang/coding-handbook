# Style Guide

* Never deviate from the following guidelines. If you do so anyway, carefully consider the implications.
* These guidelines do not reflect the opinions of my past and future employers.

[toc]

## Documentation

See [documentation](documentation.md).




## Design
- Code should not be clever. Designs should be as simple as possible, but not simpler.
  - Solutions may be [insightful](https://www.hillelwayne.com/post/cleverness/) but be careful with assumptions and constraints.
- First solve the problem (e.g. proof that specification is correct), then write code.
- *Low* level code changes more often than *high* level code.
    - A change in an interface requires a change in the implementation but not the vice versa.
- *Generic* code changes less frequently than *specific* code.
  - E.g. linear algebra libraries are unaffected by changes in consumer preferences.
- Interfaces should be backwards compatible. Otherwise create a new interface. Only if that is not possible, break the interface and update all implementations.
    - Design for [replacement](https://martinfowler.com/bliki/SacrificialArchitecture.html) rather than reuse.

- Log and monitor everything. Build this into the design instead of adding it later.



## Tests

See [testing](software-engineering.md#Testing)

- Strive towards a single unit-test per test, rather than a single assertion per test.




## Variable names

* Variable (attribute) names should be self-explanatory. 
   * Don't use the type of a variable as its name. 
      E.g. `dataframe_list = list(DataFrame())`.
   * Don't prefix names with non-descriptive terms such as `do, perform, execute, determine, compute, establish`.
* Don't use overly complex object names, especially if they cause error messages that overflow the terminal buffer.
   * E.g. `org.java.beans.beancontext.BeanContextServiceProviderBeanInfo`



## Classes & methods

* The average number of lines per function or method should be `5`.
* When writing Python, don't make it look like Java.
```diff
- if (obj.data.getSize() > 0) {
-     return (apple.getWeight(), grapes.getFromIndex(0)).sumTotal();
- }
+ if obj.data:
+     return apple.weight + grapes[0]
```

* When designing classes, use class-composition by default and class-inheritance otherwise.




## Formatting

* Use _language-specific_ autoformat.




## Data

Always consider the tradeoffs of `AoS` and `AoS` (array of structures, structure of arrays). Consider terms of usability, performance, adaptability and scalability.
```py
class Agent  = {.name, .position, .velocity}
class Agents = {Agent(), ..}
```



```py
class Agents = {names = [], positions = [], velocities = []}
```



Tuples should not have a length greater than 3 or 4 or 5. Suitable alternatives might be named tuples, records or (hash-) maps.



## Flow

- Make the flow of a procedural program trivial to understand.
    - Avoid unnecessary indentation.
    - Simplify [conditionals](https://en.wikipedia.org/wiki/De_Morgan's_laws). Moving negations outside is usually more intuitive.

E.g.

``` python
def f(a, b, c):
    if not a: 
        return 1
    if b: 
        return 2

    later()
    return 3
```

