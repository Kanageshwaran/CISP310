# CISP310
Computer Architecture and Organization
Recursive Sorted Linked-List Insertion
C → Assembly Translation & Debugging
Overview

This project implements and debugs a low-level assembly translation of a recursive C program that inserts nodes into a singly linked list while maintaining sorted order. The original implementation is written in C and uses a pointer-to-pointer (Node **) parameter to correctly update the head pointer during recursive insertion.

The goal of the project was to reproduce the exact semantics of the C implementation at the assembly level, ensuring correct pointer manipulation, control flow, and recursive behavior. This required careful handling of stack frames, memory addressing, conditional branching, and function return values.

Developed as part of coursework at American River College, this project emphasizes deep understanding of how high-level language constructs map to low-level machine operations.

Project Objectives

Translate recursive C logic into assembly while preserving program semantics

Correctly implement pointer-to-pointer behavior at the assembly level

Debug stack and pointer errors to ensure correct recursion and list updates

Strengthen understanding of memory layout and function calling conventions

Design & Implementation

The original C function inserts a node into a sorted singly linked list by recursively traversing the list and updating pointers as needed. It accepts a Node **ppn parameter so the function can modify the caller’s head pointer when inserting at the beginning of the list.

In the assembly translation, this behavior was recreated by:

Manually managing stack frames for recursive calls

Loading and dereferencing pointers to access node data and next pointers

Implementing conditional branches to compare node values and determine insertion points

Ensuring correct restoration of the stack and registers after each recursive return

Multiple debugging iterations were required to resolve issues related to incorrect pointer loading, branching logic errors, and improper stack cleanup, all of which can cause subtle and difficult-to-trace failures at the assembly level.

Key Concepts Demonstrated

Recursive algorithms in low-level code

Pointer-to-pointer manipulation

Stack frame construction and teardown

Assembly-level control flow and branching

Debugging memory and pointer-related bugs

Technologies Used

C

Assembly Language

Low-level debugging techniques

Learning Outcomes

This project strengthened my understanding of how high-level recursive data structure operations are implemented at the machine level. It reinforced core systems programming concepts, including memory management, calling conventions, and pointer semantics, which are essential for work in operating systems, compilers, and low-level software development.
