# Product Discovery

Discovery is about alignment, planning and testing. Also see [requirements](project-requirements.md), [bets](bets.md) and [results](realization.md).

[toc]

## Overview

Approaches

- Discover what people want, and build it.
- Start with what you can build and discover out to make people want it.



Discovery consists of:

- Discovering new product ideas.
- Discovering the needs of customers, stakeholders and users.
- Translating ideas into plans. Using traditional [project management](https://en.wikipedia.org/wiki/Project_management) or storytelling.
- Testing (optimizing) market fit.



<img src="../img/prototype-to-release.png" alt="prototype-to-release" style="width:90%;" />

Discovery happens after a mission and vision are set.

![purpose-discovery](../img/purpose-discovery.png)



The next sections are about **translation** between ideas, goals and plans. It present a method based on storytelling. It emphasizes:

- Storytelling over requirement handovers.
- Experiments over upfront planning.



## Translation

>  Specialists know what they want, but groups do not.

One of the hardest parts of software engineering is communication and alignment. The biggest waste is not inefficiency, but rather misdirection. This is caused both by *a priori* unknowns and miscommunication.

One solution to this issue is to develop software incrementally, and continuously incorporate feedback. This requires strong alignment on abstract goals, and flexibility in planning.

This section sections present a way of translating product ideas into concrete plans.



### Storytelling

>  "Stories get their name from how they’re supposed to be used, not from what you’re trying to write down" ~ Jeff Patton

User stories a way of working that is based on *telling stories*. It prioritizes shared understanding over formal documents and requirements. 

- Stories tend to emphasize people and their purpose. Developing a plan is secondary to this.
- Telling a story requires *at least* two people. Conversations may involve the organization, customers, users and developers.

Use documentation to recall conversations rather than as an alternative for them.

#### User Stories

> A user's story. How a user would call the feature.

A user story has three components. See [extreme programming](https://en.wikipedia.org/wiki/Extreme_programming).

| Component    | Action                                                       |
| ------------ | ------------------------------------------------------------ |
| Card         | Write down a sentence that describes what you'd like to see. |
| Conversation | Explore the idea together, using words and pictures.         |
| Confirmation | Record your agreements.                                      |

The conversations should lead to agreements on:

- Acceptance criteria. *How do we know that we’re done?*
- Demo. *How can we demonstrate this to stakeholders?*

A plan to *implement* the user story can be created *ad hoc*, e.g. in a refinement session.



#### Traditional Project Management

This approach differes from traditional project management. Project requirements are formulated after a negotiation. They are then handed over to developers. This works well for predictable environments.

|                | Project document    | (User) Story                |
| -------------- | ------------------- | --------------------------- |
| **Purpose**    | Delivery            | Alignment                   |
| **Creation**   | Through negotiation | Through conversation        |
| **Delivery**   | Handovers           | Continuously                |
| **Commitment** | Time, scope or cost | Satisfy acceptance criteria |
| **Optimize**   | Output              | Outcome                     |



#### Discovering Requirements

> The worst thing you can do is start building immediately.

A typical problem of projects is that there can be a huge amount of uncertainty at the time of their formulation. This effect is stronger for larger projects.

An alternative to this is to use [experiments](bets.md) before building new features. This may involve questionnaires, paper prototypes, wireframes, mockups, etc.



> “Requirements” means shut up.

![user-story-requirements](../img/user-story-requirements.png)



**Anti-pattern**

*"Give me the requirements, I don't need to understand the problem."*



## Experiments

See [bets](bets.md).



## References

- Patton. *User Story Mapping*

