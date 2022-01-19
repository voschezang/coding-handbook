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



## Hierarchy of Components

This section uses the term "team" instead of "component", but the categories do extend beyond this.

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

