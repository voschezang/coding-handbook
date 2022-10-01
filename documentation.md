# Documentation

[toc]

## Audience & Author

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

**Views**

Documentation (and visualizations) can be created at different [levels of detail](https://en.wikipedia.org/wiki/C4_model). E.g.

1. Context. How it relates to the outside world.
2. The messy middle
    1. Behaviour of the system itself. How it changes.
    2. Components and the relations between them. What the responsibilities are.
3. Inner workings of a given component.



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

Comments are metadata. They do increase maintenance. In contrast to programming languages, they do not have syntax or grammar restrictions. They can be tailored towards the audience, e.g. in a native language rather than english.

A few categories:

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



## Templates

To visualize systems, long-running processes, value chains and pipelines. See also [systems-management](systems-management.md).



**Outside view**

System as a black box. Focus on inputs and outputs.

<img src="img/system-flow-value.png" alt="system-flow-value" style="width:50%;" />

**Value Chain(s)**

<img src="img/feature-functional-teams.png" alt="feature-functional-teams" style="width:60%;" />

**Functional view**

Activities and communication

<img src="img/bpmp-simple.png" alt="bpmp-simple" style="width:50%;" />

**Ownership / Responsibility**

<img src="img/bpmp-ownership.png" alt="bpmp-ownership" style="width:50%;" />

<img src="img/bpmn-responsibility.png" alt="bpmn-responsibility" style="width:50%;" />

**Commoditization of Components**

<img src="img/map-commoditization-visibility.png" alt="map-commoditization-visibility" style="width:60%;" />

**Queues**

<img src="img/scheduling-slack.png" alt="scheduling-slack" style="width:80%;" />



**Resource Contention**

<img src="img/critical-chain.png" alt="critical-chain" style="width:60%;" />

