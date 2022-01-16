# Scrum

This document is compatible with the  [Scrum guide](https://scrumguides.org/scrum-guide.html) (2020). At first sight, the original text may seem unnecessarily strict and even dogmatic. Although it contains strict rules, it is intended as a guideline and it should be interpreted in the right context. Unfortunately, the deeper meaning of the authors cannot easily be written down in [natural language](https://en.wikipedia.org/wiki/Natural_language). A typical point of discussion is whether Scrum is applied *correctly*, but it would be more useful to focus on how Scrum can be used most effectively.

The guide does not specify how to apply Scrum in a specific domain. If you want to adapt Scrum it is advised to make use of complementary resources. For example by hiring Scrum trainers to establish a two-way conversation.

[toc]

## High-Level Overview
Scrum is designed for  small teams that manages a single product in a [complex environment](https://en.wikipedia.org/wiki/Cynefin_framework). It is by design generic and under-specified. For it excludes how to develop product portfolios, how to define a target market, how to do UX or how to manage employees. Scrums generic approach allows it to be adapted to a specific domain and organization. The main caveat is that it does require a major [cultural](https://en.wikipedia.org/wiki/Organizational_culture) shift, namely a product mindset.

### Values
Scrum values people over processes. It advocates for the following values: `commitment, focus, openness, respect, courage`. Teams should discover themselves how they can apply these values in practice, in their organization.

> Inspection is useless if you don't want to change.

Scrum is founded on empiricism and lean thinking.

1. Transparency: continuously make observations and collect data.
2. Inspection: periodically analyze the current state in order to detect and predict possible (undesirable) consequences.
3. Adaption: when a process deviates from acceptable bounds then it must be adjusted as soon as possible. This requires empowerment of the team and its members.

Naturally, Scrum is opposed to practices of hiding problems (from managers). E.g. polishing statistics out of fear or reprisal.

**Agile**
It is a framework that helps teams to be [agile](https://en.wikipedia.org/wiki/Agile_software_development); to be able to inspect and adapt. It advocates for iteration as the main method to manage uncertainty, change and risk. This contrasts with other methods that rely on [functional phases](https://en.wikipedia.org/wiki/Waterfall_model) and tightening of requirements. A major reason for this is that this would just constrains the solution, without addressing the underlying problem.

**Product Mindset**
Scrum revolves around products rather of projects. See [this document](product-management.md#Product and Projects). It prioritizes the creation and delivery of value instead of time and cost. In this spirit, success is defined as:

- Frequent delivery of value to customers.
- The ability to adapt to changes. E.g. in markets, technology, customer preference.
- Ownership of the team.

**Anti-patterns**

- Managers that spend their time firefighting.

### Sprints

Sprints are short projects with a fixed length and a goal (outcome). Scrum specifies a few sprint-specific events:

1. Sprint Planning: define a single Sprint Goal and a plan to achieve it.
2. Sprint Review: an interactive session to share progress with stakeholders and get feedback from them.
3. Sprint Retrospective: plan ways to increasing quality and effectiveness.

In addition, there are a few other activities

- The Daily Scrum
- Refinement work.




## Roles

A scrum team consists of a Product Owner (PO), a Scrum Master (SM) and one or more development teams. The scrum team usually refers to a specific development team and the PO and SM.

The PO is accountable for the following items, but can delegate them if desired:

- Developing and communicating the product goal and strategy. 
    - Prioritizing *new* features and deciding which *existing* features to keep.
    - Choosing the target market.

- Mediation between stakeholders, customers and the development teams.



The Scrum Master (SM) role includes:

- Removing impediments; manage dependencies.
- Educating the organization on Scrum.
- (Optional) Coaching of team members.

It is [servant leader](https://en.wikipedia.org/wiki/Servant_leadership), rather than a boss, chairman, scribe, secretary or police agent.



The rest of the development teams does not have a hierarchy and are instead self-organizing. They should hold each other accountable (as a team) rather than by an external party.

They deliver periodic increments of work, which can be released 



The Scrum teams consists of the SM and Development team. It excludes stakeholders. The Development team includes developers and the PO.



**Anti-patterns**
Micromanagement, PO without authority, too many dependencies.

## Events

**Sprint**
Sprints can be independent from the release cycle; in the ideal case releases happen multiple times per week. The focus of a sprint should be to reach the Sprint goal rather than following the initial planning; it may not be necessary to finish all work in the Sprint Backlog. If the sprint goal becomes obsolete then the sprint can be ended prematurely. New sprints start automatically after the previous sprint has ended. 

The time-limit of a sprint is fixed. Any unfinished work may be moved over the the next sprint. If the sprint goal is not reached then the team should take it as an opportunity to learn and choose a new sprint goal in the next sprint. Hence it is not permitted to increase the length of a sprint. In addition,  reducing quality for the sake of reaching a deadline is a no-go.

**Sprint Events**
Sprint events are opportunities to inspect and adapt. They are all timeboxed. Usually they don't take up the capacity, especially not for shorter sprints.

| Event                | Inspection                         | Adaption                                       | Who Attends                 | Time-box (for 1 Month) |
| -------------------- | ---------------------------------- | ---------------------------------------------- | --------------------------- | ---------------------- |
| Sprint Planning      | Product Backlog                    | Sprint Goal, Sprint Backlog, Planning/Forecast | Scrum Team, invited experts | 8 hours                |
| Sprint Review        | Increment, Sprint, Product Backlog | Product Backlog                                | Scrum Team, Stakeholders    | 4 hours                |
| Sprint Retrospective | Sprint                             | Improvements                                   | Scrum Team                  | 3 hours                |

The Daily Scrum is independent of the sprint length.

| Event       | Inspection                   | Adaption       | Who Attends      | Time-box |
| ----------- | ---------------------------- | -------------- | ---------------- | -------- |
| Daily Scrum | Progress towards Sprint Goal | Sprint Backlog | Development Team | 15 min.  |



**Daily Scrum** 
This event that occurs daily, at the same place and time. It is exclusive to developers, to incentivize ownership. If a PO, SM or manager is present anyway, they should not facilitate the session.



**Sprint Planning**
A sprint starts with a planning session where the Why, What and How of the current sprint are discussed. Note that these points impact each other, so it may be necessary to go back and forth between them.

- Why is this sprint valuable? -> Sprint Goal
- What can be done this sprint. -> Sprint Backlog
- How will this be done? -> Planning
    - E.g. split backlog items up into manageable or predictable tasks.
    - Note that any forecast should be given under clear conditions. E.g. with the condition that the capacity will be stable and that no unforeseen events pop up.
        - Use confidence intervals?




**Sprint Review**
The team informs stakeholders about their progress. A moment for stakeholders and other parties to give feedback. This is not a validation stage.

- Note that stakeholders usually know the problem space better than members of the scrum team. Hence their feedback is vital.
- The content of the review should not present features that are still in progress, but it can discuss the progress towards them (e.g. challenges).



## Artifacts

Scrum does not prescribe [user-stories](https://www.atlassian.com/agile/project-management/user-stories) or [epics](https://www.atlassian.com/agile/project-management/epics-stories-themes), but instead uses the generic term Product Backlog Item (PBI). The flow ` idea > WIP >  delivery > release` is as follows:

1. Product Backlog Item. The size and complexity can vary, but higher priority items should be more specific, and preferably smaller. Items should not be split up into multiple stages (e.g. `develop, test`).
2. *Refined* Product Backlog Item, which is clearly defined and can be explained to stakeholders. Refining should be done just-in-time rather than months in advance, to prevent waste. External dependencies should be minimized (or addressed). The Sprint Backlog contains a plan how to deliver each item.
3. Increment; a piece of functionality that complies with the Definition of Done (DoD). It should be a usable and may combine multiple PBIs.



Some common patterns for PBIs:

- `ABC ABC ABC`: release frequently, but without focus.
- `AAA BBB CCC`: release less frequently, but with focus.
- `abc abc ABC`: release after third sprint (anti-pattern).



### Commitments

| Artifact                               | Commitment         |
| -------------------------------------- | ------------------ |
| Product Backlog (ordered list of PBIs) | Product Goal       |
| Sprint Backlog (selection of backlog)  | Sprint Goal        |
| Increment (finished work)              | Definition of Done |




**Product Goal**
If the Product Goal is achieved or obsolete then a new goal is chosen.

**Sprint Goal**

As mentioned, reaching the sprint goal has precedence over the sprint backlog. The development team is solely responsible for the Sprint Backlog, and can change it as they see fit.



The **Definition of Done** (DoD) is specific to an organization and a team. It describes quality standards and usually includes:

- ˙Integration tests

The DoD is complemented by Acceptance Criteria of backlog items.

Ideally, compliance with internal or external regulation is ensured to automated pipelines rather than manual verification.

Features and changes must adhere to the DoD and even then the PO should decide whether to release them.



### Hierarchy

Product Portfolio: a set of products.

For each product: Product Vision (Why) > Product Strategy (How) > Product Goal (Why) > Product Roadmap (How) > Sprint Goal.



- Why: Corporate Vision
    - What: Product Portfolio
    - How: Corporate Strategy



- Why: Product Vision
    - How: Product Strategy
- Why: Product Goal
    - How: Product Roadmap
- Why: Sprint Goal.
    - What: Sprint Backlog
    - Who: Sprint plan



