# Management Principles

Inspired by [[1]][1]. See also on [goals and planning](goals-planning-strategy.md).

[toc]

## Overview

Three main types are:

- Product management.  More [here](product-management.md#Product and Projects).
- Project management
- Process & People management.



**Main Activities**

Management consists of two main activities:

1. Set *optimistic* goals, prioritize them and make a *realistic* planning/estimation.
    - Be great at setting expectations.
    - Adapt over time. Revisit past decisions.
    - Prioritization includes deciding what *not* to do.
2. Creating an environment where employees can reach those goals.

    - Employees should have agency and be incentivized to be pro-active. Allow them to question everything.
    - The organization should be a community, where people interact.

Hence management styles can be oriented towards (1) leadership or (2) facilitation. In addition there might be a focus on a specific function, for example a product or project. The work will vary greatly dependent on the type of organization and the composition of teams.

There is a tradeoff between adapting to the current team, and seeking out employees that accept a certain management style.





**Measure of Success**

Define a proper measure of success. Evaluate whether the assignment could be successful (outcome-based) without meeting the requirements. 

Typical components:

- Efficiency: of the system as a whole or individual components (e.g. resources).
- Quality: high quality and low variance.
- Agility: be able to adapt.



## Systems & Processes

Anything can be described as a system, but the level of uncertainty and control may vary.



**Systems & Processes**

Any system can be modeled as a black box with inputs and outputs. Given an objective (e.g. provide value) or a key result (e.g. making money), the progress can be understood using this simplified system:

- *Input*: money moving into the system (over time). E.g. through sales, or services being delivered to customers.
    - This can be defined as *throughput*
- *Output*: operational expenses (over time). The cost to turn inventory into sold products.
- *Inventory*: everything else. This category doesn't (yet) create value.
    - E.g. investments that can be sold or reserves that are kept for risk containment.
    - The longer inventory sits idle the lower the relative ROI. This drags down the performance of the whole.
    

Be careful not to make the boundary of the system too small, as it will lead to optimization of local optima.

Using these measurable properties, a universal system-metric would be: `input - output - inventory`. Any choice can be evaluated using this metric. Is the change going to improve this metric in a given timespan?

From this definition, it follows that any work that does not contribute towards throughput is either an investment or a complete waste.

> Working on the right thing > investing (e.g. optimizing, learning) > working on the wrong thing (over-producing)

As a complement to this metric, a relative ROI can be defined as: `(input - output) / inventory` (where inventory is never zero). This metric highlights the cost of inventory. Beware that it doesn't include absolute profit. Any comparison will have to be adjusted for scale (e.g. thousands or millions). 

The future profitability can be defined as the [expected value](https://en.wikipedia.org/wiki/Expected_value) of the first metric: `E[input] - E[output] - E[inventory]`. Naturally, the [risk-adjusted return](https://en.wikipedia.org/wiki/Risk-adjusted_return_on_capital) is obtained by dividing this metric by the variance (or some other proxy for risk).



**Propagation of errors**

>  A chain is no stronger than its weakest link.

The variance of a system is [equal](https://en.wikipedia.org/wiki/Bienaym%C3%A9%27s_identity) to the sum of the variance of each individual component and the covariances between them. In systems with high dependence (correlation), any bottleneck will greatly impact the product of the system. The typical example of this is traffic congestion.

The only way to exclude bottlenecks is to let the system run at partial capacity; build in slack. This requires a system to have more capacity than market demand, resulting in a a tradeoff between having formation of bottlenecks and resource efficiency.

Hence, a *bottleneck* can be defined as: any resource that has capacity ≤ than the demand placed upon it.

- Based on this definition, optimizing non-bottleneck components doesn't improve the efficiency of the system.
- Before optimizing a specific component it should be taken into account whether the component is likely to be a bottleneck.

The first step is to [find and study](https://en.wikipedia.org/wiki/PDCA) bottlenecks. Then resolve them. If this is not possible, either:

- Improve their efficiency and reduce their variance.
- Ensure that the resource is used for the right job.

In the same spirit, it can be concluded that any idle time of non-bottleneck resources is perfectly fine. This can even be preferable over over-production (which will increase inventory).

Tasks that go to bottleneck resources typically have high queue times, while all other tasks have high waiting times.



**Efficiency & Optimization**

> Resource activation does not imply resource utilization.

There are two types of efficiency:

- Efficiency of resources. 
    - Measured by resource utilization, which is defined as: "The percentage of time the resource is producing something which is contributing to the main goal". This definition excludes the production of e.g. spare parts.
    - Risks: inventory (over-production), over-stretching of resources, over-optimization (silos).
    
- Efficiency of flow (to customer). I.e. [pull-strategy](https://en.wikipedia.org/wiki/Push%E2%80%93pull_strategy), demand-oriented. Because the customer pays for the service.

Assume that people are never [blocked](https://en.wikipedia.org/wiki/Context_switch) and [always](https://en.wikipedia.org/wiki/Parkinson's_law) busy. Focus on the flow of *tasks*; ensure that they are not blocked. If tasks are picked up as planned (following demand), then people can be free to make improvements and learn.

> Low idle time is a side-effect of flow efficiency but not a method of reaching it.

In a *balanced* system, all resources produce exactly the right amount. There is no excess inventory. This theoretical state is dangerous. Any perturbation (expected variance) would be detrimental to flow, because all components are related and depend on each other. This inherent risk can be contained in two fundamental ways:

- Increase inventory. This decreases agility and limits cash flow.
- Decrease batch sizes, which decreases lead time. This increases setup time (handovers).



**Effectiveness**

The two main directions to be effective are:

- Deliver (maximize) value to customer. This may require investment and innovation (change).
- Eliminate (minimize) waste. This doesn't just demand reliability and stability, but it also requires an investment to remove obstacles.

This involve

- Continuous improvement of purposes, people, processes.
- Continuous discovery of value and waste.

Note that investment involves a short term cost by definition.





Management is about finding a balance. For example:

- Focus on an optimistic ideal or a realistic planning.
- Being adaptive (pragmatic) or being consistent (conservative).
- Optimizing for the next quarter or multiple decades.
- Optimizing the whole or focussing on individual components (e.g. departments, teams, individuals)
- Improve what you are doing or stop doing what you should not be doing



Time is constrained and limits productivity.

1. Be more productive, e.g. by increasing the productivity per employee or the number of employees.
2. Decrease the amount of work. Prioritization of *core* activities and outsourcing of *contextual* activities.
    - I.e. do what you'd do if time was even more constrained.

Making waste cheaper (e.g. through outsourcing) is not the same as improving a process.



**Types of Challenges**

Fundamental characteristics of the world (from [Buddhism](https://en.wikipedia.org/wiki/Three_marks_of_existence)):

1. Change. Nothing is permanent (time moves forward). As a result, systems degrade and expire. Hence there is a need to adapt, transform and sometimes start over. Naturally, even methods itself have to be adapted.
2. [Interdependence](https://en.wikipedia.org/wiki/Systems_theory). Consider components and connections. Hence we should embrace collaboration over isolation.
3. Dissatisfaction. Repetition is boring. Hence there is a need to iterate, learn and improve.

In addition, learning (adapting) takes practice. Both at the individual and organizational level.



**Organization Levels**

An organization may be divided into departments, teams and individual. At each level there is a trade-off between generalization and specialization. Two possibilities:

- Functional departments, DevOps teams, specialized individuals.
- Product-based departments, functional teams, generalized individuals.

Note, you can't specialize at every level without impacting cohesion, alignment and collaboration.



Local improvements and adaptation are a vital complement to top-down strategies.

- This requires alignment on all levels. Hence higher management should share their vision and strategy within the organization.
- Local improvements are usually easier than global ones.



**Influence (organizational level)**

[Three influences](https://danluu.com/culture/)

- Incentives. Rewards and punishments for behaviour or achievements.
- Processes. E.g. regulation, validation.
- Culture. "inherent" values. E.g. ideals to strive for.



**Work environment**

Company values should be reinforced though the work environment. E.g. if software quality is valued then internal software should also be of high standards.



## Collaboration

Reaching consensus on what *needs* to be done is easier than reaching consensus on what *can* be done.

Determine whether a team needs to **adjust** or whether it needs to **change**. Two different approaches can be:

- Use ceremonies & tools for team alignment (i.e. slight adjustment), until the desired behaviour or culture has been reached.
- Apply the concept of a "fresh start" whenever you want to change or disrupt the current way of working. E.g. formulate former practices or habits as something the "old" team would do, and the new practice as something you would do from now on.

Make sure there is regular reflection, both on the level of individuals and the level of teams.



Make goals and problems **visible**. E.g. using a scrum or kanban board, milestones. Dashboards, alerts, red/green builds. This incentivizes us to think about them (and re-think our approach).



**Meetings**

- Publish a schedule or agenda beforehand and stick to it. I.e. set expectations.
- Schedule time to do preparation and post-preparation.
    - These should be roughly proportional the length of the meeting and the number of participants.
- Avoid overfull meetings. Allow flexibility for attendees.



**Persistence**

One-pagers. One page is enough to introduce an idea but does forces the writer to be concise. In addition they are well-suited for collaboration. Although they are abstract, the corresponding idea should be measurable in order to be effective.



**Turnover**

- Warm welcome. Put in special care for team members that join and leave. These are critical moments.
- Note down their first impressions. This is a unique moment where one can get unbiassed input.



## Organizational Learning

An optimal learning environment has:

- A teacher/coach/facilitator
- Other learners
- Customer or real-world feedback

Learning requires both theory and practice (experimentation). Making mistakes is a vital part of learning.

- Prefer collaboration over competition. The latter discourages mistakes, and thus hampers learning.

Learning on a local level is easy, but learning at the "middle management level" is not (e.g. due to competition, fear of failure).





## Management per Type

**Crisis management**

- Dealing with risk after they've materialized.



**Expectation management**

- Under-promise (and over-deliver) to stakeholders. Avoid uncertainty and build trust.
- Over-promise internally, in order to motivate employees. In addition, prefer learning over blaming.

Technique:

1. What do you expect?
2. This is what you can expect. This is what we will do.



**Time management**

Let the other accept your schedule. Not everything is possible, so force the client to choose explicitly. Communicate transparently.



### Risk management

Definitions:

- Risk: a future undesirable event and events that precede it.

- Risk management: dealing with unpleasantness, instead of counting on luck.

The main *prerequisite* is a certain corporate culture: Thinking in probabilities & decriminalize risk. Uncertainty should be preferred over being wrong (or overly optimistic).

- Prefer mean-variance optimization over point-estimates. A typical prediction should include (un)certainty bounds. E.g. "We need at least 4 months, and it may take up to 1 year (in the worst case). We estimate a 80 % chance of finishing it in 6 to 8 months. "
- Express projects success not as an absolute (success or fail), but as progression (number of features delivered at end of time period).
    - Build in slack, i.e. the flexibility to skip/add/change features during the project.

A secondary prerequisite is a list of assumptions. These are (usually show-stopping) risks that are delegated upwards to the employer. This reduces the change of overlooking "unthinkable" risk.



**Types of Strategies**

1. General strategies:
    1. Avoid or limit tail-risk rather than focussing on winning.
    2. Diversify to handle idiosyncratic (unsystematic) risk. I.e. make multiple small bets over a single large one.
2. Specific strategies that don't address risk:
    1. Avoidance: don't take risks at all (but miss out on potential wins).
    2. Evasion (retainment): count on luck, assume low-probability events won't occur.
3. Specific strategies that do address risk:
    1. Containment: decrease impact of risk when they do occur. E.g. reserve *buffers*.*
    2. Mitigation: reduce containment cost. This has an up-front cost, independent of whether the risk will materialize. 



*Given a set of independent risks, the risk exposure per risk is the product of the probability of occurrence and the cost of occurrence. A conservative *buffer* is strictly higher then the total exposure. 

> Risk exposure = probability of risk times the cost of occurrence



**Types of Containment Strategies**

- Isolate; use layering.
- Minimize
- Monitor; collect information about the incident and the second-order effects. E.g. uncommon patterns.
- Active Defense



**Types of risks**

- Planning-related:
    - Inherent flaws in the schedule. E.g. an unrealistic, aggressive schedule
    - Requirements inflation; an increase in requirements over the scope of the project.
    - Ambiguity in the specification. Design decision that are deferred until implementation time.
    - Dependencies.
- Employee-related:
    - Employee turnover.
    - Poor productivity. E.g. due to lack of motivation, poor working conditions, problems with communication, collaboration or coordination.
- User-related
    - Usability (user interaction).
- Context-related
    - Adaptability (to new environments). E.g. scaling up.
    - Supply chain / dependencies.





**References**

[1]: Rother	"Toyota Kata: Managing People for Improvement, Adaptiveness and Superior Results"
