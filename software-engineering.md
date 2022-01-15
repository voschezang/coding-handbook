# Software Engineering

As a discipline.

Also see [Product Management](product-management.md).

[toc]

## Software methods / Bugs / Stability

There doesn't exist a method that guarantees bug-free code. Don't make assumptions about the reliability of code but instead verify it. This requires the following points:

- Transparency, Traceability, Visibility. 

    - E.g. (predictive) monitoring and alerting.
    - Ensure that there is up-to-date documentation that is clear and covers both the components and the interactions of the system.

- Testing.

    -  E.g. a sandbox-environment that is effectively equivalent to the production-environment.
    - Multiple levels of testing. E.g. `unit, system, functional, performance`.

- Automation.

- Teams that are in control of their own application. Without agency they cannot realistically be accountable.

    - A third-party should not be able to change the application outside the control of the team itself. Consider hair triggers and safety caps.

        - > You build it you run it.
    
    
    - The team should be able (authorized) to block the release of a change they don't support.
    


- Communication between teams and departments. Both personal and using proper APIs.

- Risk management. E.g. thread modeling. See [management principles](management-principles.md).



**Tips / Habits**

- Don't deploy on Friday or in the evening, unless there is a good reason for it.
- Do regular gardening/grooming, e.g. every Friday.
- At the end of each day, spend a few minutes cleaning up.
- Take time every to reflect and question your way of working.
- Go to bed early.



### Clean Code

Although there is no consensus on the definition of "clean" code, some indisputable properties are the following.

- Consistency of style.
- Meaningful variable names.

- Separation between [commands and queries](https://en.wikipedia.org/wiki/Command%E2%80%93query_separation) should be the norm. Only combine them by exception, for good reasons.



See also [programming-paradigms.md](programming-paradigms.md) and [sytle-guide.md](style-guide.md).



## Types of Work

Ordered along the [Cynefin domains](https://cynefin.io/wiki/Cynefin) `chaotic-complex-complicated-obvious`. Also see [Traditional Paradigms](#Traditional Paradigms).

1. Research (theoretical, experimental), deconstruct the application domain.
2. Development: novelty, effectiveness, build/improve an application. I.e. invest and introduce change.
3. Operations: efficiency & quality, run a black-box application. I.e. cut cost and block change. Execute a process.
4. Administration: consistency, manage a black-box application. Audit an executed process.

Addition

- Managing X: making sure X is done in a certain way or at a larger scale.

[DevOps](quotes.md): vertical integration of development, operations and more. A single team that builds and runs an application or service.



**Traditional Paradigms**

With minimal collaboration, roles could be distributed as follows. The alternative would be a cross-functional team.

- Architect: designs theoretical systems.
- Developer: turns requirements into code.
    - Senior: write interfaces. Coach others. Take ownership. Adapt.
    - Junior: write implementations. Follow instructions. Experiment.
    
- Tester: turns code into bug-reports.
- PO: requests features.
- Scrum master: process management, coaching, HR



## Ways of working

> Agile is a mindset, not a process

Ordered descending by release time and size (lead-time).

1. Waterfall: long cycles, clearly separated (but optimized) stages (design, develop, test, release). Big bang release (optics). Top-down decisions.
2. Agile: (be able to) inspect and adapt; to be able to create or adjust your own process. Use iterative improvement, short feedback loops. Bottom-up decisions (e.g. user-oriented). Defer uncertain decisions unless there is a good reason not to.
    1. Scrum: sprinting to a goal, MVP-first. Limit total WIP (number of stories).
    2. Kanban: continuously improving. Limit WIP per column (`dev, review, test, release `).
    3. The hacker way: no deadlines, no fixed teams, no synchronization.



Notes

-  Agile is a tradeoff of agility (flexibility) and efficiency. Optimizing for a given use-case does always come at the cost of being flexible. You cannot optimize for everything.
- If the full strategy is decided top-down then the agility of development teams is limited.




### Integration & Delivery

In the broadest sense this would be integration of units of work. E.g. merging source code or sitting together in a cross-functional team.

The rate of integration directly affects the tome to receive and act upon feedback.

- [Continuous](https://en.wikipedia.org/wiki/Continuous_delivery). E.g. committing directly to the main production branch.
- Days or weeks. E.g. short-lived feature branches.
- Months or years. E.g. working in parallel branches.

  

**Risk.** Changes can impact stability. Risk mitigation can be done by these two strategies:

- Separation by demographic. E.g. [canary releases](https://martinfowler.com/bliki/CanaryRelease.html) where software is released gradually. In case of risk materialization, this will limit the impact to users and it will allow developers to address issues immediately.
    - This increases the time-to-market, similar to the concept of a one-by-one production flow .
- Separation by non-production environments. E.g. [DTAP](https://en.wikipedia.org/wiki/Development,_testing,_acceptance_and_production).
    - This introduces safety barriers at the (potential) cost of time-to-market.



**Release train.** The main goal is to improve predictability of software releasees. Optimize for a certain release size at fixed intervals. The train consists of stages that first add or integrate software and then a number of filters that don't add functionality but instead protect the end-product from faulty changes being introduced. Once a stage fails the release is cancelled and the work is deferred to the next scheduled release date, thus increasing inventory. Different stages can be picked up either by multiple specialized teams or by a single cross-functional team.

This pattern has some downsides:

- It requires a high level of synchronization between teams and components.
- It may create an incentive to build a "feature factory", with a bias for LOC or number of features, over customer value.



#### Testing

Three methodologies:

- Write spec, then code, then test.
- TDD
- Develop a PoC, then evaluate whether it should be put into production, and only then continue with TDD on that specific feature. This means that there are not tests written for unused code.




### Collaboration

The typical way to plan work in a team is to use stories or tasks. The owner of a story will try to either finish the story quickly or assign resources such that the story  doesn't take unnecessary long.

On a daily basis there can be a *standup*, which is a briefing that covers at least any deviations from the planning and optionally some relevant updates. This meeting will go over either (1) all tasks that are *in progress* or (2) all team members. The former has the advantage of identifying any tasks that are blocked.



## Programming productivity

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

