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
   * A way of ensuring that your tests are actually testing your code
   * A measurement of how many lines/blocks/arcs of your script (or set of scripts) are executed while the automated tests are running
* Why do we need code coverage
   * A program with high code coverage has been more thoroughly tested and has a lower chance of containing software bugs than a program with low code coverage
* Types of code coverage (C0, C1, C2, C3)
   * Function coverage - Has each function (or subroutine) in the program been called?
   * Statement coverage - Has each statement in the program been executed?
   * Branch coverage - Has each branch of each control structure (such as in if and case statements) been executed? For example, given an if statement, have both the true and false branches been executed? Another way of saying this is, has every edge in the program been executed?
   * Decision coverage - Has every point of entry and exit in the program been invoked at least once, and has every decision in the program taken on all possible outcomes at least once? (where a decision is a Boolean expression composed of conditions and zero or more Boolean operators)? This definition is not the same as branch coverage,[3] however, some do use the term decision coverage as a synonym for branch coverage.[4]
   * Condition coverage (or predicate coverage) - Has each Boolean sub-expression evaluated both to true and false? This does not necessarily imply decision coverage.
   * Modified condition/decision coverage (MC/DC) - Have both decision and condition coverage been satisfied?
   * State coverage - Has each state in a finite-state machine been reached and explored?
   * Parameter Value Coverage - In a method taking parameters, have all the common values for such parameters been considered?
   * Linear Code Sequence and Jump (LCSAJ) coverage - has every LCSAJ been executed?
   * JJ-Path coverage - have all jump to jump paths (aka LCSAJs) been executed?
   * Path coverage - Has every possible route through a given part of the code been executed?
      * C0 = coverage of lines of code
	   * C1 = coverage of branches
	   * C2 = coverage of paths
	   * C3 = coverage of every condition inside an ‘if’ is once true and once false
	   * C4: Path-coverage = every possible path was taken, if(a) x else b; if(c) y requires 4 tests
         * a true c true
	      * a true c false
	      * a false c true
	      * a false c false
   * Entry/exit coverage - Has every possible call and return of the function been executed?
   * Loop coverage - Has every possible loop been executed zero times, once, and more than once?
   * Multiple condition coverage - This criterion requires that all combinations of conditions inside each decision are tested
   * Data coverage - Measures how many of the instance and static non-final fields were fully exercised by the test run. To be fully exercised, a field must have the last value assigned to it read by at least one test.
   * Line coverage - Tells us how much of the executable code in a source file has been exercised by tests. Each executable line of code can be uncovered, covered, or partially covered.

* Sources
   * http://en.wikipedia.org/wiki/Code_coverage
   * http://pjcj.net/testing_and_code_coverage/paper.html
   * http://xdebug.org/docs/code_coverage
   * http://stackoverflow.com/questions/195008/what-is-code-coverage-and-how-do-you-measure-it
   * http://testbench.in/TS_11_TYPES_OF_CODE_COVERAGE.html
   * http://www.atollic.com/index.php/trueanalyzer/types-of-code-coverage-analysis
   * http://grosser.it/2008/04/04/whats-my-coverage-c0-c1-c2-c3-path-coverage/
   * http://jmockit.googlecode.com/svn/trunk/www/tutorial/CodeCoverage.html
   * http://dev-logger.blogspot.com/2008/06/c0-c1-and-c2-coverage.html

* Best practices about code coverage
    * __Robert Martin__ (Uncle Bob)
        * > 100% test coverage is a natural side effect of proper development practices, and therefore a bare minimum indicator of quality. (quoted from [Deciphering Ruby Code Metrics](http://blog.codeclimate.com/blog/2013/08/07/deciphering-ruby-code-metrics/))
    * __David Heinemeier Hansson__ (creator of Ruby on Rails)
        * > Seven don’ts of testing: 1. Don’t aim for 100% coverage. [Testing like the TSA](http://37signals.com/svn/posts/3159-testing-like-the-tsa)


### Demonstration (ArmSE)

* Write short complex software
* Run test and display code coverage
* What other people say about code coverage?



Cyclomatic Complexity
---------------------

### Definition (Thai)

* Cyclomatic complexity is a software metric.
    * Developed by Thomas J. McCabe, Sr. in 1976
* It can be analyzed __statically__.
    * We do not need to run the code to measure the complexity.
* Why do we need to measure Cyclomatic Complexity
    * When a function is complex, it can be hard to maintain.
    * Give an example: a maze
* What does the number mean?
    * Number of linearly independent path through program's source code
* How to use these numbers?
    * Thomas J. McCabe: programmers should count the complexity of the modules they are developing, and split them into smaller modules whenever the cyclomatic complexity of the module exceeded 10
    * 10?
    * "For each module, either limit cyclomatic complexity to [the agreed-upon limit] or provide a written explanation of why the limit was exceeded."
    * Source: <http://en.wikipedia.org/wiki/Cyclomatic_complexity>



### Demo (Nut and Oak)

* Write short complex code
* Use tool to calculate cyclomatic complexity
* Refactor to reduce cyclomatic complexity



### Calculation (Oak)

* Code &rarr; Graph
	* Fournum Code : https://www.dropbox.com/s/0gvs7e6acsu35wj/FourNum.cs
	* Fournum graph : https://www.dropbox.com/s/g6p42rblycx5csl/final.jpg
	* Fournum (Less complexity) Code : https://www.dropbox.com/s/si6eiqma892vqv5/FourNum2.cs
* Calculation of cyclomatic complexity
	* REF: http://en.wikipedia.org/wiki/Cyclomatic_complexity
	* The cyclomatic complexity of a section of source code is the count of the number of linearly independent paths through the source code. For instance, if the source code contained no decision points such as IF statements or FOR loops, the complexity would be 1, since there is only a single path through the code. If the code had a single IF statement containing a single condition, there would be two paths through the code: one path where the IF statement is evaluated as TRUE and one path where the IF statement is evaluated as FALSE.
Mathematically, the cyclomatic complexity of a structured program[note 1] is defined with reference to the control flow graph of the program, a directed graph containing the basic blocks of the program, with an edge between two basic blocks if control may pass from the first to the second. The complexity M is then defined as[2]
M = E − N + 2P,
where
E = the number of edges of the graph,
N = the number of nodes of the graph,
P = the number of connected components (exit nodes).
An alternative formulation is to use a graph in which each exit point is connected back to the entry point. In this case, the graph is said to be strongly connected, and the cyclomatic complexity of the program is equal to the cyclomatic number of its graph (also known as the first Betti number), which is defined as
M = E − N + P.
This may be seen as calculating the number of linearly independent cycles that exist in the graph, i.e. those cycles that do not contain other cycles within themselves. Note that because each exit point loops back to the entry point, there is at least one such cycle for each exit point.
For a single program (or subroutine or method), P is always equal to 1. Cyclomatic complexity may, however, be applied to several such programs or subprograms at the same time (e.g., to all of the methods in a class), and in these cases P will be equal to the number of programs in question, as each subprogram will appear as a disconnected subset of the graph.
It can be shown that the cyclomatic complexity of any structured program with only one entrance point and one exit point is equal to the number of decision points (i.e., "if" statements or conditional loops) contained in that program plus one.
Cyclomatic complexity may be extended to a program with multiple exit points; in this case it is equal to:
π − s + 2,
where π is the number of decision points in the program, and s is the number of exit points.



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

