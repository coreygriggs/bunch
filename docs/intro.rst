Introduction
============

What is Bunch?
--------------
``Bunch`` is tool for grouping, managing and running tests written as ``Lettuce`` features.


Motivation
----------
The main reason for Bunch was the motivation to write more flexible and powerful tests with Lettuce. The key points to improve were:

* **Avoid hardcoded values in test scenarios.** Lettuce offers the only way for data-driven scenarios. It does it via scenario outlines. That means that all data is stored in script itself. External data sources may be only supported by your own test code. Bunch fills that gap introducing Jinja2 templates and YAML configuration files. Feature templates stay readable but gain flexibility. Every test execution produces regular Lettuce scenarios thus saving BDD style. Scenarios remain comprehensible for end-user.
* **Write test fixtures explicitly.** It should be possible to write setup and teardown BDD stories. It is also important to have behavior specifications for installation procedures.
* **Share and re-use test fixtures, specify that test depends on specific fixtures** Tests should be self-suffucient and should not rely on the state created by other tests. However It is often a huge overhead when each test performs its own setup which may always the same. Bunch provides the concept of "dependencies" between tests and test fixtures.
* **Tests are environment agnostic but test fixtures are environment dependent** Bunch enables writing environment agnostic tests by moving all environment specific action into test fixtures. Thus test fixtures may have multiple versions aimed for different environments.

Benefits
--------
* ``Bunch`` offers explicit separation of test fixtures from test scenarios by dividing it into setup, teardown and test scripts.
* ``Bunch`` encourages writing clean, self-sufficient and multi-environment tests, which can be executed in parallel.
* ``Bunch`` provides more flexibility for test parameterization - test scenarios are treated as templates, which get parameterized upon execution.

