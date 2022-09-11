# Product Management

This is more about *projects* than a *product*, but it borrows some useful terminology from product management. See also [goals and strategy](goals-planning-strategy.md),  [management principles](management-principles.md) and [requirements-engineering](requirements-engineering.md).

[toc]

> Product management combines short term projects with long-living products.

> Products are never finished, only deprecated.

## Introduction

**Not project, but project<u>s</u> management**
Often, projects are executed in conjunction to each other. To avoid local optimization, the portfolio of products must be taken into account. A *product* is a model that combines multiple projects, usually with the goal to deliver value to customers. See [Terminology](#Terminology).

**The problem of uncertainty**
In uncertain environments, projects will usually fail to meet either time, cost or initial requirements. In the presence of both [idiosyncratic](https://en.wikipedia.org/wiki/Idiosyncrasy) and [systematic risk](https://en.wikipedia.org/wiki/Systematic_risk) there can be a need for flexibility or agility. In product management this takes the following form:

- A product strategy may consists of [multiple](https://en.wikipedia.org/wiki/Diversification_(finance)) initiatives that are designed to create a competitive edge.
- A product roadmap lists the concrete projects that will be executed to realize this ideal.

**Product and projects**
First, there is a difference in mindset:

- **Project** mindset: Finish a fixed set of tasks within a *time* and *cost* limit.
- **Product** mindset: Continuously deliver value to a customer.

The former is ideal in a predictable environment, whereas the latter is optimal for uncertain environments. Rather than focussing on <u>successful completion</u>, it focusses on delivering value <u>sooner</u>.

In practice, products are improved through multiple small projects.

Because products are never finished, they cannot be reduced to a set of requirements. Instead they represent an outcome, which should be conveyed by telling a story or showing a vision.



### Differences

A few differences between projects and products.

**Projects** *terminate*; either successfully by meeting requirements or by reaching deadline. There is a preference for the short term (the duration of the project) over the long term (after the project).

- Optimize **cost**. Satisfy requirements as fast and efficiently as possible.

    - Build a feature/project/product, then hand it over and move on.

    - Reach the deadline at all cost; strip features or reduce quality if necessary.

**Products** are *continuous*, but may expire (based on alternatives). There is a preference for value and sustainability.

- Maximize **value**, opportunity and viability. 
    - Delivering value to customers > resource efficiency.

- Compatible with DevOps and vertical integration.
    - "You build it, you own, you run it"

- Place bets on potential wins. Prefer outcomes over meeting (initial) requirements.
    - Long-term revenue stream > quarterly results.

Projects typically have three constraints: a time bound, cost bound and a set of requirements (input or output). When risks materialize then at least one of these must be let go.



## Product Management

### Terminology

A *Product* is a proxy for the set of [products](https://en.wikipedia.org/wiki/Product_(business)) and [services](https://en.wikipedia.org/wiki/Service_(economics)) that are used by a *User*, paid for by a *Customer*. The *Stakeholder* supports the products and aims to eventually profit it, either financially or in some other way. The product is usually build and delivered by employees of an organization. The product is optimized for a target market, but can also be delivered to a boundary market.

Following this terminology, a successful product would need to fulfill the desires of customers, users, stakeholders and employees.

**Product Discovery**
Deciding what to build, for whom, when.

**Product Delivery**
Building it (R&D) and delivering it (ops).



## Background

**Types of Products**

- Traditional Product: a static object. Must be right the first time.
- "Software" Product: can be updated (patched) after the first release.
- Service: completely continuous. Regularly updated to market conditions.



**Product Portfolio**

Three innovation horizons. From exploitation to exploration.

1. Current cash-flow (value): profitable now. Risk: they may become a commodity.
2. High-growth businesses: will become cash-flow.
3. Growth options: will potentially become growth.



**Types of Customers and Stakeholders**

- The product-owner or project-manager
- The business (the rest of the organization)

- The users of a platform (e.g. sellers on ebay)
- The end-users (e.g. buyers on ebay)



**Market**

>  Good strategy means saying no.

Don't expect to satisfy all possible customers. Instead optimize for a limited subset of them.

- Target market: optimize product for this market
- Boundary: additional sales, but don't optimize product for this markter
- Excluded from target



[Market segmentation](https://en.wikipedia.org/wiki/Market_segmentation) is key because perception of value is subjective. In non-segmented markets, customers with high value perception pay just the average price and customers with relatively low value perception will not pay at all. Ideally products are optimized for a single user, at scale.



**Lifecycle Mangement**

Designing products and leading product-based teams is one thing. A next challenge is managing complexity, which might increase as systems and codebases evolve.

Solutions include:

- Move from product-based teams to functional teams (or back).
- Scope down applications, outsource non-core activities.



**Innovation**

The main constraints are:

- Capital. Expected rate of return of an investment should exceed the interest rate (weighed by risk).
- Human capital. E.g. organization size.



Similar to markets, processes may have to be adjusted constantly. Do have regular conversations about the tooling and way of working. Don't rely on just metrics.



**Timeline**



![plot-expected-completion-time](img/plot-expected-completion-time.png)

![plot-estimated-num-features](img/plot-estimated-num-features.png)



## Planning

> Strive for continuous planning rather than up-front planning.



**Template**

1. Refine the product portfolio and a range of desired outcomes.
2. Choose a single North Star Goal and find metrics to track the progress towards it.
3. Decide on [initiatives](https://www.atlassian.com/agile/project-management/epics-stories-themes) that are abstract and *replaceable*. 

Based on this preparation, a roadmap can be setup. Then, projects can be defined, based on this roadmap. Ideally these project will only be refined *just in time* (JIT).



### JIT Planning

**Prioritization of future work**
Two different methods to plan work:

- Sprints of 1-4 weeks. See [scrum-guide.md](scrum-guide.md). The team commits to a single short-term goal and comes up with a plan to reach it. This commitment is motivational  rather than an obligatory: left-over tasks should be seen as a possibility of improvement rather than a failure. In cross-functional teams the diversity of the work in the sprint may be taken into account.
- No sprints, but instead use a continuously updated product backlog. Whenever a task is finished the tasks that is at the top of the backlog can be picked up. This requires a limit on the amount of work in progress. The team has more freedom and should have a high level of discipline.

**Prioritization of work in progress**
Maximize flow and minimize inventory (i.e. unfinished tasks, unmerged code). Prefer finishing tasks over starting new tasks. Address blocked task immediately instead of avoiding them. Find an optimal number of tasks to work on at the same time (within a team).

**Human resource management**
Instead of unpredictable waterfall stages,  _just_ do DevOps. Maintain a stable team-size by default and change it when the product demands it.



### Backlog

Also see [requirements-engineering](requirements-engineering.md).

The product backlog is a list of future work. Ideally it is prioritized. Each item is usually treated as a small project. Higher priority items can be fully formalized, while the rest of the items can be rough drafts. This low-priority section of the backlog can be treated as an "option pool".

Items can be grouped together in two ways:

- By goal. E.g. a sequence of tasks with a single purpose.
- By type. E.g. individual, independent tasks that happen to be similar. E.g. improving `adaptability, user-experience, efficiency, security`. 



**Administration**

> Work needs to be defined before it can be delegated.

Let the *product backlog* be defined as an ordered list of items that represent work that can be done in the future. Planned work can be administrated in the following ways.

- Explicit: on the backlog.
	- Rough ideas, goals, outcomes, results.
	- Small, fully refined items (stories) that can be finished within a few weeks.
	- Minor tasks that are no more than a day of work.
- Implicit: not on the backlog.
  - Alerts on a public dashboard that require attention.
  - In documentation (readme, specification, or external documentation).
    - Features that are currently supported, but that can be removed once they demand disappears.
    - Limitations of current design or implementation.
    - Possibilities of current approach / next steps.
    - Known risks.
  - Comments in source code (e.g. `TODO, SMELL`).
  - Hidden in private (mental) notes. E.g. questions send over email.

Within a team it is unavoidable that there are "private" ideas that are not though out. Ideally they would be brought up whenever the idea is ready to be shared and (part of) the team has capacity to discuss it.



## Patterns & Anti-patterns

[Agile Product Ownership](https://www.youtube.com/watch?v=502ILHjX9EE) - overview by Henrik Kniberg



**Customer chasing development**
Optimize on satisfying a single customer, instead of a market.

**Feature Factory**
Bias for releasing features, rather than solving customer problems. See [software-engineering](software-engineering.md]).

**Invisible work**
Single-point-of-failure. No handover in case of problems.

**Pet Projects**
Build something in secret to avoid the administrative or collaborative overhead.

**Promotion driven development**
Bias for optics & complexity. Build interesting stuff tools of useful tools.

**Shadow Backlog**
Typically non-prioritized and not discussed openly.

**Zombie product**
A product that is kept alive for political or personal reasons rather than market demand.



**Bottlenecks**

- What is holding you back?
- What patterns do you see developing?
- Where would you focus more/less on?



### Possible Processes from Idea to Implementation

From objective to discovery to delivery. Note that these phases could happen in parallel.

Formal steps

1. Initial idea.
2. Let it grow. Re-think it or share it with other people.
3. Prioritize it.
4. Build it. This requires development capacity.
5. Release it. This requires stakeholder and/or customer management.



**Implementation agnostic idea**

1. Narrative: `I wish my app would do X`
2. Short preparation `Is this technically feasible?`, `Can this be split up?`
3. Prioritization, then specification, then re-evaluation.
4. Implementation, then (gradual) release



**Low-hanging fruit / technical  possibility**

1. Technical possibility: `We could connect X to Y`
2. Brain-storm of implications and possibilities: `What are the advantages for the user?`
3. Prioritization
4. Implementation, then (gradual) release.



**Risk-based**

1. Signal of a risk.
2. Analysis of exposure and possible counter-strategies.
3. Prioritization of chosen strategy.
4. ...

