

# Modelling

Principles of modeling, statistics and machine learning. Note that a model can be either mathematical or conceptual (e.g. a flowchart).

- [All models are wrong](https://en.wikipedia.org/wiki/All_models_are_wrong). A model is never equal to reality.
    - The real world can only be explained by multiplicity of models.
    - Multiple models can be correct; they may provided different perspectives of the same phenomena.
- Good models have clear boundaries.
- There is no [free lunch](https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff); making models specific to 1 dataset decreases the performance on all others (i.e. generalization).
- 
    - Minimize the number of [assumptions](https://en.wikipedia.org/wiki/Occam%27s_razor) in a model. Simplicity is the greatest sophistication.
    - Distinguish between [systematic & random](https://en.wikipedia.org/wiki/Observational_error#Random_errors_versus_systematic_errors) errors. And between [sensitivity & specificity](https://en.wikipedia.org/wiki/Sensitivity_and_specificity).
- Generalization gap: performance on a test set is always worse than performance on the training set.
- Garbage in, garbage out: designing models requires reliable data.
- There is a difference between [validation & verification](https://en.wikipedia.org/wiki/Verification_and_validation).
- Optima can be global or [local](https://en.wikipedia.org/wiki/Saddle_point).



**Analogies vs. First Principles**

- If an event is observed frequently, then analogies can help.
- If a process is novel, but the inner process is understood, then it can be beneficial to start with fundamentals.



## Learning

> Learning revolves around revising your opinions.

Experiments not require complex setups. Start simple and expand if necessary. Three types:

1. Learn by observation. Then reflect on the observations.
2. Iterate. Change a single  variable and measure the result. Then repeat.
3. A/B Testing. 
    1. Replicate multiple environments. 
    2. Change one of them and use the other one as a baseline.
    3. Compare the results.



See [learning](learning.md).



### Sources

> With false assumptions, any idea can be sold.

Distinguish between the inside view and the [outside view](https://buttondown.email/hillelwayne/archive/the-outside-view/). Evaluate the idea first from the outside view perspective, and use that as a consideration (limitation) of the validity of any internal claims.

- Outside view: without going into details, is the source credible?
    - Is it a radical idea, or conforming to consensus?
    - Is the source a single entity, or a multiplicity? Is it dogmatic?
    - Is the scope of the idea well-defined, or is the idea applied to various domains, without a firm grounding (racing thoughts)?
    - Is there an "enemy view"? Is there an obsession over categorization of alternative ideas?
        - Are both the advantages and disadvantages considered? Is there a tradeoff or is the idea an absolute?
    - Is the channel of communication reliable? Public? Can others criticize the idea openly?
    - Is the method of communication suitable? Does the source have honest intent?
- Inside view: go in depth.
    - Are the assumptions valid?
    - Given the assumptions of the source, does the story make sense?



## Evolution

This concerns evolution in the theoretical sense. Evolution can be defined as iterative improvement by granular steps. This can be used in mathematical optimization, but it can also be used to explain behaviour of successful organizations, apps, or [memes](https://en.wikipedia.org/wiki/Memetics).

The evaluation of states is done using an [*objective*](https://en.wikipedia.org/wiki/Loss_function) (e.g. *fitness, loss, utility, reward*, *stock price*).

```python
for each point in time:
	1. copy the initial state(s)
  2. mutate each copy
  3. select the best copy as the next initial state
```

This assumes a non-convex learning landscape (otherwise simpler methods such as [gradient descent](https://en.wikipedia.org/wiki/Gradient_descent) can be used).

The  [learning rate](https://en.wikipedia.org/wiki/Learning_rate) controls the size and frequency of mutations. In a complex learning landscape, a low learning rate will cause the population to get stuck in a local optimum, but a high learning rate may result in overshooting. A common strategy is to [decrease](https://en.wikipedia.org/wiki/Simulated_annealing) the learning rate over time.

