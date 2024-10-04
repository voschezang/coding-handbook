# Mathematical models

See [modelling](../intelligence/modelling.md).

[toc]

## Spectra & Dimensions

Values can be:

- Singular. E.g. `nothing`.
  
- Discrete: Binary or categorical. E.g. `left` or `right`.
  
- Continuous. E.g. [real numbers](https://en.wikipedia.org/wiki/Real_number).



<img src="../img/models-categories.png" alt="models-categories" style="width:70%;" />



| Type          | Question                                                     | Action                      |
| ------------- | ------------------------------------------------------------ | --------------------------- |
| *Unity*       | What happens in a different perspective?                     | Change the perspective.     |
| *Binary*      | [What if](https://en.wikipedia.org/wiki/Mu_(negative)) neither option is applicable? | Refine boundary conditions. |
| *Categorical* | What sits between categories?                                | Find intermediate steps.    |
| *Continuous*  | What are the limits? What affects the function?              | Reflect.                    |



Questionioning dimensions

- E.g. focus on X or de-focus. 
- E.g. in organizations: focussing on specialization (efficiency) vs focussing on features (quality) vs focussing on simplicity.



**From binary to categorical**

<img src="../img/binary-category.png" alt="binary-category" style="width:30%;" />

**Independent or dependent dimensions**

Tradeoffs of independent dimensions

<img src="../img/dimensions.png" alt="dimensions" style="width:80%;" />



**Correlation**

Values may span over multiple dimensions. Dimensions may be correlated or uncorrelated. E.g.

- The *performance* of an algorithm may be correlated to *complexity*.
- *Messiness* can be correlated to *creativeness*.



A set of particles can be discretized over space, and transformed into a density function.

<img src="../img/particles-discretize-density.png" alt="particles-discretize-density" style="width:40em;" />

Alternatively, particles can be grouped into clusters.

<img src="../img/particles-experssion-assemblage.png" alt="particles-experssion-assemblage" style="width:55em;" />

### Junctions

Options

1. Continue as planned. Optimize.
2. Deviate or expand. Diversify.
3. Do something radically different

<img src="../img/junction-change-deviate-rest.png" alt="junction-change-deviate-rest" style="height:250px;" />

## Distributions (Statistics)

**Statistics**

Three fundamental probability distributions.

1. Uniform. E.g. the result of flipping a fair coin or a roll of a fair dice.
2. A bell curve. The average of averages [follows](https://en.wikipedia.org/wiki/Central_limit_theorem) a normal distribution.
3. A [power law](https://en.wikipedia.org/wiki/Pareto_distribution), where 80% of the results are caused by 20% of the participants.
    - Or, 10% of the results [outweigh](https://en.wikipedia.org/wiki/Sturgeon's_law) the other 90%.

Many probabilistic processes are [ergodic](https://en.wikipedia.org/wiki/Ergodicity); i.e. *time* average = *ensemble* average. Equality may not hold for higher-order moments.

- In such processes, anything that can happen [will happen](https://en.wikipedia.org/wiki/Murphy's_law) (eventually).

**Equilibria**

Long-term stable distributions (but not necessarily without tension).

- Uniform, 50-50. Equally sized components. Typically self-organizing, but up to a certain boundary. A large deviation may disrupt the balance.
- Skewed: majority-minority. E.g. Microsoft and Apple market shares.
  - Size-effects make it difficult for the majority party to conquer the whole.

## Growth

Growth of populations.

- Linear: constant increase in size.
- Exponential: relative increase in size.
- Hyperbolic: nonlinear increase in size.
- Logistic: diminishing returns.

![plot-ODE-growth](../img/plot-ODE-growth.png)

**Compounding**

Exponential growth can result in strong compounding.

- This shows how powerful continuous improvement can be.

![plot-compounding](../img/plot-compounding.png)

### Queueing Theory

**Terminology**

Utilization is the relative amount of time that a resource is busy (i.e. not idle). Variability is the variance in service time of a specific component.

**Theories**

[Little's law](https://en.wikipedia.org/wiki/Little's_law) states that for a stationary system, the long-term average:

> Mean lead time =  number of items in the system / mean arrival rate (of items)

[Kingma's formula](https://en.wikipedia.org/wiki/Kingman's_formula) predicts that given certain constraints, full system utilization results in infinite lead time.

## Game Theory

Interaction of rational agents.

In the real world, agents are always constrained.

- Bounded rationality: asymmetric information causes agents to act sub-optimally.
- Limited influence over environment.



### Karma

> What you do comes back.

The following derivation explains effects of karma in certain environments.

1. Propositions.
   1. Actions have consequences
   2. People repeat what they observe
2. Together, these result in an accumulations of consequences.
3. Consequences range from good to bad. Some are *universally* good (beneficial), some are universally bad (malicious).
4. Actions with such consequences make the same consequences more likely.



Sidenote: the existence of universal good is controversial.



## Entropy

![plot-entropy-complexity](../img/plot-entropy-complexity.png)

## Series

**Statistics**
A random variable (r.v.) `X` can be approximated in several levels of detail, which are called *moments*.

0. [Mean](https://en.wikipedia.org/wiki/Mean) or [expected value](https://en.wikipedia.org/wiki/Expected_value). `E[X]`
1. [Variance](https://en.wikipedia.org/wiki/Variance). `Var[X]`. See also [covariance](https://en.wikipedia.org/wiki/Covariance).
2. [Skewness](https://en.wikipedia.org/wiki/Skewness) or asymmetry.
3. [Kurtosis](https://en.wikipedia.org/wiki/Kurtosis) or tailed-ness.

**Taylor Series**
[Taylor series](https://en.wikipedia.org/wiki/Taylor_series). Knowing all higher order derivatives at a certain point `f(x)` allows you to infer the whole function `f(x+a)`.

In physics, the following terms are used:

0. **Position**. The current state of the system
1. [**Velocity**](https://en.wikipedia.org/wiki/Velocity). The change of the system over time (or space).
2. [**Acceleration**](https://en.wikipedia.org/wiki/Acceleration). How fast the system is changing.

**Fourier Series**
[Fourier series](https://en.wikipedia.org/wiki/Fourier_series).
