# Software Engineering

As a discipline.



**Software methods**

There doesn't exist a method that guarantees bug-free code. Don't make assumptions about the reliability of code but instead verify it. This requires the following points:

- Transparency, Traceability, Visibility. 

    - E.g. (predictive) monitoring and alerting.
    - Ensure that there is up-to-date documentation that is clear and covers both the components and the interactions of the system.

- Testing.

    -  E.g. a sandbox-environment that is effectively equivalent to the production-environment.
    - Multiple levels of testing. E.g. `unit, system, functional, performance`.

- Automation.

- Teams that are in control of their own application. Otherwise they cannot be really accountable.

    - A third-party should not be able to change the application outside the control of the team itself. Consider hair triggers and safety caps.

        - > You build it you run it.


    - The team should be able (authorized) to block the release of a change they don't support.

- Communication between teams and departments. Both personal and using proper APIs.

- Risk management. E.g. thread modeling.



**Types of work**

Ordered along the [Cynefin domains](https://cynefin.io/wiki/Cynefin) `chaotic-complex-complicated-obvious`

1. Research (theoretical, experimental), deconstruct the application domain.
2. Development: novelty, effectiveness, build/improve an application.
3. Operations: efficiency, run a black-box application.
4. Administration: consistency, manage a black-box application.



**Ways of working**

Ordered descending by release time and size (lead-time).

1. Waterfall: long cycles, clearly separated stages (design, develop, test, release).
2. Agile: iterative improvement, short feedback loops.
    1. Scrum: sprinting to a goal, MVP-first
    2. Kanban: continuously improving
    3. The hacker way: no deadlines, no fixed teams, no synchronization.



**Testing**

Three methodologies:

- Write spec, then code, then test.
- TDD
- Develop a PoC, then evaluate whether it should be put into production, and only then continue with TDD on that specific feature.



**Traditional Paradigms**

With minimal collaboration, roles could be distributed as follows. The alternative would be a cross-functional team.

- Architect: designs theoretical systems.
- Developer: turns requirements into code.
    - Senior: write interfaces.
    - Junior: write implementations.
- Tester: turns code into bug-reports.
- PO: requests features.
- Scrum master: process management, coaching, HR



**Tips**

- Don't deploy on Friday or in the evening, unless there is a good reason for it.
- Do regular gardening/cleaning/grooming, e.g. every Friday.



### Programming productivity

**Language/System Agnostic**

1. Blind, fast typing, muscle memory. Typing without conscious thinking.
2. `vi`/`vim` commands: manipulating text files
4. `grep`, `sed`, regular expressions: quickly writing queries for and through files). E.g. to search through log-files.



**Tools**

1. Version control (e.g. `git`)
2. A simple editor with syntax highlighting, syntax checking, type checking, linting, etc.
3. An advanced editor (IDE).
4. CI/CD pipelines.



An IDE could:

- Predict compilation errors
- Predict runtime errors
- Visualize test coverage (both individual lines and variable-ranges)
- Refactor:
    - Flip branches.
    - (Un)Negate statements.
    - Convert between [CNF](https://en.wikipedia.org/wiki/Conjunctive_normal_form) and [DNF](https://en.wikipedia.org/wiki/Disjunctive_normal_form).
    - Extract/encapsulate variables.
    - Generate tests.
    - Inline functions.

