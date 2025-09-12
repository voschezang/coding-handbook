# Planning

This document discusses methods for planning. It assumes a pre-defined given a set of goals and a [strategy](../management/alignment-strategy.md).

[toc]

## Overview

> Strive for continuous planning rather than up-front planning.

**Tools**

A few common tools are:

- A product backlog. Ideas that will be worked on in the future.
- A [Kanban](https://en.wikipedia.org/wiki/Kanban_board) board. A dashboard that visualizes what is happening at the moment.

**Template**

From [goals and strategy](../management/alignment-strategy.md).

Alignment.

1. Refine the product portfolio and define a range of desired outcomes.
2. Communicate this and align the organization or team.

Leadership and motivation.

1. Choose a single North Star Goal that is consistent.
2. Choose an objective to focus on and find metrics (key results) to track the progress towards it.
3. Decide on [initiatives](https://www.atlassian.com/agile/project-management/epics-stories-themes) that are abstract and *replaceable*.

## JIT Planning

Suppose the main constraint in a team is capacity. Then there is a need to focus on the most important tasks. This can be done by either:

- Structured: Periodic planning sessions where work is selected and planned. E.g. week sprints in [Scrum](../collaboration/scrum-guide.md).
- Ad-hoc: A WIP-limited way of working. Whenever a task is finished a new task is selected.

**Prioritization of work in progress**
Maximize flow and minimize inventory (i.e. unfinished tasks, unmerged code). Prefer finishing tasks over starting new tasks. Address blocked task immediately instead of avoiding them. Find an optimal number of tasks to work on at the same time (within a team).

**Human resource management**
Instead of unpredictable waterfall stages,  *just* do DevOps. Maintain a stable team-size by default and change it when the product demands it.

## Backlog

A backlog is a list of future work and past ideas. It can range from *wish-list* to a *commitment*. It functions as:

- A scheduling mechanism.
- A prioritation device.
- An inventory of technical debt and risks.
- A list of commitments.

Also see [requirements-engineering](../requirements-engineering.md).

The items on the backlog are ordered by e.g. value or priority. Each item can be treated as a small project. [JIT planning](https://en.wikipedia.org/wiki/Lean_manufacturing) can be used to minimize over-production (of planning). This means that higher priority items can be fully formalized, while the rest of the items can be rough drafts.

Items can be grouped together in several ways:

- By goal. E.g. a sequence of tasks with a single purpose.
- By theme. E.g. individual, independent tasks that happen to be similar. E.g. improving `adaptability, user-experience, efficiency, security`.

**Administration**

> Work needs to be defined before it can be delegated.

Let the *product backlog* be defined as an ordered list of items that represent work that can be done in the future. Planned work can be administrated in the following ways.

- Explicit: on the backlog.
  - Rough ideas, goals, outcomes, results.
  - Small, fully refined items (stories) that can be finished within a few weeks.
  - Minor tasks that are no more than a day of work.
- Implicit: not on the backlog.
  - In other systems.
  - Alerts on a public dashboard that require attention.
  - In documentation (readme, specification, or external documentation).
    - Features that are currently supported, but that can be removed once they demand disappears.
    - Limitations of current design or implementation.
    - Possibilities of current approach / next steps.
    - Known risks.
  - Comments in source code (e.g. `TODO, SMELL`).
  - Hidden in private (mental) notes. E.g. questions send over email.

Within a team it is unavoidable that there are "private" ideas that are not though out. Ideally they would be brought up whenever the idea is ready to be shared and (part of) the team has capacity to discuss it.

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

**Types of stories**

In general there are two types of stories, both of which add value.

- *User* stories. These are directly visible to end-users or stakeholders.
- *Tech* stories. These are important, but their value is mostly visible internally. E.g. risk mitigation.

## Anti-patterns

**Invisible work**
Single-point-of-failure. No handover in case of problems.

**Shadow Backlog**
Typically non-prioritized and not discussed openly.
