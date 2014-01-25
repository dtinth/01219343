Code Coverage and Cyclomatic Complexity
=======================================

Project Presentation Plan

Introduction
------------

* Introduce Group
* Outline
    * Source code quality management
    * Code coverage
    * Complexity
    * Other measures
    * Tools


Quality Management (Thai)
-------------------------

> "A software project is only as good as its QA workflow."
> —[Esprima Unit Test Page](http://esprima.org/test/index.html).

* Why do we need to manage source code quality?
    * [Software Rots](http://www.agile-process.org/change.html)
        * Quick fixes can increase complexity
        * Example: Copypasta
            * TODO add example
        * Example: Working around bugs in a hackish way
            * TODO add example from bms game
        * More complexity, harder to change
            * Everything is tangled up
            * Changing something in the software has chain-reaction effect
            * Fixing one bug can cause more subtle bugs to occur
                * These bugs are harder to find, and more expensive to fix


> [Y]ou can not effectively increase software quality
> at the end of the project by testing and fixing bugs.
> It remains low quality but with fewer bugs.
> —Don Wells, [Surprise! Software rots!](http://www.agile-process.org/change.html), 2009.


* So we need to keep the quality of the source code high.
    * We can do that using code quality measures.
* How to measure source code quality? There are many measures (metrics), such as
    * Code coverage
    * Cyclomatic complexity
    * Others will also be discussed in this session



Code Coverage
-------------

### Explanation (Nut)

* What is code coverage
- A way of ensuring that your tests are actually testing your code
- A measurement of how many lines/blocks/arcs of your script (or set of scripts) are executed while the automated tests are running
* Why do we need code coverage
- A program with high code coverage has been more thoroughly tested and has a lower chance of containing software bugs than a program with low code coverage
* Types of code coverage (C0, C1, C2, C3)
1. Function coverage - Has each function (or subroutine) in the program been called?
2. Statement coverage - Has each statement in the program been executed?
3. Branch coverage - Has each branch of each control structure (such as in if and case statements) been executed? For example, given an if statement, have both the true and false branches been executed? Another way of saying this is, has every edge in the program been executed?
4. Decision coverage - Has every point of entry and exit in the program been invoked at least once, and has every decision in the program taken on all possible outcomes at least once? (where a decision is a Boolean expression composed of conditions and zero or more Boolean operators)? This definition is not the same as branch coverage,[3] however, some do use the term decision coverage as a synonym for branch coverage.[4]
5. Condition coverage (or predicate coverage) - Has each Boolean sub-expression evaluated both to true and false? This does not necessarily imply decision coverage.
6. Modified condition/decision coverage (MC/DC) - Have both decision and condition coverage been satisfied?
7. State coverage - Has each state in a finite-state machine been reached and explored?
8. Parameter Value Coverage - In a method taking parameters, have all the common values for such parameters been considered?
9. Linear Code Sequence and Jump (LCSAJ) coverage - has every LCSAJ been executed?
10. JJ-Path coverage - have all jump to jump paths (aka LCSAJs) been executed?
11. Path coverage - Has every possible route through a given part of the code been executed?
12. Entry/exit coverage - Has every possible call and return of the function been executed?
13. Loop coverage - Has every possible loop been executed zero times, once, and more than once?
14. Multiple condition coverage - This criterion requires that all combinations of conditions inside each decision are tested

Sources
- http://en.wikipedia.org/wiki/Code_coverage
- http://pjcj.net/testing_and_code_coverage/paper.html
- http://xdebug.org/docs/code_coverage
- http://stackoverflow.com/questions/195008/what-is-code-coverage-and-how-do-you-measure-it
- http://testbench.in/TS_11_TYPES_OF_CODE_COVERAGE.html
- http://www.atollic.com/index.php/trueanalyzer/types-of-code-coverage-analysis
- http://grosser.it/2008/04/04/whats-my-coverage-c0-c1-c2-c3-path-coverage/


### Demonstration (ArmSE)

* Write short complex software
* Run test and display code coverage
* What other people say about code coverage?



Cyclomatic Complexity
---------------------

### Definition (Thai)

* Cyclomatic complexity is a software metric.
* It can be analyzed __statically__.
    * We do not need to run the code to measure the complexity.
* Why do we need to measure Cyclomatic Complexity
* What does the number mean?
* What is the standard number?
* What to do when we have high cyclomatic complexity?



### Demo (Nut and Oak)

* Write short complex code
* Use tool to calculate cyclomatic complexity
* Refactor to reduce cyclomatic complexity



### Calculation (Oak)

* Code &rarr; Graph
* Calculation of cyclomatic complexity



Exercise (ArmSE)
----------------

* Calculate complexity (quiz)
* Give code, and have students refactor (game)
    * Give them initial code with high cyclomatic complexity (and explanation of what it does)
    * Have them reduce the complexity
    * The code must pass all tests!



Other Metrics (Thai)
--------------------

* Lines of Code
    * Not an accurate measurement.
* Test/Code Ratio
    * Analogy — Review/Test Ratio (A/FR)
* ABC Metrics
* Similarity and Duplicate Code
* Churn + Complexity
    * Look at version control. Count how many commits



Tools (Nut and Oak)
-------------------

* Code Climate (JavaScript, Ruby)
* SonarQube (Java and 25 more languages)
* JavaNCSS (Java)
* CCM (*.js, *.cs, *.ts, *.c, *.cpp, *.h, *.hpp)


Summary
-------
TBA



Discussion
----------
* QA

