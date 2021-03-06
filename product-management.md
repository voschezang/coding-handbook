# Product Management

This is more about *projects* than a *product*, but it borrows some useful terminology from product management. See also [goals and strategy](goals-planning-strategy.md) and  [management principles](management-principles.md).

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

**Project sizing**
Projects can usually be split up into smaller parts that are delivered immediately - to customers. This may provide revenue *sooner* and it allows subsequent iterations to incorporate feedback from customers. This may reduce the amount of unused features. This is an alternative to delivering the whole project in one go - and never looking back. This iterative way of working is considered to be [*agile*](scrum-guide.md).

![choosing-agile](img/choosing-agile.png)

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



## Project Management

Typical requirements include time- and cost-bounds, and a *scope*. In theory, only two of these can be guaranteed.

This scope can be defined in different levels:

- **Input**-based. This bears the least uncertainty, but the output itself may be unpredictable.

- **Output**-based. This leaves some freedom on the implementation side.  If risk materialize, either time or cost would have to be let go.

- **Outcome**-based. This method is more subjective. It focusses on building the right thing, rather than something.



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



## Up-front Planning

> Strive for continuous planning rather than up-front planning.

Planning can be split up into [two phases](goals-planning-strategy.md). After more information become available this cycle can be repeated.

1. Refine the product portfolio and a range of desired outcomes.
2. Choose a North Star Goal, metrics and initiatives.

The latter would would result in:

- A North Star Goal, with a metric to track progress.
    - Consider multiple possible scenarios/futures, not just the ideal case.
- Diversified sub-goals ([initiatives](https://www.atlassian.com/agile/project-management/epics-stories-themes)) that are abstract and can easily be adjusted.
    - Note that these are not just categories of stories (e.g. "improve security").

- Stories or Tasks. The titles can be denoted in advance, but the details should not be added until the point where they are going to be picked up to be worked in the short-term (based on the number of dependencies). I.e. only add details to the highest-priority stories.
    - In practice, some stories will contribute to multiple sub-goals. There isn't always  a one-size-fits-all solution, so be pragmatic about this. 


In general, MVP-based iterations are preferred. Their size is context-dependent.

Ideally, go to production as soon as possible. Use gradual releases (e.g. by demographic) and build-in the option to adapt if expectations are not met.



In general there are two types of stories, both of which add value.

- **User stories**. These are directly visible to end-users or stakeholders.
- **Tech stories**. These are important, but their value is mostly visible internally. E.g. risk mitigation.



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



### Types of Tasks

The generic concepts PoC and MVP can be applied to tasks and features. In general, smaller task are less unpredictable and have a less rework associated with them. On the other hand, lengthy tasks [incentivize](https://medium.com/hackernoon/wip-it-real-good-66aa710178fd) the use backchannels, local agenda's and contribute to a lack of overall focus.

- **Proof of concept** ([PoC](https://en.wikipedia.org/wiki/Proof_of_concept))
    Build an experimental application and learn on the way. The goal is not to develop finished end-product but rather to demonstrate feasibility and/or learn what a production-like application would entail (and gain a head-start).

- **Minimum Viable Product** ([MVP](https://en.wikipedia.org/wiki/Minimum_viable_product)): 
    Deploy a minimal feature ASAP s.t. you can collect early feedback and improve it iteratively. Maximize the amount of learning (e.g. from users/customers) with the least amount of effort. It emphasizes the value of customer-feedback is 
- **Minimum Lovable Product** (MLP): 
    Work towards a release that will overwhelm customers/end-users. In case of infrastructure this could mean an automated and sufficiently secured and monitored system.



**Types of features**
Note that features often have multiple roles, and can be sold as feature anyway.

|                | User-invisible | User-visible                                                 |
| -------------- | -------------- | ------------------------------------------------------------ |
| Positive Value | Feature        | Architecture, non-functional requirements, process improvements |
| Negative Value | Defect         | Technical debt                                               |



## JIT Planning

**Prioritization of future work**
Two different methods to plan work:

- Sprints of 1-4 weeks. See [scrum-guide.md](scrum-guide.md). The team commits to a single short-term goal and comes up with a plan to reach it. This commitment is motivational  rather than an obligatory: left-over tasks should be seen as a possibility of improvement rather than a failure. In cross-functional teams the diversity of the work in the sprint may be taken into account.
- No sprints, but instead use a continuously updated product backlog. Whenever a task is finished the tasks that is at the top of the backlog can be picked up. This requires a limit on the amount of work in progress. The team has more freedom and should have a high level of discipline.

**Prioritization of work in progress**
Maximize flow and minimize inventory (i.e. unfinished tasks, unmerged code). Prefer finishing tasks over starting new tasks. Address blocked task immediately instead of avoiding them. Find an optimal number of tasks to work on at the same time (within a team).

**Human resource management**
Instead of unpredictable waterfall stages,  _just_ do DevOps. Maintain a stable team-size by default and change it when the product demands it.



### Backlog

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



#### Story Points

The [many roles](https://twitter.com/johncutlefish/status/1425849975108358147/photo/1) of story-points. Remember; story-points are not real.

- Incentive to write smaller stories, s.t. they more easily fit in the next sprint.
- Make estimations less subjective, e.g. by combining multiple (independent) estimations.
    - Use the abstraction "complexity" to make estimations less personal.
    - Stimulate discussion about the story itself and the number of points assigned to it. Talk about complexity.
- Estimate or report on team-capacity and/or productivity per sprint.
    - Show that the team works hard and consistently. Identify struggling teams.
- Shared value between the team and higher management. Improve reporting towards management.
    - Create burndown charts.
- Make (reasonable) commitments to motivate team members. Improve prioritization.



**Alternatives**

- Units: scope all tasks down until they have a comparable, small and manageable size. Large tasks are a challenge.
- Days per engineer: more specific than story-points but there is a risk of simplification (i.e. the comparison with an *average* engineer)



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
