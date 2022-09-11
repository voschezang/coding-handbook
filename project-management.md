# Project Management

This document is about refining and implementing an assignment. Such an assignment can be for example a project or user-story.

See also [product-management](product-management.md)  [management principles](management-principles.md) and [requirements-engineering](requirements-engineering.md).

[toc]

## Overview

There are a few phases that can be distinguished in a typical assignment.

- **Refining** the assignment to ensure that for example the right feature will be build.
    - It is likely that *your interpretation* of the initial requirements is imperfect.
    - There can be *ambiguity* - or even imperfection - in the initial requirements. It may be beneficial to analyze the problem in advance.
    - During the implementation of the project the context may *change* - which could require deviations for the planning. Hence there is some risk management involved.
- **Execution** of the refined assignment. This phase may reveal surprises. This may lead to deviations.
    - This may include resourcing.
- **Review** of the implementation. This includes communication to stakeholders.



### Refinement

Alignment with:

- Stakeholders. E.g. the assigner or sponsor.
- [Customers](https://en.wikipedia.org/wiki/Customer). E.g. the ones that will recipient some service or product.
- Employees and hires.



#### Planning

An assignment can be broken down into sub-tasks. For both these levels there is a certain amount of [requirements engineering](requirements-engineering.md) involved.



#### Sizing

Projects can usually be split up into smaller parts that are delivered immediately - to customers. Estimating the optimal granularity *a priori* is difficult. The major benefits of small deliverables are:

- Provide revenue *sooner*.
- Allow subsequent iterations to incorporate *feedback* from customers.
- Reduce the amount of *unused* features.

This is an alternative to delivering the whole project in one go - and never looking back. This iterative way of working is considered to be [*agile*](scrum-guide.md).

It is especially beneficial in context with the following problems:

- There is uncertainty in the demand from customers. This creates a risk of building the wrong product.
- There is uncertainty w.r.t the progress of the project. Any problems that arise might be discovered too late.
- There are risk associated with the duration of project. E.g. when missing a deadline would be catastrophic.

![choosing-agile](img/choosing-agile.png)



**Evaluating risk and uncertainty**

- Is the demand from customers clear?
- Is the proposal technically feasible? If not, then consider starting with experiments.
- Will progress be measurable?



### Types of Tasks

The generic concepts PoC and MVP can be applied to tasks and features. In general, smaller task are less unpredictable and have a less rework associated with them. On the other hand, lengthy tasks [incentivize](https://medium.com/hackernoon/wip-it-real-good-66aa710178fd) the use backchannels, local agenda's and contribute to a lack of overall focus.

- **Proof of concept** ([PoC](https://en.wikipedia.org/wiki/Proof_of_concept))
    Build an experimental application and learn on the way. The goal is not to develop finished end-product but rather to demonstrate feasibility and/or learn what a production-like application would entail (and gain a head-start).

- **Minimum Viable Product** ([MVP](https://en.wikipedia.org/wiki/Minimum_viable_product)): 
    Deploy a minimal feature ASAP s.t. you can collect early feedback and improve it iteratively. Maximize the amount of learning (e.g. from users/customers) with the least amount of effort. It emphasizes the value of customer-feedback is 
- **Minimum Lovable Product** (MLP): 
    Work towards a release that will overwhelm customers/end-users. In case of infrastructure this could mean an automated and sufficiently secured and monitored system.



**Types of features**
Note that features often have multiple roles, and can be sold as feature anyway.

|                | User-invisible | User-visible                                                 |
| -------------- | -------------- | ------------------------------------------------------------ |
| Positive Value | Feature        | Architecture, non-functional requirements, process improvements |
| Negative Value | Defect         | Technical debt                                               |



**Types of stories**

In general there are two types of stories, both of which add value.

- *User* stories. These are directly visible to end-users or stakeholders.
- *Tech* stories. These are important, but their value is mostly visible internally. E.g. risk mitigation.

