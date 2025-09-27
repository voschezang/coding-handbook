# Game Theory

How to win games. See e.g. https://en.wikipedia.org/wiki/Prisoner%27s_dilemma

See also [statistics](statistics.md).



**Interaction of rational agents**

In the real world, agents are always constrained.

- Bounded rationality: asymmetric information causes agents to act sub-optimally.
- Limited influence over environment.



**Types of games**

- Winner's game. Play deliberately to score points.

- Loser's game. Avoid losing as a result of losing points.



**Types of strategies**

- Zero-sum game
- Win-win outcome



**Games**

A chess game

1. Opening game. Focus on essentials. Deploy pieces into the game. Explore areas with risk.
2. Middlegame. Improve reliability, scalability, stability, usability.
3. Endgame. Finishing touch. Improve efficiency, maintainability.



### Karma

> What you do comes back.

The following derivation explains effects of karma in certain environments.

1. Propositions.
   1. Actions have consequences
   2. People repeat what they observe
2. Together, these result in an accumulations of consequences.
3. Consequences range from good to bad. Some are *universally* good (beneficial), some are universally bad (malicious).
4. Actions with such consequences make the same consequences more likely.



Sidenote: the existence of universal good is controversial in philosophy.



## Evolution

*(This concerns evolution in the theoretical sense, rather than the biological phenomenon)*

Evolution can be defined as iterative improvement by granular steps. This can be used in mathematical optimization, but it can also be used to explain behaviour of successful organizations, apps, or [memes](https://en.wikipedia.org/wiki/Memetics).

The evaluation of states is done using an [*objective*](https://en.wikipedia.org/wiki/Loss_function) (e.g. *fitness, loss, utility, reward*, *stock price*).

```python
for each moment in time:
 1. copy the initial state
 2. mutate each copy
 3. select the best copy as the next initial state
```

This assumes a non-convex learning landscape (otherwise simpler methods such as [gradient descent](https://en.wikipedia.org/wiki/Gradient_descent) can be used).

The  [learning rate](https://en.wikipedia.org/wiki/Learning_rate) controls the size and frequency of mutations. In a complex learning landscape, a low learning rate will cause the population to get stuck in a local optimum, but a high learning rate may result in overshooting. A common strategy is to [decrease](https://en.wikipedia.org/wiki/Simulated_annealing) the learning rate over time.

