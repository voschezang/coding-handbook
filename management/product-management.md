# Product Management

This document explores the management of [products and projects](../labour/products-projects-initiatives.md). It de-emphasises [business operations](https://en.wikipedia.org/wiki/Business_operations). See also [goals and strategy](./goals-planning-strategy.md),  [management principles](../management-principles.md), [requirements-engineering](../requirements-engineering.md) and [results](../labour/realization.md).

[toc]

## Overview

**Components**

1. People. An organization, developers and customers.
2. Products and services. Markets and competitors.



**Activities**

1. Discovery. Channels and methods to deliver value.
2. Delivery. Realizing a vision. Responding to change.



**Value Chain**

Two perspectives are a contextual view and an internal view. These map to the value and production chains.

<img src="../img/value-chain-production-chain.png" alt="value-chain-production-chain" style="height:15em;" />



The value chain exists within an environment and a context. The scope of product manager stops at this boundary. The value chain is contingent upon organizational (and technical) capabilities. See [accountability](../collaboration/accountability.md).

<img src="../img/value-chain-environment.png" alt="value-chains-environment" style="width:40em;" />

In some cases there are multiple value and production chains. For example a internal platforms (products) that enable  commercial products.



### Contextual View

Running a business involves collaboration and [management](https://en.wikipedia.org/wiki/Business_Model_Canvas).

- It is centered around a **value proposition**.
- **Activity**. Coordinating partners and resources in order to realize the proposition.
- **Channels**. Delivering to customers. Developing relationships with customers.



<img src="../img/grid-business-partners-customers-value.png" alt="grid-business-partners-customers-value" style="height:12em;" />



### Internal View

Value delivery is the result of realization of a vision. See [performance](../collaboration/team-performance.md).

<img src="../img/grid-organization-production-product.png" alt="grid-organization-production-product" style="height:12em;" />

Value delivery is contingent upon production and capability.



<img src="../img/product-production-capability.png" alt="product-production-capability" style="width:55%;" />



## Value Delivery

Value is a mix of direct value and growth.

<img src="../img/growth-and-value.png" alt="growth-and-value" style="height:16em;" />



### What

Value delivery can be understood in two directions. See [delivery](../labour/realization.md).

**1.** Ideas guide production, which results in increments, which are delivered to users, which provides them value, which results in profit.

<img src="../img/output-outcome-impact.png" alt="output-outcome-impact-project" style="width:80%;" />



**2.** Ideas guide target conditions, which guide planning, which results in initiatives, which result in execution. 



![output-outcome-impact-reversed](../img/output-outcome-impact-reversed.png)

See also [initiatives](../labour/initiatives.md) and [bets](../labour/bets.md).



### How

Three innovation horizons. From exploitation to exploration. *Do you want it cheap, quick or good?*

1. Current cash-flow (value): profitable now. Risk: they may become a commodity.
2. High-growth businesses: will become cash-flow.
3. Growth options: will potentially become growth.

<img src="../img/effective-efficient-predictable.png" alt="effective-efficient-predictable" style="height:16em;" />



## Background

### Project Management

**From project to product**

> Product management combines short term projects with long-living products.



![output-outcome-impact](../img/output-outcome-impact-product-project.png)



**Not project, but project<u>s</u> management**
Often, projects are executed in conjunction to each other. To avoid local optimization, the portfolio of products must be taken into account.

**The problem of uncertainty**
In uncertain environments, projects will usually fail to meet either time, cost or initial requirements. In the presence of both [idiosyncratic](https://en.wikipedia.org/wiki/Idiosyncrasy) and [systematic risk](https://en.wikipedia.org/wiki/Systematic_risk) there can be a need for flexibility or agility. Moreover, the behaviour of users and market dynamics are even more difficult to predict. This can be address in several ways.

- A product strategy may consists of [multiple](https://en.wikipedia.org/wiki/Diversification_(finance)) initiatives that are designed to create a competitive edge.
- Continuous product discovery. Iteratively testing beliefs.
- Fast delivery of product increments.



### Strategy

Ansoff's matrix. Product-Market Expansion Grid. Uncertainty increases from top-left to the bottom-right.

|                      | Existing Products  | New Products                   |
| -------------------- | ------------------ | ------------------------------ |
| **Existing Markets** | Market penetration | Product development            |
| **New Markets**      | Market development | Product/Market diversification |

[Porter's generic strategies](https://en.wikipedia.org/wiki/Porter's_generic_strategies): market and competitive advantage

|                                      | Uniqueness / value                                           | Cost position                                                |
| ------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **Industrywide / mass scope**        | Differentiation leadership<br />(marketing, branding, quality) | Overall cost leadership<br />(economies of scale, efficiency) |
| **Particular segment / niche scope** | Differentiation focus<br />(target/respond to specific customer needs) | Cost focus<br />(limit scope/complexity)                     |

Philosophy

- MVP. Then iterate
- Be insanely great (Apple).



### Terminology

**Software as a service**

- [SaaS](https://en.wikipedia.org/wiki/Software_as_a_service): the customer manages the (application) data and access to it.
- [PaaS](https://en.wikipedia.org/wiki/Platform_as_a_service): the customer manages the application themselves.
- [IaaS](https://en.wikipedia.org/wiki/Infrastructure_as_a_service): the customer manages the application and its runtime (e.g. the OS).

- [B2B](https://en.wikipedia.org/wiki/Business-to-business): Sell to a business
- [B2C](https://en.wikipedia.org/wiki/Direct-to-consumer): Sell directly to a consumer

**Marketing**

- Focus, sell one idea. Kort en bondig.
- Analogies to fuel imagination.
- Present features as solutions

**Market**

> Good strategy means saying no.

Don't expect to satisfy all possible customers. Instead optimize for a limited subset of them.

- Target market: optimize product for this market
- Boundary: additional sales, but don't optimize product for this markter
- Excluded from target

[Market segmentation](https://en.wikipedia.org/wiki/Market_segmentation) is key because perception of value is subjective. In non-segmented markets, customers with high value perception pay just the average price and customers with relatively low value perception will not pay at all. Ideally products are optimized for a single user, at scale.

**Lifecycle Mangement**

Designing products and leading product-based teams is one thing. A next challenge is managing complexity, which might increase as systems and codebases evolve.

Solutions include:

- Move from product-based teams to functional teams (or back).
- Scope down applications, outsource non-core activities.

**Innovation**

The main constraints are:

- Capital. Expected rate of return of an investment should exceed the interest rate (weighed by risk).
- Human capital. E.g. organization size.

Similar to markets, processes may have to be adjusted constantly. Do have regular conversations about the tooling and way of working. Don't rely on just metrics.

**Timeline**

![plot-expected-completion-time](../img/plot-expected-completion-time.png)

![plot-estimated-num-features](../img/plot-estimated-num-features.png)



## Anti-patterns

[Agile Product Ownership](https://www.youtube.com/watch?v=502ILHjX9EE) - overview by Henrik Kniberg

**Customer chasing development**
Optimize on satisfying a single customer, instead of a market.

**Feature Factory**
Bias for releasing features, rather than solving customer problems. See [software-engineering](../software-engineering.md%5D).

**Pet Projects**
Build something in secret to avoid the administrative or collaborative overhead.

**Promotion driven development**
Bias for optics & complexity. Build interesting stuff tools of useful tools.

**Shadow Strategy**
A [locally optimized, simplified version](https://twitter.com/johncutlefish/status/1574851694348750849) of a greater strategy. It may be created by ignorance or on purpose (for motivational reasons).

**Zombie product**
A product that is kept alive for political or personal reasons rather than market demand.

