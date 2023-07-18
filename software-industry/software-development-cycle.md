## Software Development Cycle

> Agile is a mindset, not a process

The [structure of teams](../systems/organization-structure.md) and departments has a great impact on how software is developed. Having specialized/functional teams often requires a fixed release cycle with *handovers*, whereas product-teams can (ideally) develop independently. The former can lead to a "waterfall" way of working, while the latter is considered to be "agile".

A software development process usually consists of phases such as: `requirements, analysis, design, implementation, testing, operations`. In practice some phases can be combined, e.g. using TDD. In general, the following steps will increase quality:

1. Include all the phases. At minimum, these phases are done in sequence.
2. Adjust after obtaining new information. Go back and forth between consecutive phases.
3. Do it twice. Iterate frequently. Strive to release "version 2". Prototype for `1x`, design for `100x`, and only then build for `10x`.

**Two extremes: from *efficient* to *flexible***

See [project management](../management/project-management.md).

1. Waterfall. A fixed project scope, price and deadline. Future changes are expensive.
    1. Designed for *throughput* and *stability*.
    2. Requirements drive design which drives development.
    3. Top-down decision making. Specialized (functional) teams with limited responsibility.
    4. `Outcome = Output`
2. Agile
    1. Designed to be *fast* and to be resilient to *changing requirements* (due to customers, markets or technology).
    2. Objectives (outcomes) drive discovery which drives development.
    3. Collaborative decision making. Empowered cross-functional teams.
    4. `Outcome > Output`

**Agile**

The ability to inspect and adapt; to be able to create or adjust your own process.

Formal principles:

1. Individuals and interactions over processes and tools
2. Working software over comprehensive documentation
3. Customer collaboration over contract negotiation
4. Responding to change over following a plan

Practice:

- Focussing on value streams (towards the customer) instead of resource efficiency.
- Eliminating waste, e.g. inventory or unreleased software.
- Minimizing lead time per feature. This can greatly reduce risk.
- Having goals that are guiding rather leading. Defer uncertain decisions unless there is a good reason not to.

A few frameworks for small or decentralized organizations:

1. [Scrum](../collaboration/scrum-guide.md): sprinting to a goal, MVP-first. Limit total WIP (number of tasks/features).
2. Kanban: continuously improving. Limit WIP per phase (e.g. `dev, review, test, release`).
3. The hacker way: no deadlines, no fixed teams, no synchronization.

Notes

- Agile is a tradeoff of agility (flexibility) and efficiency. Optimizing for a given use-case does come at the cost of being flexible. You cannot optimize for everything.
- If the full strategy is decided top-down then the agility of development teams is limited.

**DevOps**

DevOps *an sich* is similar to [vertical integration](https://en.wikipedia.org/wiki/Vertical_integration).

> You build it, you run it.

The DevOps movement goes further than this. It [emphasizes](../intelligence/learning.md) flow, feedback and learning. Especially the latter requires empowerment and autonomy of teams.

- Specialization can be achieved by scoping down the product (e.g. into a microservice), and outsourcing (e.g using SaaS products).
- Maximizing flow goes hand-in-hand with a fast, automated build-test-deployment process. E.g. be able to deploy 100 times per day.

<img src="../img/flow-3-steps.png" alt="flow-3-steps" style="width:80%;" />

**Anti-pattern**

- FrAgile: Agile teams without authority to overcome bureaucratic impediments.
- Product-oriented teams in a project-oriented (management or bureaucratic) environment.
- Feature factory. A focus on *delivering* new functionality rather than *solving* long-term customer problems (quantity over quality). This can result in high WIP.

## References

- [Agile manifesto](https://agilemanifesto.org/)
- [Heuristics](https://holub.com/heuristics/)
