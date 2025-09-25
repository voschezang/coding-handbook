# Management Patterns

Find part 1 [here](../management/management-principles).

[toc]

**Cost breakdown**

- Research
- Development
- Operations, Maintenance
- Sales, Marketing
- Support
- Documentation, Cleanup
- Turnover
  - Increased by stress, fear, blame, scapegoats

**Levels**

- Impact level. Impact is the product of execution, strategy and the market.
- Execution level
- Optics level

Short-term outcomes do not necessary result in long-term gain.

Inefficiency: experts who perform non-core work

Slack: too much slack (bureaucracy & fat middle management layer), too little (overly-efficient at the cost of adaptability)

**Types of Goals/Targets**

- Optimize for [Cost](https://en.wikipedia.org/wiki/Cost_accounting).
  - Goal: maximal ROI
  - Strategy: reduce everything by 10%.
  - Metrics: cost, profit.
  - Split organizational components into cost and profit centers.
    - Cost center: Maximize profit. This implies that profit is created here.
    - Cost center: Minimize cost. This usually leads to a bias for short-term cost reductions.
- Optimize for [Throughput](https://en.wikipedia.org/wiki/Throughput_accounting). Idea that the organization as a whole creates.
  - Goal: Sustainable flow of value.
  - Strategy: identify and resolve bottlenecks. Respond to feedback.
  - Metrics: lead time.
- Optimize for Quality. Product-teams. User-centricity.
- Optimize Culture. Create an organization of learning.
  - Make it cheap to make mistakes.

**Awareness**

- Goals, vision
  - What is the latest good news?
  - What is the three/six/twelve month vision? What is the next milestone?
  - Why this solution?
- Learning, adaptability
  - What did we learn recently?
  - What do we need to learn?
  - How has the story changed?
  - What is the user-response to this? How does this relate to sales/marketing?
  - What is blocking us?
- Risk and success
  - How are you measuring success? What will be possible as a result?
  - How is team morale?
  - How does our success relate to individual team members?
  - What are the emergent risks?
  - What are the nightmarish risks?

**Bureaucratic Waste**

- more managers than employees
- jobs that revolve around selling ideas and proposals to others
- paperwork & manual administration

Bureaucracy limits innovation

- Bias against investment and experimentation. Assignment of minimal resources by default. Requirement to write down beforehand what the end result will be.
- Waste through marketing/advertising: Employees compete against each other for funding.

**3 lines of defense**

1. Ops / business line
2. Risk management, compliance
3. Internal audit. Verify that 1 and 2 are working in the right way

## Management Types

Subjects

- People management
  - of employees, of managers
- Product management (PO)
- Project management
- Process management (scrum master)
- Operations management
  - Largely invisible to users; "make sure that users are not impacted".
  - Continuous process. Not like (some types of) development where features are finished and shipped.

**Project vs. Product management**

See [product-management.md](../management/product-management.md)

**Decision-making**

- Product-led: make a great product that is easy to sell

- Sales-led: build the features that users want

Situational leadership: `Delegating - Supporting - Coaching - Directing`

**Definitions**

- Output: what one do/did to go from A to B
- Outcome: the condition B itself
- Impact: the result in comparison to environment/context. e.g.. ROI

> Maximize outcomes but minimize (software) output

Output and outcome.

- Feature factory: measure output velocity.
- Value creation system: value creation velocity.

**Feature factory**

Risks

- Output > outcome. Lack of outcome-based measurements.
- Bias for optics and releasing, over removing and re-adjusting.
- Culture of hand-offs.
- Large batches.

## Management by Type

### Risk Management

This is a continuation of [risk management principles](<../management/principles.md#Risk Management>).

**Steps**

1. Risk discovery

- How is risk discovery handled?
- Who is responsible?
- Are there frequent discussions that explore (operational) risk?
- Is it safe to signal a risk?
- Can you distinguish between goals and estimates (schedule/planning)?
  - Risk can be defined as the difference between the goal and the schedule.

- What risks do you see ahead?
  - What are the emergent risks?
  - What would be a catastrophic/nightmarish risk?
  - What would be a blame-worthy failure? For each positions: manager, boss, operator, developer, designer, stakeholders.

2. Exposure analysis: predict impact

3. Contingency planning: what to do afterwards
4. Risk mitigation
5. Monitoring

### Lean Management

A style rather than a type

- Value streams
  - Visualize flow of work/value. Highlight bottlenecks.
  - Bias for lead time.
    - Small batches. Prefer flow over efficiency.
- Iterate and incorporate customer feedback.
  - Adjust plans rather than sticking to them.
- Empower teams such that they can improvements.

**Hot potato method**
Prioritize the tasks. Then, be aggressive on high priority tasks, focussing on short-term efficiency. For all other tasks, allow long-term improvements to be made, until these tasks gain higher priority.

## Communication

See [communication](../communication.md).

E.g. in case of uncertainty

- This is a complex situation. We aren't sure but we can learn from this experiment.
- This is why time is of the essence.

Team culture

- How does the team or its members handle conflict? E.g. Do they address is or avoid it?
- When are bugs addressed, immediately or when there is time? Are broken builds acceptable?
- How often do processes change?

Visibility doesn't imply transparency.

Level of collaboration within a team.

- Silo's: groups of individual experts working in their domain.
- Pairing: tiny groups within the team.
- Mobbing: small groups within the team.
- Swarming: working with a large group on a single task. E.g. fix a production issue.
- Awareness: sharing of
  - Status updates
  - Details about individual work
  - Feedback of individual work
- ...

**Perceived Micromanagement**

Seemingly lack of trust.

- Is success sufficiently defined?
- Is there incremental progress?
- Is the variance expected to be high? Is risk addressed properly?
- What is the communication style?
  - Frequency, involvement?
  - Nature: reporting, coaching or delegating?

## Collaboration

### Sourcing / Human resources

Factors

- Performance. Good? Consistent?
- Skillset. What is the mix of specialist and broad skills. How do these match?
- Teamwork and collaboration. Sharing knowledge, supporting other colleagues
- Culture fit (company wide)
- Opportunity cost. What is the alternative. Are we able to attract other candidates?
- Business need. Again: skill & experience

Extra

- Employee engagement. Do we expect they to commit to long term
- Growth opportunities for this employee in this company

**Contract renewal** - reflection tools

Outside perspective

- Suppose we had a vacancy, and we could hire him/her again. What would we decide?

Invert question

- Why would they be valuable for the team?

### Group performance indicators

See <https://www.aihr.com/blog/team-effectiveness-models/>

### Other

**Processes**

Processes have a natural tendency to become more complex and less optimal. Individual components will specialize, at the cost of cohesion. Hence you occasionally have to reconsider the current process and adjust it where necessary. Both from the perspective of an outsider (top-down) and from the perspective of an insider (seeing the related components and connections)

**Turnover**

New colleagues

- Warm welcome. Put in special care for team members that join and leave. These are critical moments.
- Note down their first impressions. This is a unique moment where one can get unbiassed input.

## Value

**Work environment**

Company values should be reinforced though the work environment. E.g. if software quality is valued then internal software should also be of high standards.

### Value of Employees

The value that the average employee brings can be expressed as:

- Inherent value of the professional. Note that these are usually relative to other professionals.
  - Knowledge
  - Skill
  - Experience
    - Relevant Experience
    - Background, context, other perspectives
- Perceived value to the organization. This is subjective to the employer.
  - Cost of replacement.
  - Customer value.
  - Market supply and demand.
  - Profitability of a project, relative to the number of employees on that project

A "fair" salary has the following preconditions (excluding benefits etc.). It should be comparable to:

- Other roles. E.g. the level of difficulty and responsibility.
- Other employees. E.g. knowledge, skill, experience, personality (e.g. resilience, integrity, temperament).
  - In Dutch: `kennis, kunde, ervaring, karakter`

## Motivation & Productivity

> Busy? Is that caused by a lack of priorities, faulty expectations or grandiose desires?

Motivation and goals.

- Define a major, long-term goal. Then add intermediate steps.
- For each subgoal: *specific, measurable, acceptable/attainable, relevant* and *time-based*
- These goals should be dynamic; if circumstances change there may exist good reasons to change them.

Goals are motivational. They should be optimistic, on the edge of what's possible.

Planning should be realistic; otherwise people will become cynic.

The relation between pressure and misbehaviour.

- Unrealistic deadlines don’t influence people. They will become cynic and demotivated.
  - Use (periodic) deadlines as a tool to the extend that they are effective.
- People under high pressure don’t think faster.
- Side effects: burnout, error rate.

Periodic goals (weekly, quarterly) are motivational tools. Use it when the intrinsic motivation in a team is not sufficient.

Misbehaviour will never cease to exist, people will become better at hiding it.

![plot-pressure-misbehaviour](../img/plot-pressure-misbehaviour.png)

Behavior and ideology of higher management influences lower management and employees.

- Abusive behaviour will [trickle down](https://en.wikipedia.org/wiki/Trickle-down_economics).

Note that anger may be caused by fear.

Typical pattern: managers set a deadline. If the project is on schedule, they will turn up the pressure (e.g. move the deadline forward). If the project is halfway, they'll turn on the screws. They's like to see employees *sprinting* by default, from start to finish.

- This incentivizes employees to automatically resist deadlines and exaggerate their current work pressure.

**Overstaffing**

Adding more employees to a project won't indefinitely improve productivity and added value.

- After reaching the optimum, productivity will drop due to communication and process [overhead](https://en.wikipedia.org/wiki/Brooks%27s_law).
  - I.e. improving productivity or efficiency often results in new bottlenecks.
- Overstaffing degrades design; it forces work to be split up [based](https://en.wikipedia.org/wiki/Conway%27s_law) on the number of teams rather than through a deliberate architectural decision.

![plot-participants-value](../img/plot-participants-value.png)

[Larger](https://en.wikipedia.org/wiki/Conway%27s_law) teams tend to produce larger and more complex software (and take [longer](https://en.wikipedia.org/wiki/Brooks%27s_law)).

<https://en.wikipedia.org/wiki/Brooks%27s_law>

Project staffing stages - for which types of projects? all?

- Design
Low staf - handful of people
- Development & testing (still agile)
Medium staff
- Production - assuming new features will be added
High staff
- Production - legacy/maintenance
Small/medium staff

### Side-effects of high WIP

This is relevant to types of work where people *can* collaborate, and where interdisciplinary skills are valuable. In general, the optimum WIP limit depends on the current environment. [source](https://medium.com/hackernoon/wip-it-real-good-66aa710178fd).

Direct effects:

- The juggling of multiple tasks instead of focussing on a single task. This may result in lower throughput (per task).
- Pareto paralysis, the feeling that everyone to overly busy. Less inter-team collaboration.
  - Collaboration is considered "too disruptive".
  - Limited "focus time", self-care etc.

Indirect effects:

- Culture of handoffs: team-members optimize for short-term efficiency by finding ways to work alongside each other, instead of collaborating on a single task.
- More planning and more "dependency management". Hiring more managers and coordinators. Increasing the length of plans to account for expected delays.
- Tasks that are on hold (which could be a sign of a bottleneck) are not addressed, but instead are ignored in favor of other tasks.
- Difficulty to see what's blocking or slowing down progress.

Causes:

- Corporate culture. Doing favors. Dependence on informal collaboration.

- Bias for action instead of finishing reflection. E.g. preferring to start new tasks instead of finishing current tasks.

*Good* solutions:

- Decrease batch size to improve flow (one-by-one production). Limit total WIP and/or WIP per type.
- Address impediments. Remove obstacles.
- (Cross-functional) Product teams that are independent.

*Poor* solutions:

- More / better upfront planning - this will increase lead time and decrease flexibility.
- Stricter process, more rules - this will create an administrative/bureaucratic burden.
- Stronger commitments, motivation - people already work hard.

![WIP it real good - johncutlefish](img/WIP it real good - johncutlefish.jpeg)

Note that the following burn-down chart is "red", even though the work is finished perfectly on time.

![plot-burndown](../img/plot-burndown.png)

`Velocity = lead time per task x number of tasks`

Note that the time scale is important. Setting it too low can lead to over-optimizing a component.

A stochastic simulation of production stages over time. The average velocity per stage is set to two. The horizontal arrow indicates lead time.

This simulation is fully random and assumes that capacity and velocity are equal. In reality the velocity depends on efficiency of the work and is influenced by the number of people working on a single task at the same time. This can in turn be influenced by setting a WIP limit per stage.

![plot-cumulative-flow](../img/plot-cumulative-flow.png)

## Anti-patterns

- Planning.
  - The planning has already been done. The plan is perfect We just have to execute this.
  - QA after planning instead of during or in conjunction with.
  - Overpromising. Relying on luck to succeed, instead of relying on avoiding problems.
  - Punish good work by increasing expectations.
- Process
  - Don't ask questions, just follow the process. "You *just* have to do X".
  - Double down if something is not working, but is supposed to work.
    - Follow a drift or trend blindly.
  - Optics: Looking like you're trying instead of actually trying.
  - Using collaboration tools (e.g. JIRA) to measure/compare teams rather than to enhance productivity.
  - Keep the system running through heroics.
- Blameful culture
  - Push employees to over-promise and later hold them accountable for under-delivering.
    - Punish people who can't make (or accept) unrealistic deadlines.
  - Attribute problems (exclusively) to individuals instead of to "the system".
- Culture of certainty
  - Prefer being wrong over being uncertain.
  - Neglect and suppress risks instead of managing them. "That will never happen, otherwise we're screwed anyways."
  - Avoidance of uncertain projects (instead of making small bets or time-boxed experiments).
  - Dependencies are undesirable. Hence they are not made explicit.
- Culture of fear
  - Repeat mantra's as a means to reach goals. Credibility through repetition.
  - Overly political communication.
  - Idea that one shouldn't raise problems unless one has a solution for them.
    - Raising a problem means you have to solve it.
  - Don't be the bearer of bad news.
- Lack of free information. Information is hoarded or distorted for political reasons.
- Pitch culture. Reward successful pitches, but afterwards there is no turning back.
- Optimizing metrics instead of targets. E.g.
  - Sales revenue (at the cost of customer satisfaction)
  - Production quantity (instead of quality).
  - Employee productivity (at the cost of turnover).
  - Improve quantity AND quality (at the cost of adaptiveness or flexibility).
- Interviewing candidates
  - Single-sided interview (e.g. just technical).
  - Lack of trust between different interviewers.
- Cost center optimization.
  - Optimize individual components (e.g. resources) based their cost.
  - Maximize resource utilization and efficiency everywhere (without considering the long-term impact).
