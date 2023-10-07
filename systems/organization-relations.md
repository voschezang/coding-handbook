# Relations

Relations of components in a system can be understood in terms of:

- The direction of relations
- The type of relations

[toc]

## Autonomy and Control

The short-term behaviour of agents in a system determined by their *a priori* configuration and their (local) interaction. Interaction can be driven by demands or individual preferences. These interactions result in [orchestration](https://en.wikipedia.org/wiki/Orchestration_(computing)) and [choreography](https://en.wikipedia.org/wiki/Service_choreography), respectively. The former relies on command-driven communication that are pushed to specific agents. The latter is associated with agents that observe their surroundings and reaction autonomously.

- Depending on the domain, there is a need for a balance between the two. Too much orchestration can lead to inflexibility. Too much choreography can lead to anarchy or chaos.

|                    | Orchestration              | Choreography               |
| ------------------ | -------------------------- | -------------------------- |
| **Nature**         | Chain of command           | Autonomous agents          |
| **Centralization** | Central point of influence | Absence of a central point |
| **Optimized for**  | Execution, transparency    | Agility, resilience        |
| **Risk**           | Inertia                    | Anarchy                    |
| **Communication**  | *Commands*                 | *Events*                   |

Note that the social structure may change over time.



**Alignment**

The alignment of agents may change over time. Their behaviour can be flexible or consistent.



### Commands and events

|                 | Command      | Event          |
| --------------- | ------------ | -------------- |
| **Example**     | `doThis`     | `thisHappened` |
| **Orientation** | Future       | Past           |
| **Control**     | Demand       | Assertion      |
| **Direction**   | Peer-to-peer | Broadcasting   |

Communication (commands) may happen *synchronously* - with blocking messages - or *asynchronously*.



Event-based patterns

- See: [publisher-subscriber](https://en.wikipedia.org/wiki/Publish%E2%80%93subscribe_pattern) at the architecture level, [observer](https://en.wikipedia.org/wiki/Observer_pattern) at the application level.
- See the [Saga](https://learn.microsoft.com/en-us/azure/architecture/reference-architectures/saga/saga) pattern.



## Power

Decisions are made and forwarded according to a [chain of command](https://en.wikipedia.org/wiki/Command_hierarchy). This power structure may be:

- Explicit or implicit.
- Centralized or distributed.
- Tight or loose coupled. E.g. by formulating requests based on input, output or outcomes. E.g.
    - *"Execute these steps."*
    - *"Solve this problem by building feature X"*
    - *"Find a way to ensure that a user can achieve Y"*

[Power](https://scholar.google.nl/scholar?hl=nl&as_sdt=0%2C5&q=+A+typology+of+organisational+cultures+-+Westrum&btnG=) in organizations can follow several patterns. Based on the flow of information, the following categories can be distinguished.

1. **Authoritative**: Strive for <u>power</u>. Follow chain of command. Compete for individual gain.
2. **Bureaucratic**: Ensure fairness and resilience through <u>rules</u>. Maintain the status quo. Adhere to rules and policies.
3. **Generative**: Strive for group performance. Be pragmatic.
4. **Idealistic**: Prioritize ideals and values over individuals. Shared (higher) purpose.

These categories have the following properties.

|                                  | Oriented             | Success                                            | Responsibility       | Scale                         | Risks                                                        |
| -------------------------------- | -------------------- | -------------------------------------------------- | -------------------- | ----------------------------- | ------------------------------------------------------------ |
| **Authoritative** (pathological) | Power-oriented       | (Individual) Power.                                | Chain of command.    | Limited                       | Hide information from competitors. Suppress risks.           |
| **Bureaucratic**                 | Rule-oriented        | Fairness, protection. Sometimes scale, efficiency. | Narrow, but explicit | Global                        | Slow, difficult to adapt. Bias for status quo. Lack of individual freedom. |
| **Generative**                   | Performance-oriented | Effectiveness, outcomes.                           | Shared               | Global, but unstable          | Disruptive, unstable. Bias for metrics.                      |
| **Idealistic**                   | Value-oriented       | Following ideals.                                  | Shared               | Global, but limited cohesion. | Idealism over realism.                                       |



## Type of relations

Information can be send in the form of commands, events or requests. It can be send one-to-one or broadcasted. The information can be part of the core domain, it may support the core domain, or it can be generic.

<img src="../img/relationship-types.png" alt="relationship-types" style="width:90%;" />

