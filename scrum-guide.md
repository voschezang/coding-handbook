# Scrum

This document is compatible with the  [Scrum guide](https://scrumguides.org/scrum-guide.html) (2020). At first sight, the original text may seem unnecessarily strict and even dogmatic. Although it contains strict rules, it is intended as a guideline and it should be interpreted in the right context. Unfortunately, the deeper meaning of the authors cannot easily be written down in [natural language](https://en.wikipedia.org/wiki/Natural_language). A typical point of discussion is whether Scrum is applied *correctly*, but it is more useful to focus on how Scrum can be used most effectively.

The guide does not specify how to apply Scrum in a specific domain. If you want to adapt Scrum it is advised to make use of complementary resources. For example by hiring Scrum trainers to establish a two-way conversation.

[toc]

## High-Level Overview

Scrum is designed for  small teams that manages a single product in a [complex environment](https://en.wikipedia.org/wiki/Cynefin_framework). The main reasons to use it are (1) to  improve quality through reflection and adaption and (2) to reduce risk by delivering value in short increments.

### What

Scrum is by design generic and under-specified. For example, it excludes how to develop product portfolios, how to define a target market, how to program, how to improve UX or how to manage employees. Scrums generic approach allows it to be adapted to a specific domain and organization. The main caveat is that it does require a major [cultural](https://en.wikipedia.org/wiki/Organizational_culture) shift, namely a *product mindset*.

Scrum is about:

- Agility: inspect embrace change and an uncertain environment.
- Build & deliver incremental value to customers.
- Cross-functional collaboration.
- Discovery-driven development over requirements-driven development.
- Experimentation and learning.

Scrum includes of:

- 5 core [values](#Values):  `commitment, focus, openness, respect, courage`
- The [Sprint](#Sprint) and 4 formal Sprint [events](#Sprint Events): `Sprint Planning, Sprint Review, Sprint Retrospective, Daily Scrum`
- 3 [roles](#Roles): `Product Owner, Scrum Master, Developers `
- 3 [artifacts](#Artifacts), each with a commitment: `Product Backlog (Goal), Sprint Backlog (Goal), Increment (DoD)` .

These are hard, *immutable* requirements. This makes scrum revolutionary, rather than evolutionary. It isn't meant to be applied gradually (e.g. [kanban](learning.md#Kanban)). Instead, it requires a radical change in many traditional ways of working.

### How

> Inspection is useless if you don't want to change.

Scrum values empiricism and lean thinking.

1. Transparency: continuously make observations and collect data.
2. Inspection: periodically analyze the current state in order to detect and predict possible (undesirable) consequences.
3. Adaption: when a process deviates from acceptable bounds then it must be adjusted as soon as possible. This requires empowerment of the team and its members.

A few concrete values:

- Quality first. Do not reduce quality for the sake of reaching a deadline. The only exception to deviate from standard processes are when there is a production-incident. 
- Self-managing teams. Don't solve problems for the team but instead empower the team to find a solution.
- Scrum is opposed to practices of hiding problems (from managers). E.g. polishing statistics out of fear or reprisal.

**Agile**
It is a framework that helps teams to be [agile](https://en.wikipedia.org/wiki/Agile_software_development); to be able to inspect and adapt. It advocates for iteration as the main method to manage uncertainty, change and risk. This contrasts with other methods that rely on [functional phases](https://en.wikipedia.org/wiki/Waterfall_model) and tightening of requirements. A major reason for this is that this would just constrains the solution, without addressing the underlying problem.

**Product Mindset**
Scrum revolves around products rather of projects. See [this document](product-management.md#Product and Projects). It prioritizes the creation and delivery of value instead of time and cost. In this spirit, success is defined as:

- Frequent delivery of value to customers.
- The ability to adapt to changes. E.g. in markets, technology, customer preference.
- Ownership of the team. Developers should have enough autonomy to self-organize and adapt.

**Anti-patterns**
Mechanical scrum (without Scrum values).

#### Sprints

Sprints are short projects with a fixed length and a goal (outcome). Scrum specifies a few sprint-specific events:

1. Sprint Planning: define a single Sprint Goal and a plan to achieve it.
2. Sprint Review: an interactive session to share progress with stakeholders and get feedback from them.
3. Sprint Retrospective: plan ways to increasing quality and effectiveness.

In addition, there are a few other activities

- The Daily Scrum
- Refinement work. This doesn't have to be a formal event, but it should be done regularly.

Note that delivering software can be decoupled from releasing software. Even is delivered software is not released immediately, the periodic delivery incentivizes feedback and it increases transparency, and control.



## Values

Scrum values people over processes. It advocates for the following values:

- **Commitment**. Set realistic goals and try to achieve them as a team.
- **Focus** on the current sprint and work together as a team.
- **Openness** towards stakeholders and towards each other. Transparency is vital for learning.
- **Respect** each other.
- **Courage** to work on tough problems rather than blindly following traditional practices.

Teams should discover themselves how they can apply these values in practice, in their organization.



## Roles

A scrum team consists of a Product Owner (PO), a Scrum Master (SM) and one or more development teams. The scrum team usually refers to a specific development team and the PO and SM. More about team structure [here](organization-structure.md).

Scrum does not replace project managers. Management is considered external to scrum and should support (empower) the Product Owner and Scrum Master.

**Anti-patterns**
Managers that spend their time firefighting. Micromanagement, PO without authority, too many dependencies. [Alienated](https://en.wikipedia.org/wiki/Marx%27s_theory_of_alienation) developers that are unaware of the purpose of their work. A group of individuals rather than an aligned team.

### Product Owner

The PO is accountable for the following items, but can delegate them if desired:

- Developing and communicating the product goal and strategy. 
    - Prioritizing *new* features and deciding which *existing* features to keep.
    - Choosing the target market.

- Mediation between stakeholders, customers and the development teams.

### Scrum Master

A Scrum Master (SM) is accountable for the Scrum Process and the effectiveness of the team. The SM manages people and processes, but from a distance. This allows the SM to be a more objective observer. The end-goal is for the rest of the team to take ownership. The style can vary from leading to facilitating. A few important activities are:

- Removing impediments. This may require escalation to the rest of the organization.
- Educating the organization on Scrum.
- Coaching of team members.

The activities of a SM depend on both the organization and the team. As Scrum gets adapted in an organization, the domain where the SM may evolve:

1. An understanding of Scrum in the team or organization
2. Scrum team forming
3. Development excellence
4. Adjacent processes
5. Organizational processes

As the team develops itself from towards mastery of Scrum, the role of the SM can change as well:

1. Teaching techniques
2. Embracing empiricism
3. Valuable outcomes
4. Values and principles
5. Invisibly present

Although the SM is the expert on the Scrum process, most decisions should be made by the team. The SM is a [servant leader](https://en.wikipedia.org/wiki/Servant_leadership), rather than a boss, chairman, scribe, secretary or police agent. Based on the environment, the role can manifest itself in several ways. A good SM chooses deliberately how to act.

- Leading, pushing
    - Teacher or mentor
    - Uphold Scrum
    - Take action. E.g. escalate a problem.
- Facilitating, showing, giving perspective
    - Facilitator or coach
    - Actively do nothing. Observe. E.g. let small problems reveal itself to the team.
    - Point north

### Developers

The rest of the **development teams** do not have a hierarchy and are instead self-organizing. They deliver periodic increments of work, which can be released if desirable. A PO or SM can also have a developer role. Developers should have enough autonomy to be able to take ownership of their work. They are accountable for:

- Creating and adjusting the plan for the current sprint.
- Instilling quality by adhering to the Definition of Done.
- Holding each other accountable.

The **Scrum teams** consists of the SM and Development team. It excludes stakeholders. The Development team includes developers and the PO. Scrum prescribes a team size of at most 10 members, unless there is a good reason to have a larger team.



## Events

### Sprint
Sprints can be independent from the release cycle; in the ideal case releases happen multiple times per week. The focus of a sprint should be to reach the Sprint goal rather than following the initial planning; it may not be necessary to finish all work in the Sprint Backlog. If the sprint goal becomes obsolete then the PO can end the sprint prematurely. New sprints start automatically after the previous sprint has ended. 

The duration of sprints is chosen based on busines risk and synchronization with other business events. The chosen duration is fixed, but a sprint can be cancelled if the Sprint Goal has become obsolete. If there is unfinished work left in a sprint then that  may be moved over the the next sprint. If the sprint goal is not reached then the team should take it as an opportunity to learn and choose a new sprint goal in the next sprint. Hence it is not permitted to increase the length of a sprint. In addition,  reducing quality for the sake of reaching a deadline is a no-go.

**Anti-pattern**
Too little or too much overlap between sprints

- Start-stop scrum; no continuity between sprints. 

- Red sprints; repeatedly having leftover work from each previous sprint.

E.g. repeatedly scoping out all unfinished work at the end of the sprint to make it seem like the sprint went perfect.

### Sprint Events
Sprint events are opportunities to inspect the current sprint and adapt accordingly. These events are all time-boxed, but usually they don't take up their full capacity, especially not for shorter sprints.

| Event                | What to inspect?                   | What to adapt?                                 | Who attends?                | Time-box (for 1 Month) |
| -------------------- | ---------------------------------- | ---------------------------------------------- | --------------------------- | ---------------------- |
| Sprint Planning      | Product Backlog                    | Sprint Goal, Sprint Backlog, Planning/Forecast | Scrum Team, invited experts | 8 hours                |
| Sprint Review        | Increment, Sprint, Product Backlog | Product Backlog                                | Scrum Team, Stakeholders    | 4 hours                |
| Sprint Retrospective | Sprint                             | Improvements, Product Backlog                  | Scrum Team                  | 3 hours                |

The Daily Scrum is independent of the sprint length.

| Event                 | Inspection                   | Adaption       | Who Attends      | Time-box |
| --------------------- | ---------------------------- | -------------- | ---------------- | -------- |
| Daily Scrum (Standup) | Progress towards Sprint Goal | Sprint Backlog | Development Team | 15 min.  |

**Daily Scrum**
This is a developer-centric event that occurs daily, at the same place and time for consistency and to reduce complexity. The format is free, but it should focus on the progress towards the sprint goal rather than on what team members have done. If a PO, SM or manager is present then they should not facilitate or steer the session.



**Sprint Planning**
A sprint starts with a planning session where the Why, What and How of the current sprint are discussed. Note that these points impact each other, so it may be necessary to go back and forth between these questions.

- Why is this sprint valuable? -> Sprint Goal
- What can be done this sprint. -> Sprint Backlog
- How will this be done? -> Planning
    - E.g. split backlog items up into manageable or predictable tasks.
    - Note that any forecast should be given under clear conditions. E.g. with the condition that the capacity will be stable and that no unforeseen events pop up.
        - Use confidence intervals?



**Sprint Review**
The team informs stakeholders about their progress. A moment for stakeholders and other parties to give feedback. 

- This is not a validation stage of past work but rather a moment to incorporate new information into the product backlog.
- The review should not be a sales pitch and neither should it give a demo of features that are not yet *done*. However, it can discuss progress or challenges.

- In general, stakeholders know the problem space better than members of the scrum team. Hence their feedback can be vital.

It can include:

- What happened in the Sprint itself.
- Delivered Increments and outcomes.
- Current business conditions.
- Product Backlog and progress towards Product goal.



**Sprint Retrospective**
Reflect on the last sprint with regards to individuals, interactions, processes and tools. Discuss what went well, what problems were encountered and how those problems could be solved. The [format](https://retromat.org/) the can be varied occasionally, but not too often.



## Artifacts

Scrum does not prescribe [user-stories](https://www.atlassian.com/agile/project-management/user-stories) or [epics](https://www.atlassian.com/agile/project-management/epics-stories-themes), but instead uses the generic term Product Backlog Item (PBI). The flow ` idea > WIP >  delivery > release` is as follows:

1. Product Backlog Item. The size and complexity can vary, but higher priority items should be more specific, and preferably smaller. Some teams like use a "definition of ready".
2. *Refined* Product Backlog Item, which is clearly defined and can be explained to stakeholders. Refining should be done just-in-time rather than months in advance, to prevent waste. External dependencies should be minimized (or addressed). 
3. Items on the Sprint Backlog. PBI's are decomposed into items that take at most one day.
4. Increment; a piece of functionality that complies with the Definition of Done (DoD). It should be a usable and may combine multiple PBIs. Increments should not be split up into multiple stages (e.g. `design, develop, test`).



Some common patterns for PBIs. Lowercase letters denote preparation and uppercase letters denote a release.

- `AAA BBB CCC`: release frequently and with focus.
- `ABC ABC ABC`: release frequently, but without focus.
- `aaA bbB ccC`: release less frequently, but with focus.
- `abc abc ABC`: stack up WIP and release them after the third sprint (anti-pattern).



The size or weight of PBIs is a proxy for the effort required to finish it. It can be expressed in e.g. FTE hours or complexity. If all PBIs have a comparable size then it becomes easier to predict when work is finished, even while taking into account uncertainty. In order to make accurate estimations a confidence interval based on historical data is vital.

### Commitments

| Artifact                               | Commitment         |
| -------------------------------------- | ------------------ |
| Product Backlog (ordered list of PBIs) | Product Goal       |
| Sprint Backlog (selection of backlog)  | Sprint Goal        |
| Increment (finished work)              | Definition of Done |



**Product Backlog**
A single source of truth of planned work. It is prioritized by value, as defined by the PO. In practice, the preferences of individuals can play a role as well. E.g. due to affinity, skill or even optics.

**Product Goal**
If the Product Goal is achieved or obsolete then a new goal is chosen.

**Sprint Backlog**
The Sprint Backlog is owned by the development team. If there is demand to change it then the development team can decide to adjust the it, as long as it doesn't endanger the sprint goal.

Note that the selection and structure of sprint backlog items influences how effective the development team can be. There is a tradeoff between high autonomy and high alignment. An example of the former would be focus on individual (personal) tasks, and an example of the latter would be focus on task with the highest priority, at the cost of context switching.

**Sprint Goal**
Having a single goal forces the team and stakeholders to accept the priority of features. It incentivizes stakeholders to align on what's the most important aspect. 

As mentioned, reaching the sprint goal has precedence over the sprint backlog. The development team is solely responsible for the Sprint Backlog, and can change it as they see fit. If they want to adjust the Sprint Goal or the planning then they can discuss or re-negotiate it with the PO.

Ideally the Sprint Goal would have been reached before the end of the sprint. In such case the team could start preparation for the next sprint, but they could also take this opportunity to invest time in longer-term goals, reflect or work on personal improvements.



 **Definition of Done**
The Definition of Done (DoD) describes when an Increment is *ready* to be released to customers. It is used to ensure quality. and transparency, by providing a shared understanding. It is created by the Scrum Team. If there is a organization-wide DoD then that one must be followed as a minimum. The Dod should be equal for teams that work on the same product, but it can be complemented by team-specific *development standards*.

In addition, the DoD is complemented by Acceptance Criteria of backlog items, which are more specific. 

Ideally, compliance with internal or external regulation would be ensured through automated pipelines rather than manual verification.

