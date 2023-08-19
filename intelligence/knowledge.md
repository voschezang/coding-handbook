# Knowledge

This document discusses knowledge, truth and beliefs.

[toc]

## Domains

Science attempts to organize knowledge. It relates to the following domains.

 

💭 **Philosophy**

Philosophy is related to science. It is not strictly part of science, because it questions science itself and even our own existence and [objectivity](https://en.wikipedia.org/wiki/Objectivity_and_subjectivity) itself. 

- It also covers ethics, which is grounded on [subjective experience](https://en.wikipedia.org/wiki/Philosophical_zombie). See [personhood](https://en.wikipedia.org/wiki/Personhood).



🔨 **Engineering**

Engineering differs from science in its purpose. It's about solving problems rather than discovering truth. It involves production on top of learning. Reliability is considered sufficient, rather than seeing absolute truth.



🎨 **Art**

> L'art pour l'art.

Art differs from engineering in its purpose. It's about creation itself. It's about aesthetic and uniqueness, rather than mass-production. It can be completely [decoupled](https://en.wikipedia.org/wiki/Art_for_art%27s_sake) form any utility.



## Objectivity

> Mathematic is a convention, rather than universally true.

Knowledge is often split up into objective and subjective knowledge. The latter is dependent on the observer, which is a person with a biassed (limited) worldview. Objective knowledge is said to be independent of the observer. 

Scientific models can be interpreted as *conventions*. They are chosen out convenience, rather than universality. Science itself is supposed to be objective, but it is still guided by experimental data.

Sciences attempts to discover objective knowledge: truth. It can start with various approaches.

- A priori knowledge and [formal systems](https://en.wikipedia.org/wiki/Formal_system). Inference based on first principles (axioms). Developing a model that is internally consistent.
- Falsifiable hypotheses, repeatable experiments and peer-reviews. Incrementally update beliefs about the physical world.

Both lead to models that are *true* in certain conditions. The generality of such models may vary. Difficulties arise when multiple valid models (seemingly) conflict with each other. One example is euclidean [geometry](https://en.wikipedia.org/wiki/Geometry) and non-euclidean geometry.

A [morphism](https://en.wikipedia.org/wiki/Morphism) is a mapping between different models. The existence of a morphism for two given models "proofs" that they are both correct.

For example, see this mapping between [coordinate systems](https://en.wikipedia.org/wiki/Cartesian_coordinate_system). Both are completely valid ways to represent space.

```py
# Cartesian coordinates (x, y) to polar coordinates (r, θ)
def map(x, y):
	r = √(x² + y²)
	θ = arctan(y / x)
  return (r, θ)
```

Another example would be numeral systems. E.g. decimal digits `1,2,3`, binary digits `0, 1, 10, 11` and tally systems `I, II, III`.

In general, one could define an arbitrary number of consistent models and morphisms. One can only speculate which ones are absolutely true and which ones exists "in the real world".



## Scientific Method

> Science consists of making falsifiable predictions.

Broadly, the [scientific method](https://en.wikipedia.org/wiki/Scientific_method) consists of a prior belief, a conjecture (hypothesis), and an experiment. Specifically:

1. **Problem statement** or observation. Explore. Do research.
2. **Hypothesis**. A falsifiable prediction. Use *induction* to predict a hypothetical situation. Make a generalization based on an observation. These can range from analogies, causal inferences, syllogisms.
3. **Experiment**. Design an experiment to test the hypothesis. Use *deduction* to ensure that conclusions are valid; both in terms of syntax and semantics. This may be done with either a formal or a natural language. A inherent challenge is to maximize the likelihood `P(E | H)`.
4. **Analyze**. Observe the results and compare them to the *predicted* results. `P(H | E)`
5. **Conclude**. Draw conclusions without over-generalizing.
6. **Report** findings and share them freely. Facilitate other researchers to replicate the experiments.



There are parallels with [Bayesian inference](https://en.wikipedia.org/wiki/Bayesian_inference).

- The problem statement is the prior `P(H)`: the probability that the hypothesis `H` is true.
- The hypothesis and the experiment are the likelihood `P(X | H)`: the probability of observing the predicted result `X`, if the hypothesis would be true.
- The conclusion is the posterior `P(H | X`): the probability that the hypothesis is true, given the observation.



Challenges

- In practice, it my be impossible to proof that an hypothesis is true. Instead, a combination of experiments can be setup to disprove or reject any alternative hypothesis.
- The number of possible hypotheses is infinite. Science does not prescribe how to choose or select the right hypothesis. There is an *art* to thinking outside the box and coming up with novel hypotheses.



## Value

Facts vary in terms of value. This depends on

- Generalization. In what conditions are they true?
- Triviality or novelty. How obvious are they? How consistent are they with the status quo? 
- [Surprisal](https://en.wikipedia.org/wiki/Entropy_(information_theory)) value. How much information does it entail?

Suppose someone recorded the result of 5 coin tosses. If the head-tail ratio was balanced this would be a low-value fact. If the ratio was skewed they the value would be higher, as it provides novel information about the coin.



