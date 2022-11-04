# Tradeoffs in the Architecture of Organizations, Workflow and Products

> Software architecture and organizational architecture are intertwined.

Dependencies between teams affect both how software grows and the lead time of new features. See also [organization-structure.md](organization-structure.md).

[toc]

General strategy

* The best choice is *context-dependent* (i.e. ambiguous). Adapt if the environment changes.
* Always consider the options in between two extremes.
* In addition, consider the *impact*, and whether the decision is easily *reversible* (or adaptable).

## Principles

**Qualities**

What to optimize a system for

* Change-oriented
  * Data mutations.
  * Structure or system mutations.
  * Scalability
* Queries

**Organizations & bureaucracy**

* Teams are interdependent. Due to communication overhead, the effectiveness of a team decreases as a function of its size.

* The flexibility and resilience of an organization depends on the fluidity of teams and also on the interaction between teams.
* Autonomy comes at the cost of alignment.
* Formalization has limits.
* Formal processes create incentives to game the system.

**Bureaucracy**

Bureaucracy limits innovation

* Bias against investment and experimentation. Assignment of minimal resources by default. Requirement to write down beforehand what the end result will be.
* Waste through marketing/advertising: Employees compete against each other for funding.

## Tradeoffs

### Organizations

* Organization workflow: waterfall, agile, or anarchy.
  * The latter can be effective in for example R&D.
  * The more important question is: "How much upfront planning is required in advance of experimentation."
* Organization structure: functional/specialist (by type, e.g. `Dev, Ops`) or market/product/client-based (e.g. `DevOps`).
  * Optimize for *cost* or for *speed*.
  * Different levels typically have a different structures (e.g. `organization, department, team`).
  * Local changes are easy and global changes are expensive. Embrace independent, autonomous teams.
  * These structures show up at the level of technology (e.g. code) as well.
* Focus vs. diversification (as an organization, team, team-member).
  * E.g. work on all important areas (ticking all the boxes) or choose a subset of them to focus on.
* Unity/cohesion/diversity -  diversity/flexibility.
  * Adapt target conditions (be pragmatic) - invest in removing obstacles and bottlenecks
  * Cohesion of products - flexibility in product designs.
* Optimize for productivity (output) - value (flexibility)
  * E.g. a feature factory (output) vs. an organization of learning (agility).
* Failure of components or services
  * Resilient to failure, but allowing higher failure rates
  * Strongly impacted by failure, but immediately resolving failures and continuously reducing failure rate.
* Optimize for growth or value.
* Centralized or decentralized responsibilities and decisions (spider vs. starfish)
  * Isolation and separation - redundancy and resilience.
  * Number of teams/products per by PO and per scrum master.
  * Combined product owner and scrum master roles - distribution of roles across multiple people.
  * A priori choice:
    * In case of software: default to spider model for its simplicity and predictability.
    * In case of organizations: default to a mix, due to the unpredictability of humans.
* Cooperation or competition.
  * Cooperation stimulates organizational learning (shared goals).
  * Competition is a good motivator, but can harm both people and organizations. It gives and incentive for cheating and sabotage. It stimulates tribalism (Us vs. Them).
* Economic profit - accounting profit
* Simplicity (high bias) - complexity ([high variance](https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff))
* Specificity - generality
* Problem solving - problem mitigation, trading one set of problems in for another.
* Reward process - outcome.
* Alignment - autonomy (of teams, employees)
  * Employees that are autonomous and independent - employees that obey commands and are predictable.

* Formal - informal communication

### Products

* Optimize for quality or quantity.
  * E.g. optimize user-experience, or minimize cost.
* Time-horizon (long-term or short-term)
  * Accumulate technical debt (i.e. invest) - reduce technical debt (or quality debt, skill debt)
    * Note that not all technical debt has to be paid off; code can simply be deprecated.
  * Prioritize important tasks - short tasks
* Big bang releases - continuous delivery.

### Programming

* Application architecture: coupled or decoupled components
  * E.g. monolithic, layered, CQRS, event-sourcing.
* (Eco-)System architecture: monolithic or microservice.
* Version control:
  * Multiple branches, but moving changes in one direction through environments (e.g. `dev -> test -> production`).
  * A single main branch (trunk), where each environment is checked out at a specific commit/state (e.g. using tags).
* Small, predictable stories or tasks - large, meaningful, unpredictable stories
* Reliability or efficiency: e.g. automate risky tasks or time-consuming taks

**Solutions**

* Simplicity (high bias) - complexity ([high variance](https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff))
* Specificity - generality
* Efficiency - redundancy
  * Cohesion: local flexibility to change e.g. a db schema without affecting other components.

**Language Design**

* Default visibility of attributes and methods: `public` or `private`.
* Mutable or immutable data.
* Ordering or [structure](https://en.wikipedia.org/wiki/AoS_and_SoA) of data: a *set* of objects or an object with arrays.
  * The former is readable and intuitive, the latter let's you do linear algebra

### Experimental Design

Embrace a culture of learning.

* Do collaborate & discuss, and challenge your assumptions.
* Limit the scope of experiments and MVP's. Make sure that you have the ability to kill them.
* Consider the following ([tradeoffs](https://twitter.com/johncutlefish/status/1400681664225837057)):
  * Local - global
  * Flexible - rigid
  * Short duration - long duration
  * Short feedback loops - long feedback loops
  * Invitation - imposition
  * Minimal & compact - fully self-contained
  * Value in side-effects - risk in side-effects
  * Low threat to status quo - challenges status quo & conventions
