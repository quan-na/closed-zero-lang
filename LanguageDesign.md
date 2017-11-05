Purpose
=======
The language is designed to work across processes and hosts. In order to do that, it must satisfy these following criteria:
 - Simple parallel processing, single thread is preferred.
 - Simple synchronization mechanism, non-blocking is preferred.
 - On-the-fly interpretation and execution, full Abstract Syntax Tree should not be needed.
The name of this language is closed-zero aka zero cost closure. It is abbreviated as (0).

Core
====
This section contain criteria that make up (0). Theses are not subject for arguments.

## First class fiber
The basic operation unit in (0) is fiber.
 - Fiber has yield points that break its operations in smaller atomic units.
 - Fiber requires no stack to operate.
 - Fiber can be packed and sent to other operating units.

## Pattern matching replace condition clause and lock
The match control structure will match a variable against data structure, types, and value conditions. If there is no matched, the fiber will suspend until matched. Fiber parameter is also matched at beginning of each fiber.

## Array operation replace loop

Draft
=====

## Data types

## Inline fiber

## Lazy list evaluation

## Lazy evaluation

Preview
=======
