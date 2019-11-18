# Unit Testing Basics

- Unit Testing Definitions
- Why Unit Testing?
- Unit Testing Structure
- Writing a Quality Unit Test

## **Useful Definitions**

**Unit Test**: An automated testing that quickly and in an isolated manner, verifies a small piece of code (a unit).

**Refactoring**: The process of restructing existing code without changing its external behavior.

**Coverage Metric**: The ratio of the number of code lines executed by at least one test and the total number of lines in the production code base. This can range from 0-100%. A well built testing suite does not necessarily have a 100% coverage metric

**Testing Suite**: The entirety of the unit tests written in a production code base.

## **Why Unit Testing?**
Unit testing allows for greater confidence in the outputs of a production code base as well as allows for sustainable growth in the code base. While unit testing takes more upfront time, a quality testing suite will allows for refactoring and feature additions without a signficant amount of slowdown due to pinpointing and fixing bugs. See the image below for a look at the time spent working on a code base with and without testing.

![Alt text](/images/unit_testing_dev_cycle.jpg)

## **Unit Testing Structure**
A unit test should be built using the following *Arrange/Act/Assert* or *Given/When/Then* structure:

**Arrange/Given:** Bring the system under test and its dependencies to a desired .

**Act/When:** Call the methods on the system under test, pass the prepared dependencies, and capture the output value (if any).

**Assert/Then:** Verify the outcome.

## **Writing a Quality Unit Test**

A well built unit testing has four attributes:
- Protection against regressions
    - The tests written need to be able to catch bugs in the code and should be written in a way that will catch new bugs when features are added/removed/changed. In other words, how good the test suite is at indicating the presence of bugs.
- Resistence to refactoring
    - The tests written should be able to withstand the restructing of code without failing/throwing up false alarms. In other words, how good the test suite is at indicating the absence of bugs.

    ![Alt text](/images/unit_testing_error_types.bmp)

- Fast feedback
    - Unit tests that run quickly allow for efficient bug recognition and testing. Efficiencies here allow you to build out a greater breadth of tests which improves your coverage metrics.
- Maintainability
    - Good unit tests should be simple to understand and easy to run. Inability to capture these two sentiments leads to inefficiences when updating and refactoring tests.

If a test fails to embody these four standards, the test loses its value completely. However, it is impossible to maximize each of these four attributes as the first three at least are mutually exclusive. If you maximize two of the first three, you will end up with a shortcoming. The following diagram lays this out nicely.

![Alt text](/images/unit_testing_venn_diagram.bmp)



*All images are property of Vladimir Khorikov*
