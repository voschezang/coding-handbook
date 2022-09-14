# Goals & Strategy

[toc]

> Making plans is good, withholding from updating them isn't.

> Good strategy means saying no.



**Terminology**

Specific types of goals

| Term         | Meaning |
| ------------ | ------- |
| Mission      | Why     |
| Vision       | What    |
| Strategy     | How     |
| Roadmap      | When    |
| Segmentation | Who     |
| Positioning  | Where   |
| Tactic       | ...     |

Note that these can be chosen for an *organization* and for each *product* within that organization.



## Roadmap

> Great outcome > meeting initial requirements.

> A goal is nothing without a good system to reach it.

A roadmap is a prototype of a strategy, rather than a list of everything that will be done. Make it flexible. Design for failure.

> Separate goals from dreams

It is great to have a long-term vision, but [good](https://en.wikipedia.org/wiki/SMART_criteria) goals are a vital complement. In addition, idealistic outcomes are often difficult to measure and quantify. Hence (sub-)goals are used as a proxy.

An hierarchy of three layers:

**(1) High level / long term: North Star**

A few variants:

- North Star Goal: specific and measurable. A rough direction to go towards. Top of the goal/sub-goal hierarchy.
    - Ideally this metric is consistent with your definition of success.
    - Ideally this metric is clear to the whole organization, such that they can align.
- Objective, Outcome or narrative: what the ideal state would look like. A vision. This can be a condition that needs to be fulfilled.

Based on this high-level goal, you can start to trace back which steps are necessary to reach it. In addition, you can setup *inputs* or metrics to track progress.

**(3) Low-level / Short term: planning**

Use a rolling window. I.e. update the following list regularly/frequently. Reflect on results periodically and update them ad-hoc, on gaining new information.

1. Now: a handful of tasks that are currently worked on, and will be finished ASAP.
2. Next: 3 tasks that will be picked up next
3. Later: 1 task after that, and 1 task after that. However, if we learn more, then we might select one of these tasks instead.

Then find a way to align with the whole organization or team...

**(2) The messy middle**

Long-term goals are generally stable and short-term plans can be made continuously. Everything in between is inherently messy. The "middle" is based on the current worldview, but because it is specific it will become more and more obsolete as the environment changes. Hence it has to adjusted be from time to time.

A major strategy for this is diversification. Consider multiple initiatives that will help to reach your goal from different angles. Design these to be *replaceable*. Ensure that they can at least be adjusted over time. Note that this still allows focus on a single initiative at a time.

A common tool to address the complexity of this area are [OKRs](https://en.wikipedia.org/wiki/OKR). Do note that this works best as a *complement* to a long-term outcome.



### Living Roadmap

A roadmap becomes outdated over time due to:

- Internal changes. E.g. learning as part of the pre-planned progression.
- External changes. Changes in the environment.

Hence, use a format that is resilient to change. This can be done by combining high-level and low-level descriptions.

#### Template 1

A template for a one-pager roadmap. This can be complemented with external sources.

1. A mission or vision. A perfect outcome.
2. North star goal. A great outcome. The minimum investment you want to make. This takes in cost and time constraints.
3. Current state and target state.
4. A list of next target states. Avoid a strict ordering, but do suggest a preference based on the current circumstances.

In addition, it can be useful to include *anti-goals*, i.e. which activities are excluded. This makes trade-offs explicit, and forces the authors to investigate their choices.



<img src="img/roadmap.png" alt="roadmap" style="width:50%;" />



#### Template 2

List the desired outcomes over time, using an exponential timescale. E.g. a month, quarter, year and 4 years.



#### Meetings

Setting up dedicated ceremonies can help to ensure regular reflection, at the right timescale. E.g. in the form of meetings:

- Daily check-in meeting. Align and improve awareness. E.g. of work or people.
- Weekly tactical meeting. React to short-term issues.
- Monthly strategic meeting. Decide on long-term adjustments.
- Quarterly off-site review. Take an outside-view and reflect.



## Project Portfolio

Individually, projects can seem valuable. A more difficult challenge is maintaining a balanced portfolio of projects. A typical chicken-egg problem is that projects need to be prepared before they can be prioritized. Doing too much preparation increases WIP and thus reduces focus. This template attempts to avoid this by defining high level outcomes and excluding details.

This is especially useful w.r.t technical work that is not visible to end users. Although it is valuable, it can be easily be postponed without affecting promises to stakeholders.

### Template 1

Start with a number of categories or themes. E.g. security, incident management, operations efficiency). For each one, define the current state and the desired state. The desired state is not necessarily a *target*, but rather an <u>idealistic outcome</u>. 

This template focusses on the range of outcomes and excludes *how* to reach them. This avoids the overhead of up-front planning, and reduces the risk of plans becoming outdated.

The template:

``` markdown
# Theme A

Current State
> What is currently lacking. 

Desired State
> What outcome is envisioned.


# Theme B

Current State
> What is currently lacking. Link to Current design

Desired State
> What outcome is envisioned. Read more here.

...
```



### Template 2

This is again based on categories or themes, but this template emphasizes the option pool. The shape of the visualisation (when zoomed out) gives an indication of the amount of focus.

![option-pyramid](img/option-pyramid.png)



## Models for Goal Setting

Different ways to set goals

**Legend**

- A. Current state
- B. Next target state, which will help towards Y and Z.
- Y. Required objective for Z.
- Z. North star goal



<img src="img/setting-goals.png" alt="seq-par-chain" style="width:80%;" />




## Documentation

> Use documents to recall conversations rather than having them.

The goal is to externalize thinking. This helps to alignment the whole organization or team.

Summarize higher level in one-pages, but do use appendices (for details) and link to additional sources. See also [documentation](documentation.md).

**Assumptions & Facts**
For each goal, denote the assumptions and rationale. Be explicit in what's an assumption or uncertain.



### Tools

**Narrative**
Convey the feeling of an ideal state. E.g.*"1000 songs in your pocket"*
This is independent of the required input effort.

**Persona**
A model (or proxy) of the target market or audience. E.g. a typical user with a certain background.

**User Story**
What value a given feature would bring to a given *persona*. E.g.:

> As a `Persona` I want  `an action` because it will bring this `benefit` which helps to reach this `outcome`, based on the fact that `______`  and the assumption that `______`.

In order to be effective, a the scope should be limited to a few weeks.

**Epic**
A collection of user stories that can be finished in at most a handful of months.



## Goals

A goal should be accompanied with an *initiative* (input), *target* (output, result) and a *target condition* (objective, outcome).



The **goal** itself should be skewed towards the *Why* instead of the *What*. It should be an optimistic vision or mission.
- This includes a understanding of the relevant assumptions.
- Goals that are too high lead short term optimization (trying to survive instead of investing).
- Goal that are not high enough lead to a lack of focus.

**Initiative & Target**

Global optima are usually unknown in advance.

- Initially the target condition can be be a vague *challenge*. Missing details can be filled step by step, after reflection and experimentation. In fact, it is inevitable that you find new information when moving forward.
- Define the minimum amount of work that is required to reach an outcome and start there.

- Beware of changing the target condition to fit the current state.

**Metrics**

Use metrics as a tool to track incremental progress. Expectations for metrics should be ambitious but not impossible.

- Note that all metrics are flawed. They cannot be both generic and specific.
- Optimize targets and not [the measure](https://en.wikipedia.org/wiki/Goodhart%27s_law) (avoid [perverse incientives](https://en.wikipedia.org/wiki/Perverse_incentive)).

- Use different goals per timescale: `days, weeks, months, years, decades `. Relate shorter term goals to longer term goals. 

**Estimating**

Reasoning with probabilities and large numbers is harder than reasoning with small, discrete numbers

- `1 out of 8` is more intuitive than `12.5%`.
- Conglomerations are easier than continua and numeric values.

- Predict complexity of a tasks by the estimating the number of subtasks

Avoid personal bias. Instead of estimating your personal work (or your team), estimate what an other or similar person/team could achieve.

**Flow of Work**

The optimal size of batches, number of batching steps and the size of subtasks is context-dependent. Hence it should be optimized to current conditions, in concurrence with any target conditions.



**Choosing Goals**

Prioritization requires de-prioritization. This is inherently difficult. A few tools that can be used are:

- Select a single goal, that is absolutely necessary. E.g. address (or identify) the main constraint.

- Create a plot of the benefits as result of the effort required, for each possible goal.



Defining goals

- Bottom-up: First list features or desires, then define metrics.
- Top-down: Define a desired outcome, then define metrics to track progress towards that outcome, then list immediate actions. 
