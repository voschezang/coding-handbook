# Risk Management

> Yesterday’s problem is tomorrow’s risk

Definitions:

- Risk: a future undesirable event and events that precede it.

- Risk management: dealing with unpleasantness, instead of counting on luck.

```
Total Risk = threads (external) + vulnerabilities (internal)
```

The main *prerequisite* is a certain corporate culture: Think in probabilities & decriminalize risk. Uncertainty should be preferred over being wrong (or overly optimistic).

- Prefer mean-variance optimization over point-estimates. A typical prediction should include (un)certainty bounds. E.g. "We need at least 4 months, and it may take up to 1 year (in the worst case). We estimate a 80 % chance of finishing it in 6 to 8 months."
    - Usually point estimate overestimate in order to compensate for uncertainty. This can result in an [increase](https://en.wikipedia.org/wiki/Parkinson's_law) in the amount of work

- Express projects success not as an absolute (success or fail), but as progression (number of features delivered at end of time period).
    - Build in slack, i.e. the flexibility to skip/add/change features during the project.

A secondary prerequisite is a list of assumptions. These are (usually show-stopping) risks that are delegated upwards to the employer. This reduces the change of overlooking "unthinkable" risk.



## Strategies

1. General strategies:
    1. Avoid or limit tail-risk rather than focussing on winning.
    2. Diversify to handle idiosyncratic (unsystematic) risk. I.e. make multiple small bets instead of a single large one.
2. Specific strategies that don't address risk:
    1. Avoidance: don't take risks at all (but miss out on potential wins).
    2. Evasion (retainment): count on luck, assume low-probability events won't occur.
3. Specific strategies that do address risk:
    1. Containment: decrease impact of risk when they do materialize. E.g. reserve *buffers*.*
    2. Mitigation: reduce containment cost. E.g. though insurance. This has an up-front cost, independent of whether the risk will materialize.

*Given a set of independent risks, the risk exposure per risk is the product of the probability of occurrence and the cost of occurrence. A conservative*buffer* is strictly higher then the total exposure.

```
Risk Exposure = probability x materalization cost
```



**Containment Strategies**

- Isolate; use layering.
- Minimize
- Monitor; collect information about the incident and the second-order effects. E.g. uncommon patterns.
- Active Defense



## Types of risks

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