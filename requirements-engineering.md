# Requirements Engineering

Typical requirements include time- and cost-bounds, and a *scope*. In theory, only two of these can be guaranteed.

This scope can be defined in different levels:

- **Input**-based. This bears the least uncertainty, but the output itself may be unpredictable.
- **Output**-based. This leaves some freedom on the implementation side.  If risk materialize, either time or cost would have to be let go.
    - The bias on building something incentivizes over-engineering.
- **Outcome**-based. This focusses on solving a (user-centric) problem, with minimal effort. It incentivizes building the right thing, rather than something.
    - There is an incentive to solve the underlying problem, rather than the initially suggested problem. This can be uncomfortable.

In complex contexts, there is structural *uncertainty*. During execution of a task, more information will be discovered. The plan has to be adjusted when the initial requirements become outdated. The main challenge here is to choose whether to adjust the scope, the end date, or find another solution.



### Specification of Tasks

Some tasks can be explained in a single sentence, but (large) tasks can be defined more thoroughly.

### Template: Tasks

Before closing a task an appropriate review should be done to validate whether its purpose has been fulfilled.

#### Small Tasks

**Why** the need for change

- What problem does this task tackle?
    - Why does this need to be done now?

**What** is going to happen

- *Context*: What it the the <u>current</u> conditions?
- *Goal*:  What is the <u>target</u> condition? Use acceptance criteria. Make this user-centric.
- *Proposal*: What is the proposed solution?
- *Outcome*: To what higher-level goal does this task relate?
    - What are the next steps?

**How** to implement the change

- What are the sub-tasks that are involved?
- What is the minimal scope of the task?

#### Larger Task

In addition to the above:

**Why this** investment should be made

- What is the cost in terms of time and effort?
- How much uncertainty is there?
- What are the side-effects?

**When** this investment should be made

- What is the risk of not picking this up?
- How long can this be deferred?

How **success** is going to be measured

- What metrics will be used to track progress?



### Template: TODO Lists

Listing everything that's valuable can lead to an impractical number of items. Instead, classify the tasks. Then make the top priority task explicit.

By time horizon:

- Do now
- Do sooner
- Do later

By importance:

- Could do.
- Should do.
- Must do.

