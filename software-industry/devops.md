# DevOps

[toc]

## Purpose

The purpose of DevOps is to **deliver value sooner, safer** and **happier**. This means

- Prioritize the delivery of business value to the customer.
- Do this sooner, to avoid lagging behind changes in the environment, target market or user preferences. Avoid wasting time.
- Do this safer. Either minimize risk or make failure easier.
- Do this happier, in order to be sustainable. Build good long-term relations with stakeholders, employee, customers and users.



This works well in fast-changing contexts, e.g. [complex domains](https://en.wikipedia.org/wiki/Cynefin_Framework).



## Method & Values



### Vertical integration

> You build it, you run it.

DevOps prefers self-organizing teams. This ensures:

- Fast delivery, by being in control. Minimal dependencies on others.
- Alignment of the quality and sustainability.



> Do less

Vertical integration forces you to focus on core activities.

Specialization can be achieved by scoping down the product (e.g. into a microservice), and outsourcing (e.g using SaaS products).



> One-by-one flow

Minimize batch size and maximize lead time. This improves both efficiency and adaptability.

* Remove any bottlenecks that stand in the way of this vision.
* Finish the current tasks before starting new ones. Minimize waste.



### Quality layers

> To do things fast you need to do things well

Set *good* standards for quality. Then maximize flow while respecting these standards. Avoid perfection and [overfitting](https://en.wikipedia.org/wiki/Overfitting).

- Continuous improvement is better than delayed perfection.
- Good enough > perfect.



> Zero quality layers

Continuous testing. Build in quality from the start, rather than using quality layers. Integrate quality checks at each stage of the value chain, rather than adding a quality check at the end (when it's too late).



> Design for failure.

Assume that all people will make mistakes and act foolish eventually.

* Make failures easier. Fail fast and ensure that failure is resolved quickly.
* Change the environment to minimize potential errors (i.e. make processes and tasks [foolproof](https://en.wikipedia.org/wiki/Poka-yoke)).
* "Let it crash". Fail fast, but in a controlled way (e.g. using circuit breakers and compartmentalization). Make failure visible instead of suppressing it. Don't let problems accumulate to a [critical state](https://en.wikipedia.org/wiki/Critical_phenomena). This prevents [cascading](https://en.wikipedia.org/wiki/Cascading_failure) failures.



> If it's risky, do it more often

This forces one to address issues.

* If it's difficult then do it more often. Practice.
* If it hurts (e.g. financially), do it more often. Let the pain show.

E.g. do deployments during business hours, and make sure that this is safe.



### Automation

> Automation > formal processes

Prefer automation (and alternatives) over formal processes and contracts (e.g. in risk management).



~~Automate everything~~. Automate costly and risky processes first.



Observability. Measure and visualize both lead-time and lead-time-per-task.



## Three-step model

Based on the maturity of a DevOps team, the following stages can be followed.

1. **Flow through value chain**. Ensure that value is delivered to the customer. Be aware of the value chain.
2. **Feedback loops**. Incorporate customer feedback in order to increase value delivery and market fit.
3. **Continuous improvement**. Improve more frequently, at all stages of the value chain.



<img src="../img/flow-3-steps.png" alt="flow-3-steps" style="width:80%;" />









