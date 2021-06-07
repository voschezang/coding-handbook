# Quotes

Note that the validity of all statements is dependent on certain implicit or explicit assumptions.

* Effectiveness > efficiency.
* A culture of trust has the highest [payoff](https://en.wikipedia.org/wiki/Prisoner%27s_dilemma).
* Value both processes and outcomes (e.g. [risk-adjusted returns](https://en.wikipedia.org/wiki/Risk-adjusted_return_on_capital)). Good results with bad processes have no predictive value.
* Change is not a solution but a process. It's a balance between relying on you [priori](https://en.wikipedia.org/wiki/A_priori_and_a_posteriori) and updating your [posterior](https://en.wikipedia.org/wiki/Posterior_probability).
  * Find an appropriate [learning rate](https://en.wikipedia.org/wiki/Learning_rate) or [step size](https://en.wikipedia.org/wiki/Gradient_descent) to avoid overshooting.
  * Define conditions under which you would change your beliefs.
* Everything is a theory and could be proven wrong.


## Time to market

* What one person can do in nine months, nine persons can do in one month.
* Before software can be reusable it first has to be usable.
* [Mediocrity is expensive](https://twitter.com/johncutlefish/status/1398693641116258306).


## Software Engineering

* Find the balance between proper software engineering and the hacker way.
* [Larger](https://en.wikipedia.org/wiki/Conway%27s_law) teams tend to produce larger and more complex software (and take [longer](https://en.wikipedia.org/wiki/Brooks%27s_law)).
* Scrum does not imply agile.
* Agile does not imply [scrum](https://sanderhoogendoorn.com/jack-sparrow-and-the-end-of-scrum/).
* Finding 5 bugs in 5 lines of code is easier than finding 1 bug in 500 lines of code. Keep pull-requests small.
* It is easier to deprecate code than to refactor it.
* Timestamp everything.
* Design for failure; assume each component will break eventually.
* The _fourth_ problem in software engineering is [accidental](https://en.wikipedia.org/wiki/Accident_(philosophy)#Aristotle) complexity; i.e. using the wrong types of model for a given use case.
  * E.g. a certain programming paradigm / language / framework, database model or hardware model (e.g. CPU, GPU, FPGA).
* Software Architecture is a discipline. Software is never [perfect](https://en.wikipedia.org/wiki/All_models_are_wrong) or [finished](https://www.youtube.com/watch?v=lY54TmmEllY) and requirements will change.

<hr>

### DevOps

The following is applicable in a [complex domain](https://en.wikipedia.org/wiki/Cynefin_framework) (e.g. a highly dynamic market).

* DevOps is just [vertical intergration](https://en.wikipedia.org/wiki/Vertical_integration).
  * Specialization can be achieved by scoping down the product (e.g. into a microservice), and outsourcing (e.g using SaaS products).
  * This requires a fast and automated build-test-deployment process.
* Take calculated risks, experiment, make mistakes and learn from them.
  * Learn early. Goto [production](https://martinfowler.com/bliki/CanaryRelease.html?ref=wellarchitected) & collect (user-)feedback ASAP.
  * Use local discoveries to make [global improvments](https://en.wikipedia.org/wiki/Autonomation).
  * Build in slack, i.e. room to incorporate learning & improvement.
* In a complex, dynamic environment, it is better to release 1 feature than to leave 5 ones in-progress.
* Move fast, but in small steps. Be skeptic and optimistic. Take risks and learn by experienting.
  * Take [leaps](https://en.wikipedia.org/wiki/Leap_of_faith) by exception.


### DevOps Organizations

* Design organizations to be [self-organizing](https://en.wikipedia.org/wiki/Self-organization) and resilient.
  * Allow for [free market dynamics](https://en.wikipedia.org/wiki/Market_mechanism) and healthy competition, but to a [limited extend](https://en.wikipedia.org/wiki/Das_Kapital).
  * Minimize the amount of regulation and bureaucracy.
  * Give teams and team-members agency such that they can experiment and innovate. Don't punnish good processes with bad outcomes (but learn from them).
* Hire the most expensive experts.
* Be more than just componets (e.g. departments), be interconnected, like a community.
* Incentivize organizational [awareness](https://en.wikipedia.org/wiki/Andon_(manufacturing))


### The hacker way

* Be goal-oriented. Focus on the most impactful tasks.
* Sprint's aren't fast enough. Don't wait for other developers to sync up and instead release multiple times per day.
  * E.g. writing a story, refining it, let it wait on backlog, waiting for product owner approval.
* Action builds resilience. Inaction feeds [doubt](https://twitter.com/ShaneAParrish/status/1392110803919179787) and uncertainty.
* Never say: "Sorry, that's out of scope".
* Reconsider all conventions. Try to hack your own systems. Always aks yourself:
  1. How can I break or abuse this?
  2. Are there other ways to do this?


### Automation & Testing

* "If you have expert developers you don't need to waste time on unit tests."
* "Our build process is not automized because it is so complex that it requires experts to do it manually."
* "Our testing process is not automized because it is so complex that it requires experts to do it manually."
* "100% test coverage means that all possible input values are considered. This would include all `integers`."

### Unsorted

Don't make fun of:
* People who still use hard drives.
* People who use backward slashes in paths.


<hr>

## Programming languages
* Runtime errors are a language (design) choice.
* --Hit compile-- Break time.
* Just get the code to compile, so we can get to real work: debugging.
* Java is so flexible that it has neither of the advantages of a strong type system and a dynamic one (with duck typing).
* C++ has default arguments AND function overloading.
* Design patterns should be expressible on the language level. E.g. partial functions, Python's `@decorator`, Elm's `Maybe.andThen`.
* Tuples should not have a length greater than 3 or 4 or 5 (otherwise use named tuples / records / maps).

