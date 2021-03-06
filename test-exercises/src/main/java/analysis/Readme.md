Spoon
===

[Spoon](http://spoon.gforge.inria.fr/) is an open-source library that enables you to transform and analyze Java source code. Spoon provides a complete and fine-grained Java metamodel where any program element (classes, methods, fields, statements,
expressions...) can be accessed both for reading and modification. Spoon takes as input source code and produces transformed source code ready to be compiled. Spoon can be integrated in Maven and Gradle. 

Here, the students will write Spoon processors that statically analyse (i.e. analysing the code without running it) Java code to find bad coding practices in Java code. You will also refactor the analysed code to
remove these bad coding practices. A first toy processor that detects double for loops is provided.

Practical session
===

 Pictures of the abstract syntax tree (AST) of the code
to analyse are provided here: https://github.com/VANDV-M2-ISTIC-2016/Exercises/tree/master/test-exercises/src/test/resources/java/testannot. Theses pictures will help you in identifying the Spoon classes to use. 

Q1. Code a processor for detecting unit tests (i.e. public void test*() operations) not annotated with the @test annotation.

Q2. Add to the processor a method that refactors the code affected by this bug.

Q3. Code a rule for detecting unit tests that contain a try/catch block.

Q4. Improve this last rule for detecting unit tests that contain a try/catch block where the catch block contains a fail
method call, for instance:

```java
	@Test public void testFoo( ) {
	try {
		...
	} catch (...) { fail(); }
	}
```
Q5. Add to the processor a method that refactor the code affected by this bug. This means that the exception must be thrown be the method.
