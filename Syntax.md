Introduction
============

Purpose
-------

My first intention designing closed zero - (0) - is to encode machine operations into messages of inter-process communication (IPC).

Normal IPC message contain only signal or data. According to which kind of signal or data is received, the receiving process will do the predefined operations. This way the receiving process must contains all posible operations in its code, and its code must be changed if the message type to operations mapping is changed.

By introducing the operations into IPC message, the receiving process will simplify its code into providing only simple function calls as libraries or services and the operations in received message will do its business. This sounds like viruses being passing around in your system(scary but fun). There 're two reasons why this is absolutely safe:

1. (0) is an interpreted language, not machine code. There 's no way anything will be tampered outside of (0) runtime.

2. IPC has their own machenism of authentication and that will be enough to prevent messages from calling what they should not.

Design criterias
-----------------

Programming languages often add new features to make them more appeal. Some added object-oriented, other added functional. Some added new data type, other added new syntax sugar. In my own opinion, languages is more powerful only if we restrict to use only subset of them. By removing and restricting the use of ugly syntaxes, of hard-to-read expressions, or of unnecessary data types we will significantly improve readability, writability, and reduce learning effort. Because of that, I want to make (0) simple from start, no functional, no object oriented, no complex data type - thought I think I will keep the notion of closure and first-class function.

Eventhough (0) bear some similar in its syntax with LISP, it is not a LISP. There 're two main points that make it so:

1. List is not a built-in data type in (0).

2. (0) is not functional, it is imperative - super imperative to be exact.

(0) is super imperative because it has no conditional statement, no loop, and most of all no function call - therefore no stack. In place of conditional statement, (0) has pattern matching. In place of loop, (0) has parameter cross produce. And in place of function, (0) has fiber - lightweight thread requiring no stack at all.

Data types
==========

Primitive types
---------------

1. Integer

Only 5 vatiation of integer type are supported:
(int8 15)
(int32 -150)
(uint32 150)
(int64 -1500)
(uint64 1500)

2. Real number

(float 15.0e12)
(double 15.0e24)

3. Character

Complex types
-------------

1. Array

2. X-ple

Variable
========

Pattern matching
================

Fiber
=====

Parameter cross produce
=======================

