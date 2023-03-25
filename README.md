# Coding Handbook

This is a collection of guidelines and ideas related to software engineering and computer science. It is not meant to be a complete or exhaustive overview.

**Table of Contents**

Programming Languages & Software Design.

- [Style Guide](style-guide.md) - a prescriptive guide for programming (low level).
- [Programming Patterns](programming-patterns.md) - common programming, application and system architecture patterns. This builds upon  [communication patterns](communication-patterns.md).
  - [Functional Programming Patterns](programming-patterns-functional.md) - mathematical and functional programming patterns.
  - [Programming Paradigms](programming-paradigms.md) - a comparison of OOP and FP.

Theoretical computer science

- [Domain-Driven-Design](domain-driven-design.md) - examples of DDD using OOP and FP.
- [Language Specification](language-spec.md) - this can be implemented as a library or a new language.
- [Functions and Relationships](functions-relations.md) - mathematical ones.

Software Industry

- [Quotes](quotes.md) - to contemplate (high level).
- [Organization Architecture](organization-architecture.md) - tradeoffs encountered in organizations.
- [Software Engineering](software-engineering.md) - what is involves.

Systems theory

- [Systems Management](systems-management.md) - systems thinking.
- [Communication Patterns](communication-patterns.md) abstract theory regarding messaging.

Management & Organizations

- [Management Principles](management-principles.md) - a collection of domain-agnostic theories.
  - [Organization Structure](organization-structure.md) - not just application architecture.
- Project Management & Planning

  - [Goals/Planning/Strategy](goals-planning-strategy.md) - choosing goals and strategies.
  - [Product Management](product-management.md) - handling *multiple* projects.
  - [Project Management](project-management.md) - handling a *single* project.
  - [Requirements Engineering](requirements-engineering.md) - handling a *unit* of work within a project.

Other

- [Behaviour](behaviour.md) - *generic* ideas, *specific* to human behaviour.
- [Modeling](modeling.md) - theory about models.
- [Learning](learning.md) - theory about change and improvement.
- [Communication Principles](communication-principles.md) - human communication.
- [Retrospective](retrospective.md) - reflection exercises for groups.



**Relations between documents**

From abstract theory to application within a domain. For a full overview, see [this table](software-domains-table.md).

- [Communication Patterns](communication-patterns.md) > [Programming Patterns](programming-patterns.md) > [Programming Paradigms](programming-paradigms.md)
- [Requirements Engineering](requirements-engineering.md) > [Project Management](project-management.md)
- [Systems Management](systems-management.md) > [Organization Structure](organization-structure.md) > [Organization Architecture](organization-architecture.md)
- [Management Principles](management-principles.md) > (management of)  [Systems](systems-management.md) > a [Product](product-management.md) > a [Platform](platform-management) > a [Project](project-management.md)



**Perspective & Generalizability of Guidelines**

[Source](https://twitter.com/johncutlefish/status/1406534814673477633)

1. **Generic** but subjective.
    - Theory, Principle, doctrine, culture.
    - Implicit, feeling, *can be sensed*.
    - Difficult to prove or falsify.
    - Applicable always and anywhere.
2. Objective but **specific**.
    - Practice, habit, skill.
    - Explicit, Concrete, *measurable*, *actionable*.
    - Provable, falsifiable.
    - Applicable to a single moment or location.

E.g. a goal can be short-term and precise, or long-term but vague.

Definition of *anti-pattern*: a commonly used, bad solution to a problem. Possibly just an indicator, signaling a deeper issue.
