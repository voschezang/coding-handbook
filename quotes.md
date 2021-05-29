# Quotes

* Effectiveness > Efficiency. Be adaptive.
* Running > Standing Still (to stand still is to fall behind).
* A culture of trust has the highest [payoff](https://en.wikipedia.org/wiki/Prisoner%27s_dilemma)


## Time to market

* What one person can do in nine months, nine persons can do in one month.
* Before software can be reusable it first has to be usable.
* It is easier to deprecate code than to refactor it.

<hr>

## Software Engineering

* Find the balance between proper software engineering and the hacker way.
* Scrum does not imply agile.
* Agile does not imply scrum.
* [Larger](https://en.wikipedia.org/wiki/Conway%27s_law) teams tend to produce larger and more complex software (and take [longer](https://en.wikipedia.org/wiki/Brooks%27s_law)).
* Timestamp everything.
* Finding 5 bugs in 5 lines of code is easier than finding 1 bug in 500 lines of code. Keep pull-requests small.
* Design for failure; assume each component will break eventually.

### DevOps

* Take calculated risks, experiment, make mistakes and learn from them.
  * This requires an automated build/test process.
* Let's give developers admin rights on production machines.
* DevOps is just [vertical intergration](https://en.wikipedia.org/wiki/Vertical_integration).
  * Specialization can be achieved by scoping down the product (e.g. into a microservice), and outsourcing.


### DevOps Organizations

* Design organizations to be [self-organizing](https://en.wikipedia.org/wiki/Self-organization) and resilient.
  * Allow for [free market dynamics](https://en.wikipedia.org/wiki/Market_mechanism) and healthy competition, but to a [limited extend](https://en.wikipedia.org/wiki/Das_Kapital).
  * Give teams and team-members agency, such that they can experiment and innovate.
  * Minimize the amount of regulation and bureaucracy.
  * Hire the most expensive experts.
* Incentivize organizational [awareness](https://en.wikipedia.org/wiki/Andon_(manufacturing))
* Apply [Autonomation](https://en.wikipedia.org/wiki/Autonomation)


### The hacker way

* Be goal-oriented. Focus on the most impactful tasks.
* Move fast, but in small steps. Take risks and learn through experience.
 * Take [leaps](https://en.wikipedia.org/wiki/Leap_of_faith) by exception.
* Sprint's aren't fast enough. Don't wait for other developers to sync up and instead release multiple times per day.
  * E.g. writing a story, refining it, let it wait on backlog, waiting for product owner approval.
* Action builds resilience. Inaction feeds [doubt](https://twitter.com/ShaneAParrish/status/1392110803919179787) and uncertainty.
* Try to hack your own systems.
* Never say: "Sorry, that's out of scope".
* Always aks yourself:
  1. How can I break or abuse this?
  2. Are there other ways to do this?


### Automation & Testing

* "If you have expert developers you don't need to waste time on unit tests."
* "Our build process is not automized because it is so complex that it requires experts to do it manually."
* "Our testing process is not automized because it is so complex that it requires experts to do it manually."
* "100% test coverage means that all possible input values are considered. This would include all `integers`."

<hr>

## Programming languages
* Runtime errors are a language (design) choice.
* --Hit compile-- Break time.
* Just get the code to compile, so we can get to real work: debugging.
* Java is so flexible that it has neither of the advantages of a strong type system and a dynamic one (with duck typing).
* C++ has default arguments AND function overloading.
* Design patterns should be expressable on the language level. E.g. partial functions, Python's `@decorator`, Elm's `Maybe.andThen`.
* Tuples should not have a length greater than 3 or 4 or 5 (otherwise use named tuples / records / maps).
