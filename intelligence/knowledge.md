# Knowledge

This document discusses knowledge, truth and beliefs.

[toc]



## Overview

Representation

- Directly, using language and [models.](modelling.md)
- Indirectly. Embedded into physical structures or behaviour. E.g. [genes](https://en.wikipedia.org/wiki/Genetics) or [rituals](https://en.wikipedia.org/wiki/Ritual).

Knowledge begins with similarity. It recognizes structures and patterns.



### Domains

Science attempts to organize knowledge. It relates to the following domains.

| Domain            | Quality (Emphasis)     | Bias                  | Artifact                    |
| ----------------- | ---------------------- | --------------------- | --------------------------- |
| Art               | Beauty                 | Imitation             | Text, paintings, sculptures |
| Engineering       | Production, usefulness | Efficiency            | Products                    |
| Humanities        | Subjectivity           | Cultural              | Stories                     |
| Philosophy        | Theoretical knowledge  | Questioning, idealism | History of philosophy       |
| (Natural) Science | Objective knowledge    | Facts, truth          | Papers                      |




 📖 **Science**

The [scientific method](https://en.wikipedia.org/wiki/Scientific_method) focusses on acquiring knowledge through experiments and publications. It consists of making falsifiable [predictions](https://en.wikipedia.org/wiki/Hypothesis) and attempts to make generalizations. It can be split up into natural, formal, social and applied science.

- It is biased towards physical objects and their measurable properties. It tends to de-emphasize subjective experience.
- Science, and especially the subject-object split has clear limits. It does not cover (moral) values. The boundary includes the following:
    - In mathematics. [Axioms of mathematics](https://en.wikipedia.org/wiki/G%C3%B6del%27s_incompleteness_theorems).
    - In physics. The [standard model](https://en.wikipedia.org/wiki/Elementary_particle) and [relativity](https://en.wikipedia.org/wiki/Theory_of_relativity). [Quantum gravity](https://en.wikipedia.org/wiki/Quantum_gravity). [Dark matter](https://en.wikipedia.org/wiki/Dark_matter).
    - Before physics. [Metaphysics](https://en.wikipedia.org/wiki/Metaphysics).
    - Subjectivity: [aesthetics](https://en.wikipedia.org/wiki/Aesthetics) and [morality](https://en.wikipedia.org/wiki/Morality).
- It does describe fundamental parts of reality incredibly accurately.
    - [Waves and particles](https://en.wikipedia.org/wiki/Wave%E2%80%93particle_duality). [Motion](https://en.wikipedia.org/wiki/Motion). [Thermodynamics](https://en.wikipedia.org/wiki/Thermodynamics).
    - [Forces of nature](https://en.wikipedia.org/wiki/Fundamental_interaction).
    - [Mathematics](https://en.wikipedia.org/wiki/Mathematics): [Logic](https://en.wikipedia.org/wiki/Logic), [statistics](https://en.wikipedia.org/wiki/Statistics).




💭 **Philosophy**

Philosophy is related to science. It is not strictly part of science, because it questions science itself and even our own existence and [objectivity](https://en.wikipedia.org/wiki/Objectivity_and_subjectivity) itself. 

- It also covers ethics, which is grounded on [subjective experience](https://en.wikipedia.org/wiki/Philosophical_zombie). See [personhood](https://en.wikipedia.org/wiki/Personhood).

> Philosophy is fundamentally destabilizing.

This is unlike science, which attempts to provide structure and predictability.



🔨 **Engineering**

Engineering differs from science in its purpose. It's about solving problems rather than discovering truth. It involves production on top of learning. Reliability is considered sufficient, rather than seeing absolute truth.



🎨 **Art**

> L'art pour l'art.

Art differs from engineering in its purpose. It's about creation itself. It's about aesthetic and uniqueness, rather than mass-production. It can be completely [decoupled](https://en.wikipedia.org/wiki/Art_for_art%27s_sake) form any utility. It focusses on value, rather than objects.



❤️ **Humanities**

Explore the human condition: experience and beliefs. Language, culture and society.



## Objectivity

> Mathematic is a convention, rather than universally true.

Knowledge is often split up into objective and subjective knowledge. The latter is dependent on the observer, which is a person with a biassed (limited) worldview. Objective knowledge is said to be independent of the observer. 

Scientific models can be interpreted as *conventions*. They are chosen out convenience, rather than universality. Science itself is supposed to be objective, but it is still guided by experimental data.

Sciences attempts to discover objective knowledge: truth. It can start with various approaches.

- A priori knowledge and [formal systems](https://en.wikipedia.org/wiki/Formal_system). Inference based on first principles (axioms). Developing a model that is internally consistent. See [specification](https://en.wikipedia.org/wiki/Algebraic_specification).
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



**Semantics**

[Syntax](https://en.wikipedia.org/wiki/Syntax) does not imply [semantics](https://en.wikipedia.org/wiki/Semantics). It is possible to define a coherent model without any relation the "real" world.

In software development this implies that the meaning of domain code is defined externally.



### Statements & Facts

Statements consist of the following.

- A couple of *things* `a, b` (i.e. objects), of *types* `A, B`.
- A *relation* between them. E.g. `a ∝ b`.
- A context `Γ` under which the statement is made.

The **value** of a statement depends on the following.

- Truthfulness. An objective lens.
    - Claimed objectiveness. Is the statement necessarily true?
        - A *fact* is a statement that is claimed to be true.

    - Generalization. In what conditions is the statement applicable?
- Usefulness. A subjective lens.
    - How useful is this statement, to a subject?
- News. The relation between other (previous) statements.
    - Triviality or novelty. How obvious are they? *"Eureka!"*
    - Plausibility. How consistent are they with the status quo? Does it conform to to the cultural scheme? *"That's insane!"*
    - [Surprisal](https://en.wikipedia.org/wiki/Entropy_(information_theory)) value. How much information does it entail? *"Unbelievable!"*


Suppose someone recorded the result of 5 coin tosses. If the head-tail ratio was balanced this would be a low-value fact. If the ratio was skewed they the value of this fact would be higher, as it provides novel information about the coin.

The **meaning** of a statement is oriented towards a subject. It relates the statements to the experience of a subject.

- *Syntax* is the internal structure of a language or statement. Ideally it is consistent.

- *Semantics* is the meaning of a statement. It maps it to an external world (w.rt. the language). E.g. the world as it is experienced by subjects.



#### Generalization Levels

> Everywhere in the universe ≠ in every universe.

From generic to specific.

1. Eternal. In every universe.
2. Universal. In this whole universe.
3. General. In principe/theory.
4. Typical. The majority of cases that are expected to be observed.
5. Often. Multiple times.
6. Sometimes.
7. In this case.



### Deconstruction

A few typical ways to 

- Reductionism or classicism. Decompose (understand) objects in terms of (atomic) components. Focus on the objective/real world: scientific properties.
    - The tendency to break down structures may create a bias for oversimplification and tunnel vision. E.g. exclude non-material properties.

- Romanticism. Appreciate objects in relation to their environment. Emphasize subjectivity. Go beyond science.



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

