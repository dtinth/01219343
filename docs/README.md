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
* Why do we need code coverage
* Types of code coverage (C0, C1, C2, C3)



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

