# Test more effectively

This document explores ways to test more effectively.

- **Why?** Without tests, work becomes a guessing game. Testing shows you where to pay attention to. It informs your strategy.

- **Who?** Testing involves a subject: a product, person or organization. If may focus on qualities (performance) or risks (compliance).

- **Where?** It may be done online, through questionnaires or using physical experiments.



Testing is surrounded by decision making.

- *Is this product safe to use? Test it.* 
- *Should we hire this candidate? Test!*
- *Should we invest in this company? Test!*



See also [software testing](../software-industry/testing.md) [hiring](collaboration/hiring.md) and [personality](../psychology/personality.md).

[TOC]

## Overview

Testing revolves around **beliefs**. From testing if it works to learning when it will stop working. It involves two phases.

1. **Discovery**. Explore. *Unknown unknowns.* The result is a list of findings. 
2. **Checking**. Make confirmations. Verification & validation. *Known unknowns.* The result is a yes or no.

Discovery leads to more accurate beliefs. These can be turned into *requirements*. Afterwards, one test such beliefs.

- Consequently, you don't need complete, formal requirements to start testing.



Both phases include:

- Observation & inference. Experimentation.
- Collaboration & alignment. Communication.



**Skepticism**

Testing requires a beginner's mind and a skeptic mind. Be willing to learn and also question everything.

> Descriptions are never complete.

Testing is about comparisons. The imagined world differs from the real world. The description differs from imagination. Obvious requirements tend to not be said out loud.



**Relevance**

Testing involves storytelling, justification and expectation management. Align with your partners. Understand their needs. Show the relevance. 

- Use formal language to describe the outcome. Emphasis may be skewed towards feasibility, viability or desirability.

Testing activities depend on the context.

<img src="../img/venn-feasible-viable-desirable.png" alt="venn-feasible-viable-desirable" style="width:30em;" />



**Repetition**

>  If testing is repetitive, you're doing it wrong

Tests are supposed to be automated. Once you've run a test, you may write down an expectation and turn it into a step-by-step guide: a runbook. Then, any operator can run it.



## Examples

- Test the health of a **person** in a medical exam.
- Test the viability of a **product** using an MVP.
- Test the performance of a **system**.
- Test the security of a **building**.



Note the contrast to *checking*: the act of performing step-by-step actions to do verification.

- Check whether the green light is on.
- Check the speed of your car.



## Goals

- Approval. Check acceptance criteria.
- Learn potential. Explore what is possible.
- Learn risks. Rule out side effects.



## Methods

First, consider the approach to take ([wiki](https://en.wikipedia.org/wiki/Verification_and_validation)):

- **Validation**. *How useful is the system for the owner?*
- **Verification**. *How well does the system do X?*
- **Exploration**. *What else can the system do?*

Statistically, it involves exploring how likely certain events are, correlation between events. On top of this, you might consider the  accuracy and sensitivity of predictions. See [statistics](../math/statistics.md).



## Practice

> Implicit requirements are also requirements.

Steps

- Ignore requirements. Use the product and learn through practice.
- Test the requirements. Infer whether they will be met in the future.
- Question the requirements. Attempt to break the system. Assume there are unwritten requirements. E.g. explore unwanted (harmful) side-effects.



### Exploration

A typical testing scenario.

1. Start with *normal* behaviour. Observe that the system responds as expected.

2. Tinker around with the system until you find a quirk. This is a signal.
3. Isolate the issue. Deconstruct components until you find a root cause.
4. Find side-effect. *What else is happening?*



### Experiments

1. Start with an hypothesis
2. Design an experiment to obtain evidence to reject the hypothesis.
3. Run it.
4. Reflect on it.
5. Repeat.



## Attitude

>  Testing = being a sceptic

Don't belief assumptions. In fact, don't belief anything. Treat each rule of a system as a probability.



It's not about how to test. Rather 

how to test <-> what to test

testing = learning, quickly



>  if testing is repetitive, you're doing it wrong



Systems thinking



## Strategy

You need a single test. If it fails, you need a second one. Third, you need to know the context. Where are you? Where is the system?



For simple systems it's feasible to reach full test **coverage**. To test all permutations: all possible paths.

- All lines of code. Alll branches in a decision tree.
- All combinations of all possible inputs.
- All possible events.



In practice, you'll want to focus on the **critical points** of a system. This involves:

- The happy flow. The expected path.
- Transition points. The boundary of a certain behaviour.
- Extreme values. The limits of the expected flow. Failure conditions. Invalid inputs.

