# Product Management

Also see [management principles](management-principles.md)  [goals](goals-planning-strategy.md).

[toc]

> Profit is an outcome and not a purpose. Value first.

> Don't sell, tell a story instead.



**Types of Products**

- Traditional Product: a static object. Must be right the first time.
- "Software" Product: can be updated (patched) after the first release.
- Service: completely continuous. Regularly updated to market conditions.



**Types of Customers and Stakeholders**

- The product-owner or project-manager
- The business (the rest of the organization)

- The users of a platform (e.g. sellers on ebay)
- The end-users (e.g. buyers on ebay)



**Market**

- Target market: optimize product for this market
- Boundary: additional sales, but don't optimize product for this markter
- Excluded from target



**Lifecycle Mangement**

Designing products and leading product-based teams is one thing. A next challenge is managing complexity, which might increase as systems and codebases evolve.

Solutions include:

- Move from product-based teams to functional teams (or back).
- Scope down applications, outsource non-core activities.



**Innovation**

The main constraints are:

- Capital. Expected rate of return of an investment should exceed the interest rate (weighed by risk).
- Human capital. E.g. organization size.



**Breakdown of Work into Tasks**

Work and features can be divided into an abstract, long-term strategy and specific, short-term tasks.

Have a north start goal, along with a good metric to track incremental progress. Summarize them in one-pages, but do use appendices and link to additional sources. 
Based on this goal, define sub-goals or strategies that can be reached within years (or months). 

This can be [added](https://medium.com/hackernoon/the-random-ticket-game-693f6a6c7ea4) to the standard user-story template:

```
As a [persona], I want to do [this], because [benefit], because it supports [this sub-goal]
```





### Types of Tasks

The generic concepts PoC and MVP can be applied to tasks and features. In general, smaller task are less unpredictable and have a less rework associated with them. On the other hand, lengthy tasks [incentivize](https://medium.com/hackernoon/wip-it-real-good-66aa710178fd) the use backchannels, local agenda's and lack of overall focus.

- **Proof of concept** ([PoC](https://en.wikipedia.org/wiki/Proof_of_concept))
    Build an experimental application and learn on the way. The goal is not to develop finished end-product but rather to demonstrate feasibility and/or learn what a production-like application would entail (and gain a head-start).

- **Minimum Viable Product** ([MVP](https://en.wikipedia.org/wiki/Minimum_viable_product)): 
    Deploy a minimal feature ASAP s.t. you can collect early feedback and improve it iteratively. Maximize the amount of learning (e.g. from users/customers) with the least amount of effort. It emphasizes the value of customer-feedback is 
- **Minimum Lovable Product** (MLP): 
    Work towards a release that will overwhelm customers/end-users. In case of infrastructure this could mean an automated and sufficiently secured and monitored system.



### Content of tasks

Subtasks can be explained in a single sentence, but (large) tasks can be defined more thoroughly.

The questions that should be answered are as follows (ordered by importance). This is based on [Kanban](https://en.wikipedia.org/wiki/Kanban) and [PDCA](https://en.wikipedia.org/wiki/PDCA).

Approach

- What problem does this task tackle? To what higher-level goal does this task relate?
- What are the current and target conditions?
- What are the risks associated with this approach?

Steps

- What are the sub-tasks that are involved?
- What is the minimal scope of the task?
- What are the next steps?

Before closing a task an appropriate review should be done to validate whether its purpose has been fulfilled.



### Planning

**Prioritization of future work**
Two different methods to plan work:

- Sprints of 1-4 weeks. The team commits to a certain set of tasks. This commitment is used as a motivational goal rather than an obligation: left-over tasks should be seen as an indication rather than improvement rather than a failure. In non-specialist teams the diversity of the work in the sprint should be taken into account.
- No sprints, but instead use a continuously updated backlog. Whenever a task is finished the tasks that is at the top of the backlog can be picked up. This requires a limit on the amount of work in progress. The team has more freedom and should have a high level of discipline.

**Prioritization of work in progress**
Maximize flow and minimize inventory (i.e. blocked tasks). This can be achieved by prioritizing tasks that have already been started over new tasks. Address blocked task immediately instead of avoiding them. Find an optimal number of tasks to work on at the same time (in a team).

**Resource management**

Instead of unpredictable waterfall stages,  _just_ do DevOps. Maintain a stable team-size by default and change it when the product demands it.



#### Backlog

Administration of work that should be done in the future.
- Explicit (on the backlog)
	- Fully refined stories.
	- Minor stories: trivial but more than a day of work.
	- Tasks: a basic story with the minimal number of story points.
- Implicit (not on the backlog)
	- Comments in source code (e.g. `TODO, SMELL`)
	- In documentation (readme, spec, or external documentation)
		- limitations of current design or implementation
		- possibilities of current approach / next steps

The advantage of the second category is that no major upfront design is necessary.



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



**Story Points Alternatives**

- Units: scope all tasks down until they have a comparable, small and manageable size. Large tasks are a challenge.
- Days per engineer: more specific than story-points but there is a risk of simplification (i.e. the comparison with an *average* engineer)



**Types of Work**

- Saga/Epic/Story/Task. From abstract and long-term to concrete and short-term. These are thought out in detail.
- One-pointer. Trivial work that should be done sooner rather than later, but without any direct urgency.
- Spike. A time-boxed experiment with the purpose of learning.





## Patterns & Anti-patterns

[Agile Product Ownership](https://www.youtube.com/watch?v=502ILHjX9EE) - overview by Henrik Kniberg



**Promotion driven development**
Bias for optics.

**Customer chasing development**
Optimize on satisfying a single customer, instead of a market.




**Bottlenecks**

- What is holding you back?
- What patterns do you see developing?
- Where would you focus more/less on?
