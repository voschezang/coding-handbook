# Quotes

[toc]

Note that the validity of the following statements is dependent on certain *implicit* and *explicit* assumptions. Additionally they are biased towards software engineering.

* Everything is a theory and could be proven wrong.
* There is no such thing as absolute certainty. Even [rationality](https://en.wikipedia.org/wiki/Postmodernism) does not guarantee certainty. Pure objectivity does not exist.
* Language is fundamentally flawed and is merely a network of [signs](https://en.wikipedia.org/wiki/Simulacra_and_Simulation
    ) and [hyperlinks](https://en.wikipedia.org/wiki/Hyperreality
    ).
* Developing [models](https://en.wikipedia.org/wiki/Model) is the greatest skill. True genius is found in the ability to simplify.
* Mistakes are undervalued. There are a necessity for learning and they are extremely effective at creating awareness.
    * In contrast, in art mistakes are celebrated, and are often the most memorable parts of a piece.
    * Making many small mistakes (which can be controlled/rolled-back/compensated/negated) > making fewer big mistakes.
* Don't let school get in the way of your education.
    * Practice self-actualization: reaching your full potential, discovering your self and finding the meaning of life.
    * Stop thinking in closed questions: "Is this answer correct?". Rather, ask: "What are the possible answers?".
    * Too often, theories are told as absolute truths (or even laws) only to be revised years later.
* A culture of trust has the highest [payoff](https://en.wikipedia.org/wiki/Prisoner%27s_dilemma) (in contrast to e.g. retaliating strategies). 
    * It allows interaction, and the sharing of ideas. Nurture (or invest in) the positive feedback loop: `truth => trust => reputation => attraction`.
    * But do gradually reduce exposure to uncooperative participants.
* It is't necessary to continue after reaching a _good enough_ point. Perfection leads to [overfitting](https://en.wikipedia.org/wiki/Overfitting).
    * Only unicorns are perfect.
* Think in possibilities rather than limitations.
* Be wary of [sunk cost](https://en.wikipedia.org/wiki/Sunk_cost), [opportunity cost](https://en.wikipedia.org/wiki/Opportunity_cost), false [dilemma's](https://en.wikipedia.org/wiki/False_dilemma), generalizations and other [fallacies](https://en.wikipedia.org/wiki/List_of_fallacies). Cutting your losses may be more effective than optimizing your wins.
* When explaining phenomena, consider [all types of causes](https://en.wikipedia.org/wiki/Four_causes) and place them in the [dimensions](https://de.wikipedia.org/wiki/Attributionstheorien) `internal-external, stable-unstable, global-local`.
* If you don't want your product to be criticized, just give it a positive name: e.g. be *agile*, be smart, use *clean* code.
* "[Mediocrity is expensive](https://twitter.com/johncutlefish/status/1398693641116258306). [7s kill companies](https://podcasts.apple.com/us/podcast/the-knowledge-project-with-shane-parrish/id990149481?i=1000525574557) because of their opportunity cost.
* Natural developments are not inevitable.



**Processes**

* Effectiveness > Efficiency.
    * Prefer messy but effective communication over efficient silos (with tunnel vision).
* Doing the right thing > being right.
* Procedures > plans (if not overly bureaucratic). E.g. [the scientific method](https://en.wikipedia.org/wiki/Scientific_method), [PDCA](https://en.wikipedia.org/wiki/PDCA).
    * "No plan survives first contact"
* Unspoken expectations are less likely to be unambiguous than explicit ones.
* Slow down to speed up. Humans were not made for constant motion.
    * Take regular breaks. Take time to orient yourself and reflect. Take a step back to move forward.
    * Make room to make improvements (plan in slack).
    * Prioritizing too many tasks both prevents focussing and reduces the time to adjust priorities.
* Change is not a solution but a process. It's a balance between relying on you [priori](https://en.wikipedia.org/wiki/A_priori_and_a_posteriori) and updating your [posterior](https://en.wikipedia.org/wiki/Posterior_probability).
  * Find an appropriate [learning rate](https://en.wikipedia.org/wiki/Learning_rate) or [step size](https://en.wikipedia.org/wiki/Gradient_descent) to avoid overshooting.
  * Learning requires *un*learning. Define conditions under which you would change your beliefs.
* Value both processes and outcomes (e.g. [risk-adjusted returns](https://en.wikipedia.org/wiki/Risk-adjusted_return_on_capital)). 
    * Good results with bad processes have no predictive value.
* Be input-driven rather than merely output-driven. You can control the input, but the output is a side-effect.
* If the postmortem (or RCA) results in in one mistake, then the postmortem was wrong. I.e. if there was a single point of failure then that was the problem.



**Time to market**

* Deliver sooner, not faster. Velocity > speed.
* Being busy indicates a lack or prioritization.
    * Subtract to add. [Narrow](https://en.wikipedia.org/wiki/Scope_creep) your focus.
    * Say no to *good* opportunities s.t. you can focus on those rare, *great* opportunities.
* Don't jump from problems to solutions. First find the underlying causes.
* Training can be defined as "practice by doing", but at a much slower pace. It shouldn't be rushed.
* Before software can be reusable it first has to be usable.
* "What one person can do in nine months, nine persons can do in one month."
* [Solve via iteration](https://www.instagram.com/p/CP_70ppLAYC/), then get paid by repetition (scale up).
* Adding security to software after its been made is like [adding electricity and running water to a 1000 year old castle](https://twitter.com/jackrhysider/status/1453728265244315658)




## Software Engineering

* Find the balance between proper software engineering and the hacker way.
* Programming is the formalization of *human*-readable requirements and transforming them into *machine*-readable language.
* Machine learning is the art of inferring *rules* and *patterns* based on `data` and `answers`. And then predicting the future.
* Software Architecture is a discipline. Software is never [perfect](https://en.wikipedia.org/wiki/All_models_are_wrong) or [finished](https://www.youtube.com/watch?v=lY54TmmEllY) and requirements will change.
  * Design for failure. Assume each component will break eventually.
  * Design for change. Don't assume requirements will be constant.
* The _fourth_ problem in software engineering is [accidental](https://en.wikipedia.org/wiki/Accident_(philosophy)#Aristotle) complexity; i.e. using the wrong types of model for a given use case.
  * E.g. a certain programming paradigm / language / framework, database model or hardware model (e.g. CPU, GPU, FPGA)
* If tests are not run periodically they will start to fail over time.
* Not all technical debt has to be [paid off](https://www.martinfowler.com/bliki/TechnicalDebt.html); sometimes code can be simply deprecated.
* Assign owners/requestors to *requirements*. Who want this? Is it still relevant?
* Timestamp everything.
* Laziness incentivizes [innovation](https://en.wikipedia.org/wiki/Automation).
* Using [branches](https://en.wikipedia.org/wiki/Branching_(version_control)) defers integration. The average age of branches is inversely related to the [continuity](https://en.wikipedia.org/wiki/Continuous_integration) of integration.
* Choosing the right methodology < being able to adjust & experiment (as a team)
    * If your theoretically sound methodology is not working, then switching to an entirely new method will not help you. Instead learn to adjust and experiment.



### Collaboration

* There is no universal, optimal ratio between `Dev + Ops` and `DevOps`.  Instead allow teams to move in a direction that is optimal in a specific context.
* Parallelization of work is easy (silos), but working together is hard.
* [Larger](https://en.wikipedia.org/wiki/Conway%27s_law) teams tend to produce larger and more complex software (and take [longer](https://en.wikipedia.org/wiki/Brooks%27s_law)).
* Scrum does not imply agile.
* Agile does not imply [scrum](https://sanderhoogendoorn.com/jack-sparrow-and-the-end-of-scrum/).
* Success in scum involves [more](https://twitter.com/ronjeffries/status/1460048015549509633) than that what's in the scrum guide.
* Finding 5 bugs in 5 lines of code is easier than finding 1 bug in 500 lines of code. Keep pull-requests small.
* A high level of trust (between team members) is required in order to do effective pairing.
* Pairing is useful, but you can't expect everyone to use it to the same extend.
* Refinement of stories is a type of risk mitigation, where the upfront cost is independent of the materialization of risks. Hence in many cases it may feel unnecessary.
* Retrospectives are useless if you don't want to change



### DevOps

The following is applicable in a [complex domain](https://en.wikipedia.org/wiki/Cynefin_framework) (e.g. a highly dynamic market).

* DevOps is just [vertical integration](https://en.wikipedia.org/wiki/Vertical_integration). You build it, you run it.
  * Specialization can be achieved by scoping down the product (e.g. into a microservice), and outsourcing (e.g using SaaS products).
  * This requires a fast and automated build-test-deployment process. Be able to deploy 100 times per day.
* Maximize productivity by minimizing lead time per task/item.
    * Strive for a stable one-by-one production flow (small batches).
        * This is more *agile* than increasing parallelization and batch sizes.
        * Remove any bottlenecks that stand in the way of this vision.
        * Finish the current tasks before starting new ones.
    * Minimize the number of batching steps and minimize waste in between. Optimize the process such that it requires minimal inventory.
    * Measure and visualize both lead-time and lead-time-per-task.
* Take calculated risks, experiment, make mistakes (notice mistakes) and learn from them.
  * Learn early. Goto [production](https://martinfowler.com/bliki/CanaryRelease.html?ref=wellarchitected) & collect (user-)feedback ASAP. Failure enables success.
  * Use local discoveries to make [global improvements](https://en.wikipedia.org/wiki/Autonomation).
  * Build in slack, i.e. room to incorporate learning & improvement.
  * Focus on a single experiment at a time, to minimize outcome ambiguity (e.g. when inferring causality).
  * Risk-free projects are unworthy. Run towards risk.
* Design (processes) for failure.
    * Assume that all people will make mistakes and act foolish eventually.
    * Change the environment to minimize potential errors (i.e. make processes and tasks [foolproof](https://en.wikipedia.org/wiki/Poka-yoke)).
    * "Let it crash". Fail fast, but in a controlled way (e.g. using circuit breakers and compartmentalization). Make failure visible instead of suppressing it. Don't let problems accumulate to a [critical state](https://en.wikipedia.org/wiki/Critical_phenomena). This prevents [cascading](https://en.wikipedia.org/wiki/Cascading_failure) failures.
* Releasing a single feature is preferred over to leaving 5 ones in-progress.
* Defer impactful decisions if they are uncertain.
    * Use small decisions as experiments.
    * Put new code behind feature flags and use canary deployments.
* Prefer automation (and alternatives) over formal processes and contracts (e.g. in risk management).
    * If it's risky then do it more often. This forces one to address issues.
    * If it's difficult then do it more often. Practice.
* Move fast, but in small steps. Be skeptic and optimistic. Take risks and learn by experimenting.
  * Take [leaps](https://en.wikipedia.org/wiki/Leap_of_faith) by exception.
  * Ideally change one thing at the same time (in a team) so you can study the results and possibly infer causality. This is also an incentive to move faster and finish tasks.
* Improving daily working > daily work. Improve processes instead of optimizing goals.
* Rely on read-only afternoons and Fridays. Do deployments and releases during weekends.



### DevOps Organizations

* Design organizations to be [self-organizing](https://en.wikipedia.org/wiki/Self-organization) and resilient.
  * Minimize the amount of regulation and bureaucracy. Time spend on filling out forms is a waste.
* Build a community.
    * Be more than just components (e.g. departments), be interconnected.
    * Embrace communal learning. Learn for the sake of learning. This includes teaching.
    * Incentivize organizational [awareness](https://en.wikipedia.org/wiki/Andon_(manufacturing)).
* Improvement and innovation should be done both top-down and bottom-up.
    * Give teams and team-members agency such that they can experiment and innovate. Don't punish good processes with bad outcomes (but learn from them).
* Multidisciplinary teams are initially less (cost-)efficient than functional teams, but make up for this by writing better and more stable software.
* Assuming that employees are professional and act rationally, most mistakes can be attributed to external factors. Explain events with self-interest, then [stupidity](https://en.wikipedia.org/wiki/Hanlon%27s_razor), and only then malice.
* Hire the most expensive experts.
    * Hiring people for the short term incentivizes them to find short term solutions.



### The hacker way

* Be goal-oriented. Focus on the most impactful tasks.
* Sprint's aren't fast enough. Don't wait for other developers to sync up and instead release multiple times per day.
  * E.g. writing a story, refining it, let it wait on backlog, waiting for approval.
* Action builds resilience. Inaction feeds [doubt](https://twitter.com/ShaneAParrish/status/1392110803919179787) and uncertainty.
* Always ask "Why?". Ought and Musts aren't valid reasons.
    * Never say: "Sorry, that's out of scope".
* Reconsider all conventions. Try to hack your own systems. Always aks yourself:
  1. How can I break or abuse this?
  2. Are there other ways to do this?




## Programming languages
* Runtime errors are a language (design) choice.
* Unlinke Java, C is fast.
* Unlike Java, Python is user-friendly.
* Java is so flexible that it has neither of the advantages of a strong type system and a dynamic one (with duck typing).
* C++ has default arguments AND function overloading.
* Modern languages should be expressive and extensible. E.g. allow for partial functions, Python's `@decorator`, Elm's `Maybe.andThen`, Kotlin's dataclasses.
