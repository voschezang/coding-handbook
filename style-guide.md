# Style Guide

* Never deviate from the following guidelines. If you do anyway, carefully consider the implications.

* These guidelines do not reflect the opinions of my past and future employers and employees.


## Design
- Code should not be clever. Designs should be as simple as possible, but not simpler.
  - The plurar of regex is regret.
- First solve the problem (e.g. proof that specification is correct), then write code.
- Documentation should be written top-down rather than bottom-up. The latter requires a big upfront investment from the reader.

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

---

## Data

Always consider the tradeoffs of `AoS` and `AoS` (array of structures, structure of arrays, e.g. in terms of usability, performance, scalability.
```py
class Agent  = {.name, .position, .velocity}
class Agents = {Agent(), ..}
```



```py
class Agents = {names = [], positions = [], velocities = []}
```

