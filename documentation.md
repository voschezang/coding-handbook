# Documentation

[toc]

Functions of writing

- Past events: documenting
- Now: deconstructing, exploring
- Future events: delegating



**Types of documentation**

Documentation should not only be written for a specific audience, but it should also have a specific [functionality](https://documentation.divio.com/).

|               | [Tutorial](https://documentation.divio.com/tutorials/#tutorials) | [How-to guide](https://documentation.divio.com/how-to-guides/#how-to) | [Reference](https://documentation.divio.com/reference/#reference) | [Explanation](https://documentation.divio.com/explanation/#explanation) | Specification                        |
| ------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------ |
| *oriented to* | learning                                                     | a goal                                                       | information                                                  | understanding                                                | formalization                        |
| *must*        | allow the newcomer to get started                            | show how to solve a specific problem                         | describe the machinery                                       | explain                                                      | be testable                          |
| *its form*    | a lesson                                                     | a series of steps                                            | dry description                                              | discursive explanation                                       | requirements                         |
| *analogy*     | teaching a small child how to cook                           | a recipe in a cookery book                                   | a reference encyclopaedia article                            | an article on culinary social history                        | the definition of a Pizza Margherita |

- Tutorials and explanations are educational and thus suitable for learning.
- How-to guides and references are informational and more suitable for work.



**Maintaining Documentation**

This is even harder than writing good documentation. A standard way to maintain high quality is to continuously update documentation. Whenever an aspect of the subject is changed, ensure that the result is reflected in the documentation. 



## Structure

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



**Comments**

Comments are metadata. They do increase maintenance. A few categories:

- Functional comments: `TODO`, `SMELL`
    - These can be useful even if they are never addressed. They visualize code quality and warn contributes about missing or broken functionality.

- Documenting why vs. what.
- Giving examples
- Giving references (to external documentation)

The Why consists of the following categories:

- Context
    - Negative information (what is not happening).
    - Rationale, history
- Performance
- Use-cases, side-effects
- Tips



## Specification

Testable requirements. Functional or non-functional.

1. Describe behaviour of the system; how it reacts to inputs.
    - This part may be complex, but start with an high level, treating the internals as a black box.
2. Describe the boundaries of the system; list all inputs and outputs.
3. Describe the purpose of the system. This may result in some non-functional requirements.

Avoid or resolve ambiguity.

>  *Complicated* is just a euphemism for "scary to think about".

