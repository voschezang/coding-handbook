# Testing



**Testing**

> The entropy (complexity) of software without "good" tests can only increase. Tests allow features to be safely removed.

The term testing is usually used for "checks". A distinction can be made based on the role of requirements.

- No requirements: Testing. E.g. `observing, exploring, experimenting`.
  - Learn something new. Do research. This is inherently unpredictable. Techniques to improve consistency are:
    - Time-boxes. Zoom in and out.
  - Black box: study the different inputs and outputs of a system.
  - White box: study the inner systems.
- Requirements: Checking.
  - Verification and validation based on pre-specified requirements
    - This can often be **automated**
  - [TDD](https://en.wikipedia.org/wiki/Test-driven_development): write small tests (checks) first, and the implementation second.
    - Strong TDD: Write a minimum failing test, write minimum code to fix the test, then refactor without introducing new behaviour.

In the absence of pre-specified requirements it is still possible to list all the dimensions (properties) of the system and consider how they can be measured.

No testing.

- Develop a PoC, then evaluate whether it should be put into production, and only then continue with TDD on that specific feature. This means that there are no tests written for unused code.



**TDD**

>  Write new code only if tests have failed

In [TDD](https://en.wikipedia.org/wiki/Test-driven_development): small tests (checks) are written first, followed by actual implementation. It discourages any code changes done without testing, with the exception of removing duplication or optimizing code (for performance).



**Test Pyramid**
Rely on unit-tests (checks) to verify that requirements or specifications are met. Decompose large integration tests.

- UI should have unit-tests.
- Tests for interfaces can be generated automatically.



**Anti-pattern**
Ice-cone: inverse testing pyramid. Too many integration and UI tests, which are slow, unmaintainable and too sensitive.



## Testing Types

Types

- 🔗 Integration test. Test end-to-end chain.
- ⛓️‍💥 Unit test. Test individual components.
- 🐤 Smoke test. Regression tests. Find signals that are correlated with issues.
- ⚡ Stress test. Find limits of a system.
- 🆎 A/B test. Compare scenarios.
- Beta test.



## System Verification

❤️‍🩹 Is the system **healthy**? Is it degrading?

⌛ How **soon** will we know? How are we notified?

👀 Are we **aware** of all components (and roles)?

🛠️ Are we **in control**? Is the system manageable? Are we able to deploy changes?







## References

K. Beck. *Test-Driven Development*
