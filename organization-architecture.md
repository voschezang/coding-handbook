# Tradeoff in the Architecture of Organizations, Workflow and Products

Disclaimer:

* The best choice is *context-dependent* (i.e. ambiguous). Adapt if the environment changes.
* Always consider the options in between two extremes.
* In addition, consider the *impact*, and whether the decision is easily *reversible* (or adaptable).




## Organizations

* Organization workflow: waterfall, agile, or anarchy.
    * The latter can be effective in for example R&D.
    * The more important question is: "How much upfront planning is required in advance of experimentation."
* Organization structure: functional (by type, e.g. `Dev, Ops`) or market/product-based (e.g. `DevOps`).
    * Optimize for *cost* or for *speed*.
    * Different levels typically have a different structures (e.g. `organization, department, team`).
    * Local changes are easy and global changes are expensive. Embrace independent, autonomous teams.
        * You build it, you run it, you own it.
    * These structures show up at the level of technology (e.g. code) as well.
* Focus vs. diversification (as an organization, team, team-member).
    * E.g. work on all important areas (ticking all the boxes) or choose a subset of them to focus on.
* Adapt to change - be consistent (conservative)
    * Adapt target conditions (be pragmatic) - invest in removing obstacles and bottlenecks
    * Cohesion of products - flexibility in product designs.
* Failure of components or services
    * Resilient to failure, but allowing higher failure rates
    * Strongly impacted by failure, but immediately resolving failures and continuously reducing failure rate.
* Optimize for growth or value.
* Time-horizon
    * Accumulate technical debt (i.e. invest) - reduce technical debt (or quality debt, skill debt)
        * Note that not all technical debt has to be paid off; code can simply be deprecated.
    * Prioritize important tasks - short tasks
* Collaboration: centralized or decentralized responsibilities and decisions.
    * Number of teams/products per by PO and per scrum master.
    * Combined product owner and scrum master roles - distribution of roles across multiple people.
* Economic profit - accounting profit
* Simplicity (high bias) - complexity ([high variance](https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff))
* Specificity - generality



## Programming
* Application architecture: coupled or decoupled components
    * E.g. monolithic, layered, CQRS, event-sourcing.
* (Eco-)System architecture: monolithic or microservice.

* Version control:
    * Multiple branches, but moving changes in one direction through environments (e.g. `dev -> test -> production`).
    * A single main branch (trunk), where each environment is checked out at a specific commit/state (e.g. using tags).
* Small, predictable stories or tasks - large, meaningful, unpredictable stories

**Solutions**

* Simplicity (high bias) - complexity ([high variance](https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff))
* Specificity - generality

**Language Design**

* Default visibility of attributes and methods: `public` or `private`.
* Mutable or immutable data.
* Ordering or [structure](https://en.wikipedia.org/wiki/AoS_and_SoA) of data: a _set_ of objects or an object with arrays.
    * The former is readable and intuitive, the latter let's you do linear algebra

## Experimental Design

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



