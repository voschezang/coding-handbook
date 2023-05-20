# Software Engineering

Software development used to be *just* a chaotic, creative endeavour. However, gradually some **principles** are starting to emerge, making it more predictable and rigorous. The field seems to be inherently interdisciplinary. On the one hand it involves theoretical subjects such as [computer](https://en.wikipedia.org/wiki/Computer_science) and [computational](https://en.wikipedia.org/wiki/Computational_science) science, [information](https://en.wikipedia.org/wiki/Information_science) science, mathematics and statistics. On the other hand, it relates to people, product, project and operations management. See also [software product management](product-management.md).

[toc]

## Overview

Software engineering can be described from multiple points of view. In addition, it can be done in a specific [domain](software-domains.md).

Usually it consists of either:

- Domain modeling. E.g. encode business logic in a spreadsheet.
- Translating models. E.g. port a program to another language to improve performance.
- Architecture & modeling. Design compute, storage and communication. E.g. solution architecture, systems design.

**Daily Work**

1. Planning of work. E.g. [requirements engineering](requirements-engineering.md), design, stakeholder/customer management, administration.
2. Planned work. E.g. programming, designing, having discussions, reviews, testing, research, teaching.
3. Unplanned work. E.g. incident handling, customer support, troubleshooting.

**Responsibility**
Depending on the level of specialization of the team or department:

- Developing a new product, service or component.
- Managing a software product or service.
- Managing a specific component in a *value chain*. E.g. software development.

**Value chain: the process from fresh idea to production**
These phases can vary; them may take hours or years and they can be done by the same team or by specialized teams.

1. Strategy
2. Research
3. Design
4. Development
5. Testing
6. Operations, support, maintenance
7. Lifecycle management

The following are related, but are usually delegated to other people:

- Marketing
- Sales
- HR

See [software development cycle](software-development-cycle.md).

**Roles**

- Specialist / individual contributor. A domain expert. E.g. specialized consultancy.
- Engineering manager. Organizational structures and the work environment, rather than work itself: e.g. teams, people, processes.
- Technical leadership. Manage technical vision/risks/requirements. Take responsibility for the effectiveness of a development team or department. Communicate between technical and non-technical staff and stakeholders.

## Software methods

### Stability

There doesn't exist a method that guarantees bug-free code. Don't make assumptions about the reliability of code but instead verify it. This requires the following points:

- Visibility, Transparency, Traceability

  - Clear [documentation](documentation.md). An explanation from high to low level and including relevant assumptions.
    - This can be complemented by "How-to" guides.
  - Ensure that there is up-to-date documentation that is clear and covers both the components and the interactions of the system.
  - [Observability](https://en.wikipedia.org/wiki/Observability).  Two definitions
    - Being able to infer the state of a system based on its outputs.
    - Being able to see inside the system: distributed tracing.
  - (predictive) monitoring and alerting.
    - Based on service level objectives (SLO) and indicators (SLI).
  - Application performance measurement (APM)

- Software Quality

  - Code quality, decent code coverage. Good unit-tests and complementing integration tests.
    - Multiple levels of testing. E.g. `unit, system, functional, performance`.
    - Representative tests. E.g. a sandbox-environment that is effectively equivalent to the production-environment.

  - Clear documentation and specification; from high to low level, including relevant assumptions.
    - This allows obsolete code to be more easily removed, eventually reducing the entropy of a codebase.

- Automation.

- Good software, system and organizational architecture.

  - Teams that are in control of their own application. Without agency they cannot realistically be accountable.

  - A third-party should not be able to change the application outside the control of the team itself. Consider hair triggers and safety caps.

    - `You build it you run it.`

  - The team should be able (authorized) to block the release of a change they don't support.

  - The team should be able (authorized) to block the release of a change they don't support.
  - Communication between teams and departments. Both personal and using proper APIs.

- Risk management. E.g. thread modeling. See [management principles](management-principles.md).

**Tips / Habits**

- Don't deploy on Friday or in the evening, unless there is a good reason for it.
- Do regular gardening/grooming, e.g. every Friday.
- At the end of each day, spend a few minutes cleaning up.
- Take time every to reflect and question your way of working.
- Go to bed early.

### Maintainability

> Most time is spend on maintenance, rather than development of new software.

Change is inevitable in software engineering. It can be caused by:

- A change in customer requirements or user preferences.
- A change in stakeholder requirements.
- Changes in the environment, e.g. in technology.
- More information that is available. E.g. after learning.

See [programming-paradigms](computer-language/programming-paradigms.md).

### Clean Code

> Design for replacement rather than reuse.

> Clean interface > clean code

Although there is no consensus on the definition of "clean" code, some indisputable properties are the following.

- Consistency of style.
- Meaningful variable names.

- Separation between [commands and queries](https://en.wikipedia.org/wiki/Command%E2%80%93query_separation) should be the norm. Only combine them by exception, for good reasons.

- Simple interfaces for public methods.

See also [programming-paradigms.md](computer-language/programming-paradigms.md) and [style-guide.md](computer-language/style-guide.md).

### Testing

Also see *Integration & Delivery* below.

> The entropy (complexity) of software without "good" tests can only increase. Tests allow features to be safely removed.

The term testing is usually used for "checks". A distinction can be made based on the role of requirements.

- No requirements: Testing. E.g. `observing, exploring, experimenting`.
  - Learn something new. Do research. This is inherently unpredictable. Techniques to improve consistency are:
    - Time-boxes. Zoom in and out.
  - Black box: study the different inputs and outputs of a system.
  - White box: study the inner systems.
- Requirements: Checking.
  - Verification and validation based on pre-specified requirements
    - This can often be **automated**
  - [TDD](https://en.wikipedia.org/wiki/Test-driven_development): write small tests (checks) first, and the implementation second.
    - Strong TDD: Write a minimum failing test, write minimum code to fix the test, then refactor without introducing new behaviour.

In the absence of pre-specified requirements it is still possible to list all the dimensions (properties) of the system and consider how they can be measured.

No testing.

- Develop a PoC, then evaluate whether it should be put into production, and only then continue with TDD on that specific feature. This means that there are no tests written for unused code.

**Test Pyramid**
Rely on unit-tests (checks) to verify that requirements or specifications are met. Decompose large integration tests.

- UI should have unit-tests.
- Tests for interfaces can be generated automatically.

**Anti-pattern**
Ice-cone: inverse testing pyramid. Too many integration and UI tests, which are slow, unmaintainable and too sensitive.

### Other Metrics

- Lead time
- Deployment frequency (to customer)
- Mean time to repair/recovery/restore ([MTTR](https://en.wikipedia.org/wiki/Mean_time_to_repair))
- Change fail percentage

Biased metrics

- Lines of code (LOC): incentive to produce boilerplate code and to never deprecate code
- Velocity: incentive to increase bulk sizes, preference for large, risky projects
- Utilization: incentive for silo's, status quo and efficiency (rather than innovating)

## Software Quality

Two types

- External software quality; visible to users.
  - Users are directly impacted by this.
- Internal software quality; invisible to users.
  - Users are indirectly impacted by this, through lead time..

Code reviews

- Based on the risk/impact of the work
- Based on how "clean" the code is

### Technical Debt

Technical debt is an investment. It is risky, especially when the aggregate debt is kept unchecked. The typical example is to trade in quality in order to release faster. Given that requirements usually change over time, technical debt doesn't always have to be "paid back". The tradeoff can be summarized as: "You ain't gonna need it" vs. "you're not gonna fix it later".

In order to reduct risk, technical debt can be made explicit.

- Document imperfect implementations.
  - In code. E.g.:
    - `raise NotImplementedError`
    - Comments: `TODO, FIXME, SMELL`
  - In external documentation

Types

- Confusing requirements. E.g. a design that is perceived as a bug by users.

- Missing functionality.

  - Low quality, sensitivity to small perturbations. E.g. special characters.
  - Outdated software.

- Lack of documentation.

- Lack of tests.

- Unnecessary complexity.

  - Higher learning curve.
    - Increased onboarding time

  - Risk of bugs, inconsistencies, unexpected behaviour

- Bad interfaces. This may result in lot's of duplicate code.

## Types of Work

Ordered along the [Cynefin domains](https://cynefin.io/wiki/Cynefin) `chaotic-complex-complicated-obvious`. Also see [Traditional Paradigms](#Traditional%20Paradigms).

1. Research (theoretical, experimental), deconstruct the application domain.
2. Development: novelty, effectiveness, build/improve an application. I.e. invest and introduce change.
3. Operations: efficiency & quality, run a black-box application. I.e. cut cost and block change. Execute a process.
4. Administration: consistency, manage a black-box application. Audit an executed process.

Addition

- Managing X: making sure X is done in a certain way or at a larger scale. See [systems-management](systems/systems-management.md).

[DevOps](quotes.md): vertical integration of development, operations and more. A single team that builds and runs an application or service.

**Traditional Paradigms**

With minimal collaboration, roles could be distributed as follows. The alternative would be a cross-functional team.

- Architect: designs theoretical systems. Facilitate decision making.
- Developer: turns requirements into code.
  - Senior: write interfaces. Coach others. Take ownership. Adapt.
  - Junior: write implementations. Follow instructions. Experiment.

- Tester: turns code into bug-reports.
- PO: manage product and stakeholders, requests features.
- Scrum master: process management, coaching, HR.

### Integration & Delivery

In the broadest sense this would be integration of units of work. E.g. merging source code or sitting together in a cross-functional team.

The rate of integration directly affects the tome to receive and act upon feedback.

- [Continuous](https://en.wikipedia.org/wiki/Continuous_delivery). E.g. committing directly to the main production branch.
- Days or weeks. E.g. short-lived feature branches.
- Months or years. E.g. working in parallel branches.

In practice, different changes may be integrated at different time scales. E.g.:

- Linting (in milliseconds)
- Local unit tests (seconds to minutes)
- Continuous integration (minutes)
- Continuous deployment (minutes to hours)
- Canary releases (minutes to days)
- Full releases

**Risk.** Changes can impact stability. Risk mitigation can be done by these two strategies:

- Separation by demographic. E.g. [canary releases](https://martinfowler.com/bliki/CanaryRelease.html) where software is released gradually. In case of risk materialization, this will limit the impact to users and it will allow developers to address issues immediately.
  - This increases the time-to-market, similar to the concept of a one-by-one production flow.
  - This incentivizes good metrics that track not just quality but also market-fit - and outcomes.
  - This embraces learning. The early customer-feedback allows plans to be re-adjusted before sunk costs make it practically impossible.
- Separation by non-production environments. E.g. [DTAP](https://en.wikipedia.org/wiki/Development,_testing,_acceptance_and_production).
  - This introduces safety barriers at the (potential) cost of time-to-market.
  - There is a risk falling for the sunk cost fallacy. Once something has passed through multiple time-consuming or expensive stages, it becomes politically difficult to cancel.

**Release train.** The main goal is to improve predictability of software releasees. Optimize for a certain release size at fixed intervals. The train consists of stages that first add or integrate software and then a number of filters that don't add functionality but instead protect the end-product from faulty changes being introduced. Once a stage fails the release is cancelled and the work is deferred to the next scheduled release date, thus increasing inventory. Different stages can be picked up either by multiple specialized teams or by a single cross-functional team.

This pattern has some downsides:

- It requires a high level of synchronization between teams and components.
- It may create an incentive to build a "feature factory", with a bias for LOC or number of features, over customer value.

### Collaboration

The typical method of specifying work in a development team is based on user- or tech-**stories**. The assignee or owner of a story will try to either finish the story quickly or assign resources such that the story  doesn't take unnecessary long.

On a daily basis there can be a *standup*, which is a briefing that covers at least any deviations from the planning and optionally some relevant updates. This meeting will go over either (1) all tasks that are *in progress* or (2) all team members. The former has the advantage of identifying any tasks that are blocked.

**Levels of collaboration in a team**

The ratio of number of (independent) stories versus team members affects the average lead time of stories. In addition, it affect the level of awareness of each other's work. Note that these results are affected by other factors as well. E.g. the amount of informal communication between colleagues.

A few types of team collaboration:

- **Silo's**. One person works on one story. This optimizes for *utilization*. This can be efficient, but there is a risk of long waiting time due to asynchronous reviews.  If there is a need for reviews, then stories tend to be on hold disproportionally often. Each person may defer the reviewing of other people's work as soon as they have time for it. Hence there is an incentivize for workers to start new tasks, whenever other tasks are blocked. This increases work-in-progress, and it results in more context switching. Both of these decreases lead time.
- **Pairing** and mobbing. The team is split up and each sub-group works together on a single story. This optimizes for *quality* and *lead time* of the stories with the highest priority. Lower priority stories are started later. This requires an explicit prioritization, which has organizational implications. Deferring
- **Swarming**. This is an extreme version of pairing. This optimizes for *speed*. A large group focusses on a single task and drops everything else. For example, fixing a major production issue as soon as possible.

**Reviews**

Usually there is a need for reviews before code can be integrated. In general:

- Large, infrequent reviews are efficient but inflexible. Reviewing them properly is time-consuming - and thus may be postponed. If reviewers find problems then it's either too late, or it would cause significant rework. This reduces quality.
- Small, frequent reviews improve quality. However, they can also be disruptive.
  - Continuous reviews are less disruptive as they avoid context switching. However, they do require synchronization.

This seems to imply a tradeoff between quality and throughput. However, these two are intertwined. Low quality may cause rework, which in turn will decrease throughput.

The ideal way to achieve both quality and throughput is through *fast* reviews. This would require:

- High awareness. This improves the time per review.
- High availability. This improves the waiting time before a review starts.

This puts a restriction on the amount of work in progress.

**Scrum or Kanban board**

Roles:

- Transparency and visibility of the teams goals and the progress towards it.
  - Show what is planned, in progress and finished.
  - Ensure that priorities are aligned.
  - Incentivize collaboration by showing what is being worked on by whom.
- Visualize bottlenecks and blockers.
- Accountability of the work that's being done.
- Externalize planning. Increase resilience and decrease dependence on a single team member.

It helps to avoid:

- Errors related to planning and handovers.
- Invisible bottlenecks.

## Programming productivity

**Language/System Agnostic**

1. Blind, fast typing, muscle memory. Typing without conscious thinking.
2. `vi`/`vim` commands: manipulating text files
4. `grep`, `sed`, regular expressions: quickly writing queries for and through files). E.g. to search through log-files.

**Tools**

1. Version control (e.g. `git`). Usually using [multiple repositories](https://danluu.com/monorepo/).
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
