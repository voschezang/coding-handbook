# Quotes

Note that the validity of the following statements is dependent on certain *implicit* and *explicit* assumptions. Additionally they are biased towards software engineering.

* Everything is a theory and could be proven wrong.
* There is no such thing as absolute certainty. Even [rationality](https://en.wikipedia.org/wiki/Postmodernism) does not guarantee certainty. Pure objectivity does not exist.
* Language is fundamentally flawed and is merely a network of [signs](https://en.wikipedia.org/wiki/Simulacra_and_Simulation
    ) and [hyperlinks](https://en.wikipedia.org/wiki/Hyperreality
    ).
* Developing [models](https://en.wikipedia.org/wiki/Model) is the greatest skill.
* Mistakes are undervalued. There are a necessity for learning and they are extremely effective at creating awareness.
    * In art mistakes are celebrated, and are often the most memorable parts of a piece.
* Don't let school get in the way of your education.
    * Stop thinking in closed questions: "Is this answer correct?".
    * Too often, theories are told as absolute truths (or even laws) only to be revised years later.
* Be wary of [sunk cost](https://en.wikipedia.org/wiki/Sunk_cost), [opportunity cost](https://en.wikipedia.org/wiki/Opportunity_cost), false [dilemma's](https://en.wikipedia.org/wiki/False_dilemma), generalizations and other [fallacies](https://en.wikipedia.org/wiki/List_of_fallacies). 
* When explaining phenomena, consider [all types of causes](https://en.wikipedia.org/wiki/Four_causes) and place them in the [dimensions](https://de.wikipedia.org/wiki/Attributionstheorien) `internal-external, stable-unstable, global-local`. 
* A culture of trust has the highest [payoff](https://en.wikipedia.org/wiki/Prisoner%27s_dilemma).
* It is never *necessary* to continue after reaching a [good enough](https://en.wikipedia.org/wiki/Good_enough_parent) point.
    * Only unicorns are perfect.
* Think in possibilities rather than limitations.



**Processes**

* Effectiveness > Efficiency.
* Prioritizing too many tasks both prevents focussing and reduces the time to adjust priorities.
    * Take regular breaks. Take time to orient yourself and reflect.
    * Make room to make improvements (plan in slack).
* Change is not a solution but a process. It's a balance between relying on you [priori](https://en.wikipedia.org/wiki/A_priori_and_a_posteriori) and updating your [posterior](https://en.wikipedia.org/wiki/Posterior_probability).
  * Find an appropriate [learning rate](https://en.wikipedia.org/wiki/Learning_rate) or [step size](https://en.wikipedia.org/wiki/Gradient_descent) to avoid overshooting.
  * Define conditions under which you would change your beliefs.
* Value both processes and outcomes (e.g. [risk-adjusted returns](https://en.wikipedia.org/wiki/Risk-adjusted_return_on_capital)). 
    * Good results with bad processes have no predictive value.
* Be input-driven rather than merely output-driven. You can control the input, but the output is a side-effect.



**Time to market**

* What one person can do in nine months, nine persons can do in one month.
* Before software can be reusable it first has to be usable.
* [Mediocrity is expensive](https://twitter.com/johncutlefish/status/1398693641116258306). [7s kill companies](https://podcasts.apple.com/us/podcast/the-knowledge-project-with-shane-parrish/id990149481?i=1000525574557).




## Software Engineering

* Find the balance between proper software engineering and the hacker way.
* There is no universal, optimal ratio between `Dev + Ops` and `DevOps`. Instead allow teams to move in a direction that is optimal in a specific context.
* [Larger](https://en.wikipedia.org/wiki/Conway%27s_law) teams tend to produce larger and more complex software (and take [longer](https://en.wikipedia.org/wiki/Brooks%27s_law)).
* Scrum does not imply agile.
* Agile does not imply [scrum](https://sanderhoogendoorn.com/jack-sparrow-and-the-end-of-scrum/).
* Programming is the formalization of *human*-readable requirements and transforming them into *machine*-readable language.
* Machine learning is the art of inferring *rules* and *patterns* based on `data` and `answers`. And then predicting the future.
* Software Architecture is a discipline. Software is never [perfect](https://en.wikipedia.org/wiki/All_models_are_wrong) or [finished](https://www.youtube.com/watch?v=lY54TmmEllY) and requirements will change.
  * Design for failure; assume each component will break eventually.
* The _fourth_ problem in software engineering is [accidental](https://en.wikipedia.org/wiki/Accident_(philosophy)#Aristotle) complexity; i.e. using the wrong types of model for a given use case.
  * E.g. a certain programming paradigm / language / framework, database model or hardware model (e.g. CPU, GPU, FPGA).
* If tests are not run periodically they will start to fail over time.
* It is easier to deprecate code than to refactor it.
* Finding 5 bugs in 5 lines of code is easier than finding 1 bug in 500 lines of code. Keep pull-requests small.
* Timestamp everything.



**DevOps**

The following is applicable in a [complex domain](https://en.wikipedia.org/wiki/Cynefin_framework) (e.g. a highly dynamic market).

* DevOps is just [vertical intergration](https://en.wikipedia.org/wiki/Vertical_integration).
  * Specialization can be achieved by scoping down the product (e.g. into a microservice), and outsourcing (e.g using SaaS products).
  * This requires a fast and automated build-test-deployment process.
* Take calculated risks, experiment, make mistakes and learn from them.
  * Learn early. Goto [production](https://martinfowler.com/bliki/CanaryRelease.html?ref=wellarchitected) & collect (user-)feedback ASAP.
  * Use local discoveries to make [global improvments](https://en.wikipedia.org/wiki/Autonomation).
  * Build in slack, i.e. room to incorporate learning & improvement.
* In a complex, dynamic environment, it is better to release 1 feature than to leave 5 ones in-progress.
* Move fast, but in small steps. Be skeptic and optimistic. Take risks and learn by experimenting.
  * Take [leaps](https://en.wikipedia.org/wiki/Leap_of_faith) by exception.
* Improving daily working > daily work.



**DevOps Organizations**

* Design organizations to be [self-organizing](https://en.wikipedia.org/wiki/Self-organization) and resilient.
  * Allow for [free market dynamics](https://en.wikipedia.org/wiki/Market_mechanism) and healthy competition, but to a [limited extend](https://en.wikipedia.org/wiki/Das_Kapital).
  * Minimize the amount of regulation and bureaucracy.
  * Give teams and team-members agency such that they can experiment and innovate. Don't punish good processes with bad outcomes (but learn from them).
  * Assuming that employees are professional and act rational, any mistakes can be attributed to external factors. [Hanlon's razor](https://en.wikipedia.org/wiki/Hanlon%27s_razor) is about accidents rather than stupidity. The logical response is usually to change the environment to minimize future errors (i.e. make processes and tasks [foolproof](https://en.wikipedia.org/wiki/Poka-yoke)). 
* Multidisciplinary teams are initially less (cost-)efficient than functional teams, but make up for this by writing better and more stable software.
* Hire the most expensive experts.
* Be more than just componets (e.g. departments), be interconnected, like a community.
* Incentivize organizational [awareness](https://en.wikipedia.org/wiki/Andon_(manufacturing))

**The hacker way**

* Be goal-oriented. Focus on the most impactful tasks.
* Sprint's aren't fast enough. Don't wait for other developers to sync up and instead release multiple times per day.
  * E.g. writing a story, refining it, let it wait on backlog, waiting for product owner approval.
* Action builds resilience. Inaction feeds [doubt](https://twitter.com/ShaneAParrish/status/1392110803919179787) and uncertainty.
* Never say: "Sorry, that's out of scope".
* Reconsider all conventions. Try to hack your own systems. Always aks yourself:
  1. How can I break or abuse this?
  2. Are there other ways to do this?

**Automation & Testing**

* "If you have expert developers you don't need to waste time on unit tests."
* "Our build process is not automized because it is so complex that it requires experts to do it manually."
* "Our testing process is not automized because it is so complex that it requires experts to do it manually."
* "100% test coverage means that all possible input values are considered. This would include all `integers`."

**Unsorted**

Don't make fun of:
* People who still use hard drives.
* People who use backward slashes in paths.


## Programming languages
* Runtime errors are a language (design) choice.
* --Hit compile-- Break time.
* Just get the code to compile, so we can get to real work: debugging.
* Java is so flexible that it has neither of the advantages of a strong type system and a dynamic one (with duck typing).
* C++ has default arguments AND function overloading.
* Modern languages should be expressive and extensible. E.g. allow for partial functions, Python's `@decorator`, Elm's `Maybe.andThen`, Kotlin's dataclasses.
* Tuples should not have a length greater than 3 or 4 or 5 (otherwise use named tuples, records or maps).

