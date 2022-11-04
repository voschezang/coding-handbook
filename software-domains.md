## Software Domains

Any specific system usually has a balance between domain-oriented components and generic (facilitating) components.

An application usually relies on libraries and [SaaS](https://en.wikipedia.org/wiki/Software_as_a_service), [PaaS](https://en.wikipedia.org/wiki/Platform_as_a_service) or [IaaS](https://en.wikipedia.org/wiki/Infrastructure_as_a_service) components.

**Types**

- Hardware type: CPU, GPU, FPGA
- Hardware context: embedded, desktop, mobile, web, web-app
- Application Development (individual components)
- Application Architecture: e.g. a distributed monolith
- System Architecture: e.g. microservices
- Infrastructure (within a datacenter or using multiple datacenters)

Software can be managed at different **levels**.

- **Platform**/internal technology: this should usually be stable.
- **Product**: deliver value to customers.
- **Process**: complement the above by continuously improving.
- **People**: from personal well-being (of colleagues and teams), to maximizing potential.

## Related Domains

Similar to these [architectural pattern examples](https://en.wikipedia.org/wiki/Architectural_pattern#Examples).

| Fundamental Theory                                           | Emergent Theory                                              | Applied to a domain                                          | Applied to the real world                                    |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Math/Logic                                                   | Statistics                                                   | Data Science                                                 | Data Engineering                                             |
| Graph Theory,<br />Information Theory                        | Network Science                                              | Computer Networks,<br />Social networks                      | Telecommunications network                                   |
| Information Theory,<br />Computability                       | Cryptography                                                 | InfoSec                                                      | Application, Computer, Network Security                      |
| Mathematical models,<br />Queueing theory                    | Mathematical optimization                                    | Operations research                                          | Industrial engineering,<br />Scheduling,<br />Supply chain management,<br />ERP, CRM, BI, HR systems |
| Mathematical Optimization,<br />Numerical analysis           | Parallel Programming                                         | Optimization                                                 | High-performance computing                                   |
| Computational Models<br />(E.g. λ-calculus)                  | Programming Patterns<br />Enterprise Integration Patterns    | Programming Paradigms                                        | Programming Languages,<br />OOP Design Patterns              |
| Mathematical (formal) logic<br />*(e.g. set theory)*,<br />Computational Models <br />(*e.g. λ-calculus*) | Computational Complexity,<br />Computability                 | <u>Programming</u> Paradigms<br />(*e.g. FP, OOP*)           | Programming Languages<br />(*e.g. C, Java*)                  |
| [Communication Patterns](communication-patterns.md)          | [Programming Patterns](programming-patterns.md)              | <u>Enterprise</u> Integration Patterns,<br /><u>OOP</u> Design Pattern | [Programming Paradigms](programming-paradigms.md)            |
| Systems Theory                                               | System Design                                                | *(Design of)* [Organizations](organization-structure.md)     | Business administration,<br />Enterprise application integration,<br />Enterprise architecture |
| Systems Theory                                               | System Design                                                | <u>Software</u> Design                                       | [DDD](domain-driven-design.md)                               |
| ?                                                            | [Requirements Engineering](requirements-engineering.md),<br />[Systems Management](systems-management.md),<br />Goal Setting | [Management Principles](management-principles)<br />[Goals/Planning/Strategy](goals-planning-strategy.md) | [Product Management](product-management),<br />[Project Management](project-management),<br />Business Operations |

<table>
<thead><tr><th>Fundamental Theory</th><th>Emergent Theory</th><th>Applied to a domain</th><th>Applied to the real world</th></tr></thead>
<tbody>
  <tr>
    <td rowspan="1" style="background:#efefef;">Mathematical Optimization</td>
    <td rowspan="2" style="background:#efefef;">Parallel Programming</td>
    <td rowspan="2" style="background:#efefef;">"Optimization"</td>
    <td rowspan="2" style="background:#efefef;">High-performance computing</td>
  </tr>
  <tr>
    <td rowspan="1" style="background:#ddd;">Numerical analysis</td>
  </tr>
  <tr>
    <td rowspan="2">Computational Models. E.g. lambda calculus</td>
    <td rowspan="1">Programming Patterns</td>
    <td rowspan="2">Programming Paradigms</td>
    <td rowspan="1">Programming Languages</td>
  </tr>
  <tr>
    <td rowspan="1">Enterprise Integration Patterns</td>
    <td rowspan="1">OOP Design Patterns</td>
  </tr>
  <tr>
    <td rowspan="2" style="background:#efefef;">Systems Theory</td>
    <td rowspan="2" style="background:#efefef;">System Design</td>
    <td rowspan="1" style="background:#efefef;">(Design of) Organizations</td>
    <td rowspan="1" style="background:#efefef;">Business administration</td>
  </tr>
  <tr>
    <td rowspan="1" style="background:#ddd;">Software Design</td>
    <td rowspan="1" style="background:#ddd;">Domain-Driven Design</td>
  </tr>
</tbody>
</table>
