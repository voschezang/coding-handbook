# Organizational Structure

Let an **organization** be defined as *an interdependent set of components that work together towards a common goal*.  The alignment, autonomy and coordination of these components complicates the path to the goal.

The optimal structure of an organization is highly dependent on the domain and scale. At the same time, the behaviour of these systems can be surprisingly similar. Examples of organizations are:

- A government
- A company, or a specific department or team within that company
- A software application, consisting of layers such as a user-interface, a business-layer and a database.
- A system of applications, where the components are services.
- An ecosystem. E.g. a market



Control of an organization vary between being completely centralized or completely distributed. See also [programming-paradigmes.md](programming-paradigms.md).

- Orchestration: communication happens through *commands*. E.g. a CEO makes an order.
- Choreography: communication happens mainly by *events*. E.g. an investor broadcasts that they are offering stock at a certain price.



## Autonomy and Alignment per Domain

Organizations cannot be studied properly without taking into account the domain in which they live.

Four [*domains*](https://en.wikipedia.org/wiki/Cynefin_framework) ordered by structure are:

1. Chaotic. *"Novel practice"*
2. Complex. *"Emergent practice"*
3. Complicated. *"Good practice"*
4. Obvious. *"Best practice"*

There are two fundamental dimensions of of influence. 

1. Alignment: from flexibility to consistency.
2. Autonomy: from centralized to distributed.

These dimensions are intertwined and the optimum is situational. The following image gives an example of how the level of regulation can affect the value that is produced and delivered. Other properties with similar effects are: overstaffing and up-front planning.

![plot-process-value-per-domain](/Users/mark/stack/src/coding-style-guide/img/plot-process-value-per-domain.png)



## Hierarchy of Components

A large organization can consists of sub-organizations. E.g. departments, divisions, teams. It is not possible to specialize at every level without impacting cohesion, alignment and collaboration.

This section uses the term "team" instead of "component" for simplicity, but the categories do extend beyond this.

1. Functional teams.
2. Feature or product teams.
3. Core + Context.



**Functional Team**
Focus on either a specific functionality or domain. E.g. a user-interface or a database. Because the team is subordinate to the whole, there is high alignment and low autonomy. There is a uniform user-interface, but every change can affect all components, which limits flexibility of the system.

**Feature or Product Team**
Focus on a product, service, or feature. E.g. a random name generator service. The independence gives the team high autonomy. This increases productivity and flexibility, but the lack of alignment to the whole can lead to over-optimization.

**Core + Context**
This design attempts to avoid the strong coupling of functional teams and the weak alignment of product teams. There are a few variants:

1. A major core component + minor contextual adapters. E.g. a [hexagonal architecture](https://en.wikipedia.org/wiki/Hexagonal_architecture_(software)).
2. A facade (or proxy) + complementing services. E.g. a front for the user, that creates the illusion of uniform system. The complementing services provide the main functionality.
3. Multiple facades.

Note that the facade and the complementing services can be either function-oriented or feature-oriented.

