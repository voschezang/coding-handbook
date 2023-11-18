# Organizational Structure

[toc]

## Value Delivery

A [value chain](https://en.wikipedia.org/wiki/Value_chain) is the sequence of activities that are necessary to deliver *value* to the customer. This chain may cross departmental boundaries. If this is the case, then a small change could disrupt multiple departments.

Ideally each component in this chain has a [clear interface](https://en.wikipedia.org/wiki/Interface_segregation_principle). See [systems-management](systems-management.md).

These chains can intersect, based on the types of components in an organization. Ownership and responsibility of the whole value chain may be implicit. There can be independence of decision making and independence of releasing.

<img src="../img/feature-functional-teams.png" alt="feature-functional-teams" style="width:80%;" />



## Tradeoff in Interaction

### Consistency

**Availability and Consistency**
The flow of information is restricted by at least one of three properties. See [CAP theorem](https://en.wikipedia.org/wiki/CAP_theorem).

- Consistency. Whether newly retrieved information is up-to-date.
- Availability. Whether any request for information is satisfied immediately. Or, how soon a request is satisfied (latency).
- Partition tolerance. How well the system will continue to function in case of component or connection failures.

**Independence and Consistency**
One of the most impactful properties is independence. In software this comes down to modularity. Doing something in isolation and locally is generally easier than at a larger scale, with where multiple components may interact in complex ways. However, independence is associated with [redundancy](http://yosefk.com/blog/redundancy-vs-dependencies-which-is-worse.html). It comes at the cost of consistency.

Two related factors are *alignment* and *autonomy*.

### Efficiency and Flexibility

These are (to some extend) negatively correlated. Optimizing for efficiency limits flexibility.

This relates to [the bias-variance tradeoff](https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff) in data science; you can either optimize for a specific situation or adapt to many different situations.



### Autonomy and Alignment

Note that there are multiple paradigms that are theoretically sound. The important part is to be able to adapt at both the organizational- and the team-level.

<details>
<summary><b>Alignment &amp; Autonomy</b></summary>
<h4>Power of continuous improvement</h4>
<p>This is a model of an organization with autonommous components. While making local optimizations, each components effectively moves in random directions. With a tiny amount of alignment (vision) the total movement of the system can be altered radically.</p>
<img src="../img/plot-random-walk.png" alt="plot-random-walk" style="width:90%;"/>
<h4>Frameworks</h4>
<img src="../img/plot-alignment-autonomy.png" alt="plot-alignment-autonomy" />
</details>

**By Domain**

Organizations cannot be studied properly without taking into account the domain in which they live. See [learning](../intelligence/learning.md). See also the  Stacey matrix model.

Four [*domains*](https://en.wikipedia.org/wiki/Cynefin_framework) ordered by structure are:

1. Chaotic. *"Novel practice"*.
    1. Act immediately, then evaluate, then respond. [Triage](https://en.wikipedia.org/wiki/Triage).

2. Complex. *"Emergent practice"*. Learn at the same pace that the environment is changing.
    1. Probe, experiment, then evaluate, then respond.
    1. Suited for "Agile". Focus on learning.

3. Complicated. *"Good practice"*. In absence of a single best practice (golden hammer).
    1. Analyze the problem, then respond.
    1. Suited for "Lean". Focus on optimization.

4. Obvious. *"Best practice"*
    1. Categorize the situation by using existing models.

There are two fundamental dimensions of of influence.

1. Alignment: from flexibility to consistency.
2. Autonomy: from centralized to distributed.

These dimensions are intertwined and the optimum is situational. The following image gives an example of how the level of regulation can affect the value that is produced and delivered. Other properties with similar effects are: overstaffing and up-front planning.

![plot-process-value-per-domain](../img/plot-process-value-per-domain.png)





## Types of Components



### Hierarchy of Components

A large organization can consists of sub-organizations. E.g. departments, divisions, teams. It is not possible to specialize at every level without impacting cohesion, alignment and collaboration.

This section uses the term "team" instead of "component" for simplicity, but the categories do generalize beyond this. Moreover, different levels typically have a different structures. E.g. functional departments with cross-functional teams.

1. Functional, specialist teams (or departments or roles).
2. Feature or product teams.
3. Core + Context.



**Functional Team**

Focus on either a specific functionality or domain. E.g. a user-interface or a database. Because the team is subordinate to the whole, there is high alignment and low autonomy. There is a uniform user-interface, but every change can affect all components, which limits flexibility of the system.

A typical separation:

- R&D. Focus on innovation. Embrace variance.
- Dev. Deliver unique products.
- Ops. Deliver standardized products. Minimize variance.

Ideally, these teams would collaborate closely, rather than hand-over work.



**Feature or Product Team**

Focus on a product, service, or feature. E.g. a random name generator service. The independence gives the team high autonomy. This increases productivity and flexibility, but the lack of alignment to the whole can lead to over-optimization.



**Core + Context**

This design attempts to avoid the strong coupling of functional teams and the weak alignment of product teams. There are a few variants:

1. A major core component + minor contextual adapters. E.g. a [hexagonal architecture](https://en.wikipedia.org/wiki/Hexagonal_architecture_(software)).
2. A facade (or proxy) + complementing services. E.g. a front for the user, that creates the illusion of uniform system. The complementing services provide the main functionality.
3. Multiple facades.

Note that the facade and the complementing services can be either function-oriented or feature-oriented.



### Software Organizations

Graphically, this can look like this. The bottom images (autonomy, matrix) are two extremes, where teams are optimized for a local purpose. Depend on the alignment and communication between teams the structure can be rigid.

![org-arch](../img/org-arch.png)

There are two inherent boundaries between components. Often, each component is responsible (and optimized) for their own domain.

- **Functional** Boundaries. E.g. between dev, ops, sales, marketing, security, compliance.
- **Product** Boundaries. Between products or features.

Local interaction and changes are generally much easier than non local ones.

![communication-patterns](../img/communication-patterns.png)
