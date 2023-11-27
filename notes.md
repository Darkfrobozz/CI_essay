We will divide CI into two concepts:

# Tests
    There are many ways to test a program, tests are what makes modern continuous integration.
    For example, we cannot assure that all small changes due not cause some catastrophic change if we do
    not test it and we have manual vs automatic tests.

https://ieeexplore.ieee.org/abstract/document/4597151#:~:text=The%20principles%20that%20follow%20emerged,0814

## Principles
    - To test a program is to try and make it fail - not to assure quality, we are poking holes in an endless ocean
    - Tests are no substitute for specs - tests are by nature not general
    - Regression testing - turning failures into tests
    - Applying oracles
    - Manual and automatic testing
    - Empirical assessment of testing strategies.
    - A test's most important property is the number of faults it uncovers as a function of time

## Review Testing
    - The power of mind
    - The right environment
    - How to foster the right environment


## Test types
Testing paradigms follow a modular paradigm, this can be seen in the testing types.
    - Regression - fixing bugs, keeping existing functionality
    - Unit tests - testing individual components
    - Integration - testing components in relation to each other
    - System Tests - testing all components in union
    - Property-based - testing a property of a testing. Using jqwik I can use it as a resource as well, (the website).

## Automatic testing
    There is a need for controlling random generation of data. Utilizing what is not manually decided to cover a higher breadth
    than what can otherwise be achieved.
    This is also property based testing.

# Work control
    There are ways to organize our work flow such that we can effectively use continuous integration.
    For example, having a feature and main branch where any merges are controlled by our tests.
    Here the notion of branch protection comes in.