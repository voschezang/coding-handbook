# Team Productivity

This is a model for team productivity. It provides insight into dynamics such as stabilization and innovation. See also team [productivity](team-productivity.md) and [success](success.md).

<img src="../img/dragon-productivity-cycle-bg.jpg" alt="dragon-productivity-cycle-bg" style="height:8em;" />

## Introduction

Teams tend to evolve naturally through periods of instability and growth. Both productivity and value delivery fluctuate throughout these periods. A common approach is to balance the ratio between operations and strategic investment. However, a single ratio provides little control and predictive value. Our model offers a more refined view. It models the progression of productivity as an evolution through distinct challenges, and predicts shifts in priorities and productivity.

<img src="../img/team-productivity-lifecycle.png" alt="team-maturity-lifecycle"/>

The model is derived from the typical challenges faced by teams. Consider a fire brigade as analogy. Ordered by criticallity: recurring fires, traffic congestions, road detours, slack.

|                | 🔥 Recurring incidents                            | 🚗 Congestion                 | 🚧 Detours                          | 🧯 Slack                                          |
| -------------- | ------------------------------------------------ | ---------------------------- | ---------------------------------- | ------------------------------------------------ |
| **Constraint** | Too much work, components breaking down          | Too much WIP                 | Too much tech. debt                | Outdated value proposition, lacking capabilities |
| **Signals**    | Recurring incidents,skills gaps, growing backlog | Long queues, dependencies    | Complexity / clutter, workarounds. | Ambition / growing potential                     |
| **Solution**   | Hire more or reduce scope                        | Focus, improve collaboration | Make time                          | Balance expectations                             |

For each constraint, a team may focus on the following solution.

1. 🔥 **Firefighing**. Sprinting towards immediate results. Reacting to incidents. The backlog grows faster than the team can handle.
2. 🔄 **Flow**. Stop starting, start finishing. Freeze backlog and finish WIP together. Reduce waste. Incorporate feedback earlier.
3. 🪴 **Gardening**. Focus on quality, upkeep and cleanup. Pruning. Streamline complexity.
4. 🚀 **Innovation**. Re-adjust value proposition and capabilities. Growing the team scope.

When a team does not commit to solving a single constraint, it might plateau. Likewise, if a team commits to too many constraints, their effort diffused and progress will falter. Ideally, when a team does succesfully lift a constraint it will transition on to a new phase.

## Unsustainable Productivity

The harder a team pushes towards the last phase, the greater the resistance it will encounter. The innovation phase is especially unpredictable, due to its side-effects:

- Natural entropy caused by new tooling, processes or scale. Need to maintain the newly developed tooling.
- Organizational pressure to focus on lower-performing teams. Team members being be re-allocated.
- Performance being penalized by higher expectations or workload.
- External changes that disrupt the team.
- Experimentation being seen as a opportunity to cut costs.

This provides two paths forward.

- Focus on innovation and growth. Plan to evolve the team after a limited period of innovation - and continue with phase 1.

- Be conservative and spend a minority of effort on innovation. Attempt to keep a balance between operations and innovation.

## Long-term Productivity

The instable phases result to a characteristic pattern, not unlike to boom and bust cycles in economics. Over-optimizing for growth and innovation will fail eventually, and result in a period of underperformance.

<img src="../img/productivity-cyclical-evolution.png" alt="productivity-cyclical-evolution" style="height:12em;" />

Another analogy is that of (simulated) [annealing](https://en.wikipedia.org/wiki/Simulated_annealing). This optimization technique alternates stabilization (exploitation) with diversification (exploration). Local optimization is alternated with diversification to improve the global state.



## Release Frequency

Organizations guide productivity by setting a release frequency. Fast releases allow more immediate reactions to competition. However, there are various considerations. Release frequency is direclty related to batch size and efficiency. 

- Greater batch sizes can improve resource utilization, through economies of scale. Repetition allows for optimization.
- Overproduction can be used as a buffer against supply chain disruptions.

There are various downsides to larger batch sizes.

- **Risky big-bang releases:** Large, all-at-once deployments are harder to test and even harder to redirect if things go wrong.
- **Complex coordination:** Bundling many features together requires significantly more planning and cross-team alignment.
- **Incident response:** Long release cycles make it difficult to react to incidents. Urgent patches must be shipped as [hotfixes](https://en.wikipedia.org/wiki/Hotfix), which increases both risk and rework.
- **Incentive to delay:** Longer cycles encourage teams to postpone releases, waiting to include "just one more feature" rather than shipping now.

Our model provides multiple lenses to view release frequency. The table below shows the effects of release frequencies on different constraints.

<img src="../img/map-constraints-release-frequency.png" alt="map-constraints-release-frequency" style="max-height:25em;" />

Notes

- ⚠️ Immediate escalation immediately is a feature, rather than a problem. Proper change management and administration makes it easy to connect to the necessary teams and resolve the issue immediately.
- 💣 Large releases are a kind of pressure cooker. Errors go unnoticed, until the release date. Then they show up everywhere all at once.
- ⚙️ "BAU" means: manage projects and dependencies. This is *business as usual* in large software organizations that use large release cycles.
- 📦 Continuous delivery involves *canary deployments*. Releasing changes gradually to user, in order to mitigate the impact of incidents.
- 🧑‍🔬 Continuous discovery refers to the discovery of a product/market fit. Automated experiments allow algorithms to be optimized for specific customer segments.

