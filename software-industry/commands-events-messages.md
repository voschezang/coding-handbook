# Commands & Events

Organizational structure can range from hierarchical to flat.

![orchestration-choreography-orgs](../img/orchestration-choreography-orgs.png)

Hierarchies allow commands to be distributed efficiently.

As an example, consider the relations between an employer and their employees.

**Commands** flow along the hierarchy. Commands require authority.

- The employer can give commands to employees. E.g. assignments or priorities.
- The employees can obey or challenge these commands.
- Either can break the contract (hierarchy)

**Messages** can be send in any direction, even between employees. This includes proposals and opinions.

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

### Information Sharing

Information can be send in the form of commands, events or requests. It can be send one-to-one or broadcasted. The information can be part of the core domain, it may support the core domain, or it can be generic.

<img src="../img/relationship-types.png" alt="relationship-types" style="width:90%;" />

