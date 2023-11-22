# Objectivity

[toc]

## Objectivity and Subjectivity

> Mathematic is a convention, rather than universally true.

Knowledge is often split up into objective and subjective knowledge. The latter is dependent on the observer, which is a person with a biassed (limited) worldview. Objective knowledge is said to be independent of the observer. 

Scientific models can be interpreted as *conventions*. They are chosen out convenience, rather than universality. Science itself is supposed to be objective, but it is guided by experimental data.

Sciences attempts to discover objective knowledge: truth. It can start with various approaches.

- A priori knowledge and [formal systems](https://en.wikipedia.org/wiki/Formal_system). Inference based on first principles (axioms). Developing a model that is internally consistent. See [specification](https://en.wikipedia.org/wiki/Algebraic_specification).
- Falsifiable hypotheses, repeatable experiments and peer-reviews. Incrementally update beliefs about the physical world.

Both lead to models that are *true* in certain conditions. The generality of such models may vary. Difficulties arise when multiple valid models (seemingly) conflict with each other. One example is euclidean [geometry](https://en.wikipedia.org/wiki/Geometry) and non-euclidean geometry.



### Morphisms

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

It is possible to define an arbitrary number of consistent models and morphisms. One can only speculate which ones are absolutely true and which ones exists "in the real world".



### Semantics

[Syntax](https://en.wikipedia.org/wiki/Syntax) does not imply [semantics](https://en.wikipedia.org/wiki/Semantics). It is possible to define a coherent model without any relation the "real" world.

In software development this implies that the meaning of domain code is defined externally.



## Statements & Facts

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



## Deconstruction

A few typical ways to deconstruct reality:

- Reductionism or classicism. Decompose (understand) objects in terms of (atomic) components. Focus on the objective/real world: scientific properties.
  
- Romanticism. Appreciate objects in relation to their environment. Emphasize subjectivity. Go beyond science.

The former has a few biasses.

- Breaking down structures may create a bias for oversimplification and tunnel vision. E.g. the exclusion of non-material properties.
- A material understanding of phenomena can kill the its beauty and the mystery that surrounds it.

