# Computer Science Glossary <!-- omit in toc -->

## Contents <!-- omit in toc -->
- [Abstraction](#abstraction)
- [Abstract class](#abstract-class)
- [Algorithm](#algorithm)
- [Anonymous function](#anonymous-function)
- [Anti-pattern](#anti-pattern)
- [Argument](#argument)
- [Array](#array)
- [Artifact](#artifact)
- [Assembler](#assembler)
- [Assembly language](#assembly-language)
- [Big O notation](#big-o-notation)
- [Bit](#bit)
- [Branch](#branch)
- [Byte](#byte)
- [Call stack](#call-stack)
- [Central processing unit](#central-processing-unit)
- [Class](#class)
- [Closure](#closure)
- [Cohesion](#cohesion)
- [Compiler](#compiler)
- [Concrete class](#concrete-class)
- [Concurrency](#concurrency)
- [Constant](#constant)
- [Constructor](#constructor)
- [Control flow](#control-flow)
- [Coupling](#coupling)
- [Critical section](#critical-section)
- [Currying](#currying)
- [Database](#database)
- [Data structure](#data-structure)
- [Data type](#data-type)
- [Deadlock](#deadlock)
- [Declaration](#declaration)
- [Decompiler](#decompiler)
- [Decomposition](#decomposition)
- [Defensive programming](#defensive-programming)
- [Design pattern](#design-pattern)
- [Disassembler](#disassembler)
- [Encapsulation](#encapsulation)
- [Execution](#execution)
- [Expression](#expression)
- [First-class citizen](#first-class-citizen)
- [Function composition](#function-composition)
- [Function overloading](#function-overloading)
- [Functional programming](#functional-programming)
- [Garbage collection](#garbage-collection)
- [Global variable](#global-variable)
- [Graph](#graph)
- [Hashing](#hashing)
- [High-level language](#high-level-language)
- [Higher-order function](#higher-order-function)
- [Idempotence](#idempotence)
- [Information hiding](#information-hiding)
- [Inheritance](#inheritance)
- [Initialisation](#initialisation)
- [Instance](#instance)
- [Interface](#interface)
- [Interpreter](#interpreter)
- [Invariant](#invariant)
- [Linked list](#linked-list)
- [Linker](#linker)
- [Literal](#literal)
- [Loader](#loader)
- [Local variable](#local-variable)
- [Logic programming](#logic-programming)
- [Low-level language](#low-level-language)
- [Machine code](#machine-code)
- [Member variable](#member-variable)
- [Memory](#memory)
- [Message passing](#message-passing)
- [Method](#method)
- [Method overriding](#method-overriding)
- [Mixin](#mixin)
- [Model View Controller (MVC)](#model-view-controller-mvc)
- [Modularisation](#modularisation)
- [Multiple inheritance](#multiple-inheritance)
- [Mutability](#mutability)
- [Name resolution](#name-resolution)
- [Obfuscation](#obfuscation)
- [Object-oriented programming](#object-oriented-programming)
- [Object code](#object-code)
- [Object composition](#object-composition)
- [Object lifetime](#object-lifetime)
- [Operator](#operator)
- [Overhead](#overhead)
- [Parameter](#parameter)
- [Polymorphism](#polymorphism)
- [Procedural programming](#procedural-programming)
- [Process](#process)
- [Program lifecycle](#program-lifecycle)
- [Programming paradigm](#programming-paradigm)
- [Pure function](#pure-function)
- [Race condition](#race-condition)
- [Recursion](#recursion)
- [Relational database](#relational-database)
- [Resource starvation](#resource-starvation)
- [Reverse engineering](#reverse-engineering)
- [Scope](#scope)
- [Side effect](#side-effect)
- [Source code](#source-code)
- [Space complexity](#space-complexity)
- [State](#state)
- [Statement](#statement)
- [Subroutine](#subroutine)
- [Synchronisation](#synchronisation)
- [Syntax](#syntax)
- [Test-driven development](#test-driven-development)
- [Thread](#thread)
- [Time complexity](#time-complexity)
- [Translator](#translator)
- [Tree](#tree)
- [Type signature](#type-signature)
- [Type system](#type-system)
- [Unified Modelling Language](#unified-modelling-language)
- [Value](#value)
- [Variable](#variable)
- [Variable shadowing](#variable-shadowing)
- [Virtual machine](#virtual-machine)

## Abstraction
Abstraction involves **representing objects/data in a simplified/generalised way**, to focus on their most important behaviour and characteristics. Also known as *modelling*. This often involves providing a relatively simple [interface](#interface) to the object/data that [hides](#information-hiding) the specific details of the implementation (which may be more changeable and complex).

[Encapsulation](#encapsulation) is a similar concept that relates to the implementation of abstraction, beyond the object's observable behaviour (independent of implementation).

## Abstract class
An abstract class is **a [class](#class) that cannot or should not be [instantiated](#instance)**. Also known as an *abstract type* or an *abstract base class (ABC)*. Instead, an abstract class is designed to be used as a basis for developing more specific child classes, which [inherit](#inheritance) from the abstract class. Abstract classes often contain incomplete methods (e.g. with only a [signature](#type-signature), i.e. an *abstract method*) that must be properly implemented when they are inherited.

In contrast, a [concrete class](#concrete-class) is fully implemented and can be instantiated.

## Algorithm
An algorithm is a **sequence of instructions used to complete a specific task**, that produces a specific output based on a given input. The value of a specific algorithm is often assessed based on its efficiency, specifically [time complexity](#time-complexity) and/or [space complexity](#space-complexity).

Algorithms can be categorised based on *algorithm paradigms*, which are used as frameworks for the design of algorithms. Common paradigms include *divide and conquer* ([recursively](#recursion) decomposing a problem into multiple related sub-problems, e.g. *quicksort*); *greedy algorithms* (making the optimal choice at each stage, if not overall); and *brute-force search* (systematically checking all possible candidates for the solution).

## Anonymous function
An anonymous function is **a function definition that is not associated with an identifier (i.e. the function name)**, and therefore cannot be called from elsewhere in the program. Also known as *lambda functions* or *lambda expressions*. They are syntactically lighter, so can increase code readability and may be more efficient. 

Anonymous functions can be used to create "throwaway" functions that are only needed once. They can be passed to and from [higher-order functions](#higher-order-function), where a function definition is required but does not need to be referenced later, e.g. to implement [closures](#closure). They are commonly used in [functional programming](#functional-programming).

## Anti-pattern
An anti-pattern is a **commonly used software development pattern that is considered a bad programming practice**, and the opposite of a [design pattern](#design-pattern). Anti-patterns are often used in response to common problems, but are problematic as they can be ineffective and/or cause other issues.

For example, the *God object* anti-pattern refers to an object that knows or does too many different things, where multiple objects with more specific roles would be preferable. A God object results in high [coupling](#coupling) that makes maintenance more difficult.

## Argument
An argument is **a value that is passed into a [subroutine](#subroutine)** (i.e. when the subroutine is called). In contrast, a [parameter](#parameter) refers to a [variable](#variable) used within a subroutine definition. However, *argument* and *parameter* are often used interchangeably. Also known as an *actual argument* or *actual parameter*.

## Array
An array is **a linear [data structure](#data-structure) comprised of elements of the same [data type](#data-type) that can each be identified by at least one *index***. An array is stored in [memory](#memory) such that the position of each element can be computed from its index. *Array* can also refer to the data type in some [high-level languages](#high-level-language), regardless of the underlying data structure. *Lists* are similar to (and can be implemented using) arrays, but are distinct (e.g. can contain different data types).

Arrays can have one dimension (*linear arrays*), two dimensions (sometimes called *matrices*), or more. In contrast to *static* arrays which have a fixed capacity, a *dynamic array* allows for elements to be added and deleted. Unlike [linked lists](#linked-list), arrays support *direct access* (also known as *random access*), allowing many basic operations to be performed highly efficiently. Arrays can be used to implement many other data structures.

## Artifact
An artifact is **a tangible by-product produced during software development**, such as a [UML diagram](#unified-modelling-language) or project plan.

## Assembler
An assembler is **a program that translates [assembly language](#assembly-language) code into [machine code](#machine-code)**, and is a type of [translator](#translator). See also: [low-level language](#low-level-language).

## Assembly language
Assembly language is **any [low-level language](#low-level-language) in which there is a very strong correspondence between the instructions in the language and the architecture's [machine code](#machine-code) instructions**. Also known as *assembler language*, *symbolic machine code*, or *second-generation language*. Assembly language is produced by [translating](#translator) a [high-level language](#high-level-language) (i.e. [source code](#source-code)).

Because [assembly](#assembler) into machine code depends on the machine code instructions, every assembly language is designed for one specific computer architecture. Assembly code is readable by humans, with symbolic equivalents (*mnemonics*, i.e. representative text [statements](#statement)) to the corresponding machine code (which isn't readable).

## Big O notation
Big O notation is **a representation of computational complexity which describes the behaviour of complexity when the input size (`n`) increases**, i.e. *asymptotic analysis* to determine the *asymptotic behaviour* (growth rate) of the complexity. Also known as *Big-Oh*.

Specifically, big O notation is often used to describe the [time complexity](#time-complexity) and [space complexity](#space-complexity) of [algorithms](#algorithm), to assess their efficiency and usefulness. Common complexities in big O notation include `O(n)` (linear); `O(log n)` (logarithmic); `O(n log n)` (linearithmic); `O(n^2)` (quadratic); and `O(1)` (constant).

## Bit
A bit is **the most basic unit of information in computing, which represents a logical state with one of two possible values**. These values are most commonly represented as either `1` or `0`, but other representations such as `true`/`false` are commonly used. The name is a contraction of binary digit. See also: [byte](#byte).

## Branch
A branch is **a [statement](#statement) in a program that causes the [execution](#execution) of a different instruction sequence** (i.e. *branching*) rather than continuing the execution of instructions in order. Also known as a *control flow statement*. Branching is used to implement [control flow](#control-flow), e.g. via conditional statements and loops. An *unconditional branch* always results in branching, while a *conditional branch* may not (depending on some condition).

## Byte
A byte is **a unit of of information in computing, which most commonly consists of eight [bits](#bit)**. Historically, the byte was the number of bits used to encode a single character of text in a computer. As a result, in many computer architectures a byte is the smallest addressable unit of [memory](#memory).

## Call stack
A call stack is **a stack [data structure](#data-structure) that stores information about the active [subroutines](#subroutine) of a program**. Also known as an *execution stack*, *program stack*, or *control stack*. The primary purpose of the call stack is to keep track of where each active subroutine (called but not yet fully [executed](#execution)) should return control after it has been executed. Maintenance of the call stack is usually done automatically in [high-level languages](#high-level-language). 

Specifically, the instruction that makes the call *pushes* the [memory address](#memory) of the instruction immediately following it, known as the *return address*, onto the stack (also known as *winding*). When the called subroutine finishes it *pops* the return address off the call stack and transfers control to that address (also known as *unwinding*). If a called subroutine calls another subroutine, it will push another return address onto the call stack, and so on. If the stack uses up more space than it was allocated, a *stack overflow* error occurs, often causing a program crash.

## Central processing unit
A central processing unit (CPU) is **the electronic circuitry that [executes](#execution) the instructions within a program**. Also known as the *central processor* or *main processor*. 

These instructions include basic arithmetic, logic, controlling, and input/output (I/O) operations, as specified by the [machine code](#machine-code) (produced via [translation](#translator)) that controls the CPU. The execution of instructions by a CPU involves repeatedly following a *fetch–decode–execute* cycle (also known as the *instruction cycle*) for each instruction.

## Class
A class is **a template that is used to create (or *instantiate*) one or more object [instances](#instance)**. Also known as a *class definition*. 

This template defines the initial [member variables](#member-variable), [method](#method) implementations, and any [inheritance](#inheritance) from parent classes. Classes can be *[concrete](#concrete-class)* (fully implemented and instantiable) or *[abstract](#abstract-class)* (not instantiable). A class that creates other classes (only possible in some languages) is called a *metaclass*. The class name is often used to refer to the class definition, the [constructor](#constructor), and the [type](#data-type) of objects that are instantiated by the class.

## Closure
A closure refers to **a technique for implementing [first-class](#first-class-citizen) functions, via a function that *closes over* the environment in which it was defined**. The environment is a mapping associating the function's [free variables](#variable) (used locally, but defined in an enclosing [scope](#scope)) to the function/closure name binding. A closure allows the function to access the closure's copies of these captured variables, even when the function is invoked outside their scope. In other words, a closure is a persistent scope which retains free variables.

For example, if a variable `a = 1` is defined in `func` and then `a` is used within an inner function, `inner`, `a` is a free variable of `inner` (i.e. defined within the enclosing `func` scope). If `func` returns `inner`, then `x = func()` will create a name binding of `x` to `inner` (i.e. the return value of the `func` call). The version of `inner` assigned to `x` will include the variable `a` with a value of `1`.

More practically, `a` could be passed as an [argument](#argument) (rather than having a fixed value) to the outer function and then be used by the inner function. For example, `add(a)` could contain and return the function definition for `inner(b)`, which returns `a + b`. Defining `add5 = add(5)` would create a closure where `a = 5`, such that calling `add5(10)` would return `15` (`a + b`, i.e. `5 + 10`). This would allow for the generation of many similar adding functions. See also: [currying](#currying) and [higher-order function](#higher-order-function).

## Cohesion
Cohesion is the **degree of relatedness of the elements within a module or class**, i.e. how much they belong together. Higher cohesion is preferred, as this groups specific, related behaviour. See also: [coupling](#coupling) and [modularisation](#modularisation).

## Compiler
A compiler is **a program that translates (or *compiles*) code written in one programming language (the *source language*) into another (the *target language*)**, and is a type of [translator](#translator). This process is referred to as *compilation* or *compile time*, e.g. *compile-time operations*.

*Compiler* typically refers to a program that translates [source code](#source-code) from a [high-level language](#high-level-language) to a [low-level language](#low-level-language) (e.g. [assembly language](#assembly-language) or [machine code](#machine-code)). However, there are also other types of compiler, including *cross compilers* (a compiler that runs on one platform but targets another, e.g. another OS) and *source-to-source compilers* (a compiler that translates to another high-level language, e.g. Python to JavaScript, or to another version of the same language, e.g. Python 2 to Python 3).

A compiler is similar to an [interpretor](#interpreter), but they have key differences. A compiler translates the entire program at once, before reporting errors and [executing](#execution) the translated code (which can then be stored and executed independently). In contrast, an interpreter translates and executes the program one [statement](#statement) at a time (always requiring the source code), reporting errors as they are detected (helpful for debugging). Compilers typically execute programs more quickly than interpretors, even though the initial analysis is slower. Typically, different languages are either *compiled* (e.g. Java) or *interpreted* (e.g. Python).

## Concrete class
A concrete class is **a [class](#class) that is fully implemented (including all methods) and can be [instantiated](#instance)**. This contrasts to an [abstract class](#abstract-class), which cannot be instantiated and is instead used as a basis for other classes.

## Concurrency
Concurrency refers to **the ability of different parts of a program to be [executed](#execution) during overlapping time periods (i.e. *concurrently*)**, rather than each part being completed before the next starts (i.e. *sequentially*). Concurrency can apply to computing tasks including [threads](#thread) and [processes](#process).

Concurrency can improve efficiency (i.e. increase tasks completed during a given period of time), responsiveness, and [modularisation](#modularisation). However, *concurrency control* is required to ensure correct behaviour/results from concurrent operations, e.g. by managing the sequence of tasks and coordinating access to shared resources (e.g. [critical sections](#critical-section)). Some languages (e.g. Java) offer specific support for concurrency control, and more specifically for the [synchronisation](#synchronisation) of tasks. Ineffective concurrency control can introduce problems such as [race conditions](#race-condition), [deadlocks](#deadlock), and [resource starvation](#resource-starvation).

## Constant
A constant is **a [value](#value) that should not be altered by the program during normal [execution](#execution)**. Constants are defined a single time and can then be referenced throughout a program. In contrast, a [variable](#variable) contains a value that can be modified. The way to define constants (and variables) varies by language.

A *named constant* is associated with an identifier (e.g. `PI`), while a *[literal](#literal) constant* is a value that is used directly within code (e.g. `3.141`).

## Constructor
A constructor is **a special method that creates an object**. This involves preparing the object for use and [initialising](#initialisation) the object's [member variables](#member-variable). A constructor often has the same name as the declaring [class](#class). Constructors that can accept at least one [argument](#argument) are known as *parameterised constructors*. See also: [object lifetime](#object-lifetime).

## Control flow
Control flow refers to **the order in which the [statements](#statement) within a program are [executed](#execution) or evaluated**. Explicit control flow via *control flow statements* is used within imperative [programming paradigms](#programming-paradigm) (i.e. those that use statements to modify [state](#state)). Control flow statements include conditional statements (e.g. `if` blocks), loops (e.g. `while` loops), and [subroutine](#subroutine) calls. See also: [branch](#branch).

## Coupling
Coupling is the **degree of interdependence between modules or classes**. Lower coupling is preferred, as this means functionality in one module/class doesn’t depend on another. This makes software easier to maintain/develop, as changing something in one module/class won’t require changes in others. See also: [cohesion](#cohesion) and [modularisation](#modularisation).

## Critical section
A critical section is **a portion of a program containing/managing a resource that is protected against [concurrent](#concurrency) access**, i.e. so that it cannot be [executed](#execution) by more than one task (e.g. [process](#process) or [thread](#thread)) at a time. For example, this resource could be a [data structure](#data-structure), network connection, or piece of hardware, where concurrent access could result in unwanted behaviour due to a concurrency issue such as a [race condition](#race-condition). Protection against concurrent access is achieved via [synchronisation](#synchronisation).

## Currying
Currying is **the process of changing a function so that rather than taking multiple [arguments](#argument), it takes a single argument and returns a function which accepts the second argument, and so on**. For example, a division function that returns `n / d` could undergo currying to produce a function, `divisor(d)`, which accepts the number to be *divided by* and returns another function, `numerator(n)`, which accepts the number to *divide* and returns `n / d`. Currying provides a way of automatically managing how arguments are passed to functions and exceptions, and may be required in some cases/frameworks (e.g. analysis).

*Uncurrying* refers to the reverse process. *Partial application* is a similar but distinct process that involves *fixing*/*binding* a number of arguments to a function, producing another function with fewer arguments. For example, a `plus_one` function could fix `1` as the first argument of a function that returns `x + y`. [Closures](#closure) are often used when implementing currying or partial application. See also: [higher-order function](#higher-order-function).

## Database
A database is **a persistent collection of organised data**. Databases can be used when [memory](#memory) is impractical, e.g. for large amounts of data or data that needs to persist beyond a program's execution.

*(Relational) database management systems* (*DBMS* or *RDBMS*) are used to store, access, and modify this data safely (mitigating hazards such as hardware failures and malicious activity); reliably (high uptime and [concurrency](#concurrency)); conveniently (e.g. via [high-level languages](#high-level-language)); and efficiently (i.e. quickly). *Data transactions* should have *ACID* properties: atomicity (transactions complete or fail entirely); consistency (transactions are valid); isolation (transactions have appropriate visibility); and durability (transactions are permanent once committed).

*Schema* is used to define the structure of data (e.g. tables, fields, and relationships), and is set up using a *data definition language* (*DDL*). Once the schema is defined and data is imported, a *data manipulation language* (*DML*) can be used to query/modify/add/remove data. DDLs and DMLs may be sublanguages of a broader language, e.g. *SQL*. There are several types of *database model* which determine a database's structure and operations; [relational databases](#relational-database), based on the *relational model*, are the most widely used.

## Data structure
A data structure is a **collection of data that is organised to allow for efficient processing**, e.g. searching, sorting, and retrieval. More specifically, this comprises a collection of data [values](#value), the relationships among them, and the operations that can be applied to the data. 

Different types of data structures are suited to different types of applications, and can be highly specialised. Common data structures include [arrays/lists](#array), [linked lists](#linked-list), [hash tables](#hashing), [graphs](#graph), stacks (e.g. a [call stack](#call-stack)), and [trees](#tree).

## Data type
A data type is **an attribute of data which informs the [compiler](#compiler) or [interpretor](#interpreter) how the data should be used, based on the language's [type system](#type-system)**. More specifically, this includes primitive types (e.g. Booleans and integers) and composite types (derived from multiple primitive types, e.g. arrays). Also known as *type*.

## Deadlock
A deadlock is **a [concurrency](#concurrency) issue where each member of a group of tasks (e.g. [processes](#process) or [threads](#thread)) waits for another task, including itself, to take action**. Typically, a deadlock occurs when a task enters a waiting state because a requested resource is held by another waiting task, which in turn is waiting for another resource held by another waiting task, and this state continues indefinitely. 

A deadlock can only arise if all four *Coffman conditions* occur simultaneously: *mutual exclusion* (at least two resources held in a non-shareable mode); *hold and wait* or *resource holding* (a task is currently holding at least one resource and requesting additional resources which are being held by other tasks); *no preemption* (a resource can be released only voluntarily by the task holding it); and *circular wait* (each task is waiting for a resource which is held by another task, which in turn is waiting for the first task to release the resource). 

A deadlock may not occur under these conditions if a system has multiple instances of resources. Deadlocks can be handled by simply ignoring them (if they are very rare and/or the impact is minimal), by detecting and resolving them, or by attempting to prevent one or more of the Coffman conditions. See also: [resource starvation](#resource-starvation).

## Declaration
A declaration is **a unit of syntax that specifies the properties of an identifier**, i.e. it defines the identifier itself (the name) and what it means, such as the entity (e.g. function or variable) and [value](#value). Declarations are used to define [variables](#variable), [constants](#constant), [subroutines](#subroutine), [classes](#class), and other entities. A declaration is used to announce the existence of the entity to the [compiler](#compiler) or [interpreter](#interpreter).

## Decompiler
A decompiler is **a program that [translates](#translator) code from a [low-level language](#low-level-language) into a [high-level language](#high-level-language)**, i.e. the opposite of a [compiler](#compiler). Decompilers are typically unable to perfectly recreate the original [source code](#source-code), and often produce [obfuscated](#obfuscation) code. However, they are an important tool for [reverse engineering](#reverse-engineering) a program. See also: [disassembler](#disassembler).

## Decomposition
Decomposition involves **breaking down a complex problem/system into parts that are easier to understand, develop, and maintain**. Also known as *factoring*. For example, a complex task may be decomposed into several [subroutines](#subroutine), each with a single, specific purpose. Similarly, a program may be broken down into [classes](#class) that are responsible for and/or represent a specific part of the problem domain. See also: [modularisation](#modularisation).

## Defensive programming
Defensive programming refers to **a set of programming practices that intend to ensure the continuing function of software following misuse or (other) unforeseen circumstances**. These practices are typically used when high availability (e.g uptime), safety, or security are particularly important for an application. Specific techniques include documented specifications/contracts (*design by contract*), assertions, exceptions, encryption, and specific mitigations against known security vulnerabilities. 

Defensive programming can reduce bugs, improve predictability (particularly in response to unexpected or unlikely user inputs/actions), and improve readability. However, excessively defensive programming (e.g. against extremely unlikely inputs/situations) can make programs unnecessarily complex or more difficult to maintain. 

*Offensive programming* is a branch of defensive programming which emphasises that errors from within the program's *line of defence* (e.g. invalid function arguments) should not be handled defensively (i.e. errors are preferable to tolerance), while other potential errors (e.g. user input or hardware failures) should still be handled defensively.

## Design pattern
A design pattern is a **software development pattern that can be used to solve a common design problem**. These patterns are used as general templates or guidelines, and can be applied to many different situations. Design patterns were popularised by the *Design Patterns: Elements of Reusable Object-Oriented Software* book, published in 1994 by the "Gang of Four", which outlined 23 classic patterns for use in [object-oriented programming](#object-oriented-programming).

Design patterns are recognised as best-practice solutions when used appropriately, and can speed up the design/development process, although they still have limitations/trade-offs. For example, the *Singleton* pattern can be used to ensure that only a single [instance](#instance) of a [class](#class) is created and that there is a global point of access to it. In contrast, [anti-patterns](#anti-pattern) are commonly used but almost always represent poor design.

## Disassembler
A disassembler is **a program that [translates](#translator) code from [machine code](#machine-code) into [assembly language](#assembly-language)** i.e. the opposite of an [assembler](#assembler). Disassemblers are typically unable to perfectly recreate the original assembly language code, e.g. the original constants and comments (which are usually stripped out during assembly). However, they are a useful tool for [reverse engineering](#reverse-engineering) a program. See also: [decompiler](#decompiler).

## Encapsulation
Encapsulation is an [object-oriented programming](#object-oriented-programming) concept that can refer to the **bundling of data with the [methods](#method) that operate on this data within a single unit** (e.g. a class or module) or to the **restriction of direct access to some of an object's components**.

The former concept relates to [modularisation](#modularisation), i.e. [decomposing](#decomposition) a program into independent software components. The latter concept is an implementation of [information hiding](#information-hiding) that involves hiding the internal representation or [state](#state) of an object, to reduce complexity and prevent invalid/unwanted use of an object. More specifically, public methods (e.g. "getters" and "setters") provide a stable [interface](#interface) that allows for indirect access or modification of an object's state, while private methods are only used internally and are more likely to change.

[Abstraction](#abstraction) is a similar concept that relates to an object's observable behaviour, i.e. how the object and its behaviour are presented to the user.

## Execution
Execution is **the process by which a computer or [virtual machine](#virtual-machine) reads and acts on the [machine code](#machine-code) instructions of a computer program**. Execution involves repeatedly following a *fetch–decode–execute* cycle (also known as the *instruction cycle*) for each instruction, during *run time*. This process will continue until the program terminates or crashes.

## Expression
An expression is **a unit of [syntax](#syntax) that can be evaluated to determine its [value](#value)**. Expressions comprise one or more [constants](#constant), [variables](#variable), [subroutines](#subroutine), and/or [operators](#operator). For example, `2 + 3` is a simple expression. In contrast, [statements](#statement) are units of syntax that are *[executed](#execution)*.

## First-class citizen
A first-class citizen is **an entity (e.g. type, object, or function) that supports all of the operations that are generally available to other entities in a given language**. These operations typically include being passed as an [argument](#argument), returned from a [subroutine](#subroutine), and assigned to a [variable](#variable).

## Function composition
Function composition refers to **the ability to combine functions to build more complex ones**. More specifically, functions are applied directly to the results of other functions; the result of a function is passed as the [argument](#argument) to the next one, and execution of the final function in the chain produces the ultimate result. Function composition is possible in most languages, and is a key concept in [functional programming](#functional-programming). See also: [closure](#closure) and [currying](#currying).

## Function overloading
Function overloading involves **differentiating the behaviour of a function or [method](#method) based on the passed [arguments](#argument)**, where multiple functions/methods can be defined with the same name but unique [signatures](#type-signature). Also known as *method overloading*. This allows a single function/method to perform different tasks depending on how it is being used, and is a type of [polymorphism](#polymorphism). For example, a `print()` function could produce a different output depending on the argument [type](#data-type).

Where a passed object's type changes a method's behaviour, this can be considered a special type of [method overriding](#method-overriding).

## Functional programming
Functional programming is **a [programming paradigm](#programming-paradigm) that involves creating programs using the [composition](#function-composition) of concise, [first-class](#first-class-citizen) and [higher-order](#higher-order-function) functions that do not have [side effects](#side-effect)**. Other common concepts include the use of [recursion](#recursion) rather than loops, and variable values that do not change once defined (resulting in *referential transparency*). Functional programming is an *declarative* paradigm, i.e. it expresses the logic of a computation but not its [control flow](#control-flow) (*what* the program should accomplish, but not *how*). Many languages support functional programming, such as JavaScript and Haskell.

*Purely functional programming* may be used synonymously or considered to be a more rigid subtype of functional programming, e.g. this may require using only [pure functions](#pure-function).

Functional programming can be considered to be easier to understand and more easily maintainable (e.g. testing and debugging) than other paradigms (e.g. [object-oriented-programming](#object-oriented-programming)), resulting in its increasing popularity in recent years. However, it may be less appropriate/more cumbersome for some tasks and may be less efficient than other paradigms.

## Garbage collection
Garbage collection is **a type of automatic [memory](#memory) management that attempts to reclaim memory which was allocated by the program but is no longer referenced**. This *garbage* refers to data (e.g. objects) which will not be used during the rest of the program [execution](#execution), and so the memory associated with it can be *deallocated*/*released* and reused. Most [high-level languages](#high-level-language) offer some form of automatic garbage collection.

Automatic garbage collection requires less effort from programmers and avoids errors associated with manual memory management (e.g. deallocation of memory from an object that is still referenced). However, identifying memory for deallocation consumes memory itself, resulting in [overhead](#overhead) that can significantly decrease performance and/or its consistency.

## Global variable
A global variable is **a [variable](#variable) that has global [scope](#scope)**, and is therefore in [memory](#memory) and accessible by all of the program's objects and [subroutines](#subroutine) (unless [shadowed](#variable-shadowing)) throughout the program's [execution](#execution), unlike [local variables](#local-variable). The set of all global variables is known as the *global environment* or *global state*.

Global variables can be changed by any subroutine at any point, so their use can potentially cause unwanted [side effects](#side-effect) that can be difficult to debug. As such, they should only be used when necessary or particularly useful.

## Graph
A graph is **a non-linear [data structure](#data-structure) comprised of *vertices* (also called *nodes*) and *edges* (also called *links* or *lines*), where edges connect pairs of *adjacent* vertices**. In addition to vertices, edges may have an associated *edge value*. Graphs can be *undirected* or *directed*, depending on whether edges point from one vertex in a pair to the other. Graphs can also be categorised as *dense* or *sparse*, depending on the number of edges relative to possible edges, though the precise definition varies.

Graphs are commonly implemented as an *adjacency list* or an *adjacency matrix*. Implementations vary in how the relationships between vertices are represented. For example, in an adjacency list each vertex stores a list of adjacent vertices. Graphs are commonly used to model real-world networks, e.g. people in a social media application. See also: [tree](#tree).

## Hashing
Hashing is **the process of mapping keys and values into a *hash table* [data structure](#data-structure) via a *hash function***. Hashing allows for faster access to elements, typically constant average case [time complexity](#time-complexity), depending on the efficiency of the hash function used. Aside from efficiency, hashing plays an important role in encryption.

Specifically, a hash function is responsible for generating a representative (but concise) *hash code* or *index* from data (e.g. a string). The original data can be used as a *key* to generate the index, which represents a storage location (*bucket*) within a hash table. The associated index value represents some attribute, such as whether the original data is present. For example, the string `'hello'` could be hashed to produce the index `85121215`, where the associated value `1` could indicate that the string is present in the database. (Although in practice, the index is typically much more concise than the key.)

Ideally, a hash function would assign each key to a unique bucket. In practice, hash functions can sometimes generate the same index for more than one key, resulting in potential *hash collisions*. As such, *collision avoidance* is important in hashing applications, e.g. including references to multiple keys/values within a bucket.

## High-level language
A high-level language is **a language with strong [abstraction](#abstraction) from the details of the computer** (e.g. [memory addresses](#memory) and [call stacks](#call-stack)), such as Python and Java. These languages typically use intuitive [syntax](#syntax), may automate or hide some aspects of computing (e.g. memory management), and are generally designed to be easy to read and write by humans. However, the abstraction of higher-level languages often makes code less efficient/optimised (the *abstraction penalty*).

High-level languages are used to produce human-written [source code](#source-code), which is then [translated](#translator) (via [compilation](#compiler) or [interpretation](#interpreter)) into a [low-level language](#low-level-language) for [execution](#execution) by the [central processing unit](#central-processing-unit).

## Higher-order function
A higher-order function is **a function with at least one [parameter](#parameter) that accepts a function (a *procedural parameter*) and/or a function that returns a function**. The use of higher-order functions is common in [functional programming](#functional-programming). The functions passed to and from higher-order functions are often [anonymous](#anonymous-function).

In contrast, functions that do not meet at least one of these criteria are known as *first-order functions*. See also: [closure](#closure) and [currying](#currying).

## Idempotence
Idempotence describes **an operation that can be applied multiple times without changing the result, given the same input(s)**. In other words, the result/effect of an *idempotent operation* will be the same regardless of the number of times the operation occurs (although the internal operation might change). 

For example, sending a request to delete an item from a database may be idempotent (i.e. the item is deleted regardless of the number of requests), while returning the current system time is not (i.e. the time will change). See also: [functional programming](#functional-programming) and [pure function](#pure-function).

## Information hiding
Information hiding involves **segregating the design decisions in a program that are most likely to change**, so that the wider program and any external (client) applications do not need to be significantly modified if a given design changes. This involves providing a stable [interface](#interface) which protects against issues that could arise from using the (less static) implementation, e.g. if a modification breaks functionality.

Information hiding is closely related to [encapsulation](#encapsulation). Information hiding can be considered to be a principle while encapsulation is a specific technique/implementation, but the two terms are often used interchangeably. [Abstraction](#abstraction) is also a similar concept.

## Inheritance
Inheritance refers to the **ability of an object to acquire (i.e. inherit) properties and/or behaviour from other objects**, as defined by the object's [class](#class). This involves modelling objects based on their relatedness and specificity (an “*is a*” relationship), where more specific objects (*subclass* or *child class*, e.g. Rectangle) inherit from more general objects (*superclass* or *parent class*, e.g. Shape). This can minimise repeated code. Specific mechanisms of inheritance include [method overriding](#method-overriding) and [multiple inheritance](#multiple-inheritance).

[Object composition](#object-composition) is often considered preferable to inheritance ("composition over inheritance") unless objects have a strong "*is a*" relationship (e.g. most of the parent class [interface](#interface) is shared), to increase flexibility and make it easier to modify the program later.

## Initialisation
Initialisation is **the assignment of an initial [value](#value) to an object or [variable](#variable)**. Object initialisation is achieved via a [constructor](#constructor) or an initialiser. See also: [object lifetime](#object-lifetime).

## Instance
An instance is **a specific occurrence (or realisation) of a [class](#class)**, including its [member variables](#member-variable). Also known as a *class instance*, *class object*, *instance object*, or simply *object*. In contrast, a class is a template that is used to create one or more instances. The creation of an instance is called *instantiation*.

## Interface
An interface is **the collection of well-defined entry points for interacting with an object, module, or program**. In the case of objects, the entry points are the public [methods](#method) defined by the object's [class](#class), i.e. those available for external use. In the case of modules/programs, this could refer to the [concrete classes](#concrete-class) and functions. Using interfaces without relying on internal implementations is known as *programming to the interface*.

This relates to the practices of [information hiding](#information-hiding) and [encapsulation](#encapsulation), which involve providing a stable, publicly usable interface while segregating the internal implementations that are more likely to change. The creation of stable interfaces can also facilitate [polymorphism](#polymorphism).

*Interface* can also be used more specifically to refer to the (incomplete) methods and associated [type signatures](#type-signature) defined within an [abstract class](#abstract-class), which can then be *implemented* by a [concrete class](#concrete-class). This type of interface is also known as a *protocol*.

## Interpreter
An interpreter is **a program that translates [source code](#source-code) written in one programming language (the *source language*) into another (the *target language*)**, and is a type of [translator](#translator). 

An interpreter is similar to a [compiler](#compiler), but they have key differences. A compiler translates the entire program at once, before reporting errors and [executing](#execution) the translated code (which can then be stored and executed independently). In contrast, an interpreter translates and executes the program one [statement](#statement) at a time (always requiring the source code), reporting errors as they are detected (helpful for debugging). Compilers typically execute programs more quickly than interpretors, even though the initial analysis is slower. Typically, different languages are either *compiled* (e.g. Java) or *interpreted* (e.g. Python).

## Invariant
An invariant is **an [expression](#expression) whose [value](#value) doesn't change during the [execution](#execution) of a program, or during a specific phase of it**. Invariants are fundamentally useful as they can be relied on to be true, and are also helpful when checking correct program behaviour. Assertions can be used to make invariants explicit, e.g. asserting that a value is of a specific [type](#data-type).

A *class invariant* (or *type invariant*) is an invariant used for constraining instances of a [class](#class), and should be maintained between calls to public [methods](#method) (but may be temporarily broken during a method) regardless of the object's [state](#state). Class invariants are also [inherited](#inheritance). A *loop invariant* is a property of a loop that is true before (and after) each iteration, and can aid understanding of the loop's purpose/effect.

## Linked list
A linked list is **a linear [data structure](#data-structure) comprised of elements (or *nodes*) that point (i.e. *link*) to the next element in the sequence**, despite not necessarily being adjacent in [memory](#memory). A basic linked list node comprises data and a reference to the next node, while more complex versions may include additional references. The first node is called the *head*.

Linked lists allow for efficient insertion or removal of elements from any position in the sequence during iteration. Elements can be easily inserted or removed without reorganising the entire structure, in contrast to an [array](#array) where this requires computationally expensive memory reallocation. However, many basic operations require iterating through the entire linked list (*sequential access*), unlike arrays (which support more efficient *direct access*, also known as *random access*).

## Linker
A linker is **a program that combines multiple [object files](#object-code) (generated via [translation](#translator)) into a single executable file, library file, or another object file** (i.e *linking*). This process includes resolving cross-references between the files. See also: [assembler](#assembler).

## Literal
A literal is **a unit of [syntax](#syntax) used to represent a fixed [value](#value) within code**. Most (if not all) primitive [types](#data-type) in a language can be represented as literals. For example, in the [statements](#statement) `n = 1` and `s = "cat"`, `1` is an integer literal and `"cat"` is a string literal.

## Loader
A loader is **a program that writes the [machine code](#machine-code) of a program to [memory](#memory) and prepares for its [execution](#execution)** (i.e. *loading*). Once this process is complete, control is passed to the loaded program code. See also: [process](#process).

## Local variable
A local variable is **a [variable](#variable) that has local [scope](#scope)**, and is therefore only accessible by objects/functions within the same scope (e.g. a function or block) and only in [memory](#memory) during the local [subroutine's](#subroutine) [execution](#execution), unlike [global variables](#global-variable). Local variable names can [shadow](#variable-shadowing) the same names used in the wider scope.

Local variables are usually preferable to global variables, as they do not affect non-local [state](#state). As such, their use can avoid unintended [side effects](#side-effect) that may be difficult to debug.

## Logic programming
Logic programming is **a [programming paradigm](#programming-paradigm) that involves using formal logic to describe rules about a problem domain and their relation** (via *logical clauses*). These rules are then evaluated and an attempt is made to prove the logic. Logic programming is an *declarative* paradigm, i.e. it expresses the logic of a computation but not its [control flow](#control-flow) (*what* the program should accomplish, but not *how*).

Logic programming may be useful for specialised tasks such as proving theorems, and other applications where formal logic is a key consideration. Logic programming languages include Prolog, ASP, and Datalog.

## Low-level language
A low-level language is **a language with little or no [abstraction](#abstraction) from the details of the computer** (e.g. [memory addresses](#memory) and [call stacks](#call-stack)), and typically refers to either [assembly language](#assembly-language) or [machine code](#machine-code). These languages lack the intuitive [syntax](#syntax) and other features (e.g. automatic memory management) of [high-level languages](#high-level-language), but are more efficient/optimised (i.e. due to the *abstraction penalty*). Low-level languages may (e.g. assembly language) or may not (e.g. machine code) be easily readable by humans.

High-level languages (i.e. [source code](#source-code)) can be [translated](#translator) into a low-level language (i.e. [object code](#object-code)), but low-level language code (most commonly assembly language) can also be written directly.

## Machine code
Machine code is **any [low-level language](#low-level-language) which is used to directly control a computer's [central processing unit](#central-processing-unit) (CPU).** Also known as *first-generation language*. Machine code is produced via [compilation](#compiler) of a [high-level language](#high-level-language) (i.e. [source code](#source-code)) and/or [assembly](#assembler) from [assembly language](#assembly-language) (which are both types of [translation](#translator)). 

Each machine code instruction (part of the broader *instruction set architecture*) causes the CPU to perform a specific task when [executed](#execution), such as a load, a store, a jump, or an arithmetic logic unit operation on one or more units of data. Machine code is a numerical language which is designed to run as fast as possible, and so is not (easily) readable by humans (unlike the corresponding assembly language).

## Member variable
A member variable is **a [variable](#variable) that is associated with a specific object**, and is accessible by all of the object's [methods](#method). Also known as a *member field*, *attribute*, or *property*.

More specifically, member variables can be *class variables* (also known as *static member variables*) or *instance variables*. For multiple [instances](#instance) of a [class](#class), a class variable is shared by all instances (i.e. the variable exists as a single, static copy). In contrast, each instance has its own copy of an instance variable, which can be modified independently of other instances.

## Memory
Memory is **a device or system that is used to store data for immediate/current use in a computer**. A *memory address* is a reference to a specific location in memory, represented by a sequence of digits. 

*Memory management* involves allocating portions of memory to programs and their data (from a pool of memory known as the *heap*), and releasing it for reuse when no longer needed. Memory management can be automatic (e.g. [garbage collection](#garbage-collection)) or manual. Incorrect memory management can result in a *memory leak*, where unneeded memory isn't released, potentially causing performance issues. See also: [overhead](#overhead) and [process](#process).

## Message passing
Message passing refers to **the sending of a message from a program to a [process](#process) which invokes behaviour via the appropriate code**. Message passing does not directly invoke the code that ultimately runs (e.g. via a [subroutine](#subroutine) call). Instead, the recipient of the message interprets it and invokes the appropriate behaviour. As such, this can be considered a form of [encapsulation](#encapsulation). Message passing plays an important role in networks such as the internet.

Message passing often uses an *object model*, i.e. an [object-oriented](#object-oriented-programming) [interface](#interface), to distinguish general functionality from the specific implementation (e.g. via [polymorphism](#polymorphism)). This can involve either *local* or *distributed* objects; in the latter case, the sender and receiver may be located on different computers and may use different technologies (e.g. operating systems and languages). In addition, message passing can be *synchronous* (objects running at the same time) or *asynchronous* (the recipient may be busy or not running). Message passing is commonly implemented via *channels*. See also: [concurrency](#concurrency).

## Method
A method is **a [subroutine](#subroutine) that is associated with an object** (similar to a function), as defined or [inherited](#inheritance) by the object's [class](#class). Some methods are used to manage the creation and destruction of objects (*managers*, e.g. *constructors* and *destructors*); access the property values of an object (*accessors* or "getters"); and modify the property values of an object (*mutators* or "setters"). [Abstract classes](#abstract-class) may also provide incomplete *abstract methods*.

Methods can be *instance methods*, *class methods*, or *static methods*. Instance methods apply to the specific class [instance](#instance), i.e. the standard method type. Class methods are called on the class rather than the instance. Static methods are intended to be relevant to all the instances of a class rather than to any specific instance. Methods can also vary in their external availability (e.g. `public` or `private`), which can be used to achieve [encapsulation](#encapsulation). However, note that the available method types/privacies and their behaviour varies across languages.

## Method overriding
Method overriding is **a mechanism that allows a subclass to redefine the implementation of a [method](#method) that is [inherited](#inheritance) from a superclass**. This allows [classes](#class) to share the same method name (e.g `speak()`) but change the implementation (e.g. in an `Animal` superclass vs `Dog` and `Cat` subclasses). This is a type of [polymorphism](#polymorphism) (subtyping) that can be used to provide a consistent and stable [interface](#interface). Although the method body is overridden, the [parameters](#parameter) and return [type](#data-type) should remain the same.

## Mixin
A mixin is **a [class](#class) that contains [methods](#method) that are designed for use by (i.e. *mixed into* or *included in*) other classes**. Unlike standard [inheritance](#inheritance), using mixins does not model an “*is a*” relationship between the mixin and classes that use its methods. 

The use of mixins can be considered a special type of [multiple inheritance](#multiple-inheritance), where only the required mixin methods are included within a class, and can avoid the *diamond problem* (if *B* and *C* [override](#method-overriding) a method inherited from *A*, which version of the method does *D* inherit from *B* and *C*?). As with multiple inheritance, mixins are only available in some languages (e.g. Python).

Where the same functionality is required across many unrelated classes (i.e. it wouldn't be appropriate to use standard inheritance), mixins can increase code reusability. Mixins can also be used to group related functionality into modules (i.e. [modularisation](#modularisation), to improve [cohesion](#cohesion)), even if this functionality is required across many different classes/modules.

## Model View Controller (MVC)
Model View Controller (MVC) is **a [design pattern](#design-pattern) that is commonly used to implement user [interfaces](#interface), including web applications**. MVC splits up program logic based on its key responsibilities: the *model* represents and directly manages the application's data and logic; the *view* represents the model via a user interface; and the *controller* converts user input into logic that acts on the model or view. See also: [abstraction](#abstraction).

## Modularisation
Modularisation involves **[decomposing](#decomposition) an application into specific modules (i.e. software components)**, where each module is designed to perform necessary tasks independently of the others. Also known as *modular programming* or more generally as *compartmentalisation*. This process can reduce repetition, increase [cohesion](#cohesion), and reduce [coupling](#coupling).

Modularisation relates to the *separation of concerns (SoC)* design principle, i.e. separating a program into distinct sections that each address a single *concern* (a set of information that affects the code of a program, e.g. a database interaction or a calculation). See also: [encapsulation](#encapsulation).

## Multiple inheritance
Multiple inheritance refers to **the ability of an object to [inherit](#inheritance) properties and/or behaviour from multiple parent [classes](#class)**, a feature that is available in some languages (e.g. Python). The use of [mixins](#mixin) is a special type of multiple inheritance that allow methods to be *mixed into* other classes without requiring an “*is a*” relationship.

The use of multiple inheritance is controversial, as it can increase complexity and result in the *diamond problem*. This refers to cases where it is unclear which parent an object's feature is inherited from. Specifically, this occurs when a feature (e.g. method) is shared across both parents, who inherited and [overrode](#method-overriding) it from their own parent (i.e. the object's grandparent). This pattern of divergent and convergent inheritance can be visualised as a diamond. However, many languages attempt to mitigate these issues. 

## Mutability
Mutability refers to **the ability of an object to be changed (mutable) or not (immutable) after creation**. For example, strings are typically immutable, while lists/arrays are typically mutable.

## Name resolution
Name resolution is **the linking of identifiers (e.g. function calls and variables) within program [expressions](#expression) and [statements](#statement) to the intended program components**.

[Scope](#scope) is very significant for name resolution, e.g. to assess if an identifier is valid and to determine the correct component where the same identifier is used to represent different components (e.g. [variable shadowing](#variable-shadowing)). Other contributing factors include accessibility/visibility of an identifier from the current context and [overloading](#function-overloading). A *namespace* or *name scope* refers to the context of a group of identifiers, where each name must have a single meaning within that namespace.

Name resolution can occur during [compilation](#compiler) (*static name resolution*) or during [execution](#execution) (*dynamic name resolution*). A *naming collision* occurs if two or more identifiers cannot be unambiguously resolved (but need to be).

## Obfuscation
Obfuscation is **the act of creating code that is difficult for humans to understand**. For example, this could be achieved by making code unnecessarily verbose, removing comments, and using non-descriptive [variable](#variable) names. Obfuscation is typically achieved via an automated tool.

Obfuscation is typically used to conceal a program's purpose or logic (*security through obscurity*) and to discourage [reverse engineering](#reverse-engineering). It can also be used to reduce resource file sizes (e.g. JavaScript) to improve website loading speeds. [Decompilation](#decompiler) often produces obfuscated code.

## Object-oriented programming
Object-oriented programming (OOP) is **a [programming paradigm](#programming-paradigm) based on the concept of objects, which have associated data ([member variables](#member-variable)) and functionality ([methods](#method))**. OOP is an *imperative* paradigm, i.e. it uses [statements](#statement) to change program [state](#state). Programs written using OOP largely consist of objects (typically [instances](#instance) of [classes](#class), i.e. *class-oriented programming*) that interact with themselves (i.e. *self*) and each other. Many languages support OOP, such as Java.

Key concepts in OOP include [abstraction](#abstraction), [encapsulation](#encapsulation), [inheritance](#inheritance), [object composition](#object-composition), [polymorphism](#polymorphism), and [design patterns](#design-pattern). Benefits of OOP include flexibility (compared to some more rigid paradigms) and scalability (e.g. via inheritance and composition). However, some criticise the complexity/inefficiency and lack of [modularity](#modularisation) (despite this being a goal of OOP) that OOP can lead to.

## Object code
Object code refers to **the product of a [compiler](#compiler) or an [assembler](#assembler)** (types of [translator](#translator)). Also known as an *object file* or *object module*. It is a somewhat generic term to describe the result/goal of the compilation/assembly process. Object code is typically written in [machine code](#machine-code), a [low-level language](#low-level-language). [Source code](#source-code) is the inverse of object code (i.e. the input).

## Object composition
Object composition is a **method of combining objects or [data types](#data-type) into more complex ones**. For example, an object (e.g. "Address") can be used to represent one of the properties of another object (a “*has a*” relationship), to share similar functionality across otherwise unrelated objects. This aligns with the concept of modelling and minimises repeated code.

Object composition is often considered preferable to [inheritance](#inheritance) ("composition over inheritance") unless objects have a strong "*is a*" relationship (e.g. most of the parent [class](#class) [interface](#interface) is shared), to increase flexibility and make it easier to modify the program later.

## Object lifetime
An object lifetime refers to **the time and events starting from an [object's](#instance) creation up until and including its destruction**. Also known an an *object lifecycle*. A specific object's lifetime may differ between different runs of the same program, while object lifetimes vary more generally between languages.

Object creation (also known as *construction* or *instantiation*) typically involves [memory](#memory) allocation and [initialisation](#initialisation), and may be carried out by a [constructor](#constructor). Object destruction typically involves finalisation (clean-up tasks) and memory deallocation. In some cases, an object may not be specifically destroyed (i.e. until the program finishes [executing](#execution)).

## Operator
An operator is **a unit of [syntax](#syntax) that is used to determine an action to perform**. Operators are used within [expressions](#expression) and (broader) [statements](#statement). They are similar to [subroutines](#subroutine) (i.e. provide functionality) but differ in their unique syntax/usage. An *operand* is the item (e.g. a [variable](#variable)) being operated on, e.g. `x` in `x = x + 3`. 

The main types of operator are *mathematical* (e.g. `+` and `*`), *comparison* (e.g. `==` and `<`), *logical* (e.g. `AND` and `OR`), and *assignment* (e.g. `=`). Most languages have a built-in set of operators but do not allow user-defined operators.

## Overhead
Overhead refers to **the resources (e.g. [memory](#memory) and [central processing unit](#central-processing-unit) time) required to facilitate or perform an operation, or resources that are required by the technology/approach being used but do not directly contribute to the result**. The term is often used in the context of significant and/or excessive resource use, where the amount of overhead may be contrasted with the value and/or complexity of the operation, e.g. a program feature or even a bug fix. See also: [time complexity](#time-complexity).

## Parameter
A parameter is **a [variable](#variable) used within a [subroutine](#subroutine) definition**. In contrast, an [argument](#argument) refers to a value that is passed into a subroutine (i.e. when the subroutine is called). However, *argument* and *parameter* are often used interchangeably. Also known as a *formal argument*. See also: [type signature](#type-signature).

## Polymorphism
Polymorphism is the **ability of a program to use the same [interface](#interface) for different [data types](#data-type) or [classes](#class)**. For example, a `Dog` and `Cat` class could both have a `speak()` method [inherited](#inheritance) from an `Animal` superclass, which could be used without knowing the type of shape being acted upon (subtyping, implemented via [method overriding](#method-overriding)). As another example, a function’s behaviour could change depending on the supplied argument [types](#data-type), e.g. the `+` operator can be used to add integers and concatenate strings (ad hoc polymorphism).

## Procedural programming
Procedural programming is **a [programming paradigm](#programming-paradigm) that involves specifying the steps that a program must take to achieve a desired [state](#state), focusing on the use of procedures**. Procedures are a type of [subroutine](#subroutine) that perform an action (i.e. produce a [side effect](#side-effect)) but do not return a value. Procedural programming is an *imperative* paradigm, i.e. it uses [statements](#statement) to change program [state](#state). It also makes considerable use of [control flow](#control-flow) statements such as loops and conditional statements. Most widely-used languages support procedural programming.

Procedural programming is very flexible and relatively simple to implement, but may not offer the same benefits as other paradigms such as [object-oriented programming](#object-oriented-programming) (e.g. scalability) or [functional programming](#functional-programming) (e.g. maintainability).

## Process
A process is **the instance of a program that is being [executed](#execution) by one or more [threads](#thread)**. A process comprises the program code and its activity. Depending on the operating system, a process may be made up of multiple threads of execution that run [concurrently](#concurrency) (i.e. *multithreading*). *Task* is often used as a more generic synonym. See also: [central processing unit](#central-processing-unit), [loader](#loader), and [memory](#memory).

## Program lifecycle
A program lifecycle refers to **the different stages associated with program development, distribution, and execution**. However, these stages do not always occur and/or may occur in different orders. This occurs within the broader *software development life cycle (SDLC)*.

Lifecycle  phases include *edit time* ([source code](#source-code) writing and editing), *compile time* ([compilation](#compiler)), *link time* ([linking](#linker)), *distribution time* (distributing the program to users), *installation time* (installing the program on a user's computer), *load time* ([loading](#loader)), and *run time* ([execution](#execution)).

## Programming paradigm
A programming paradigm refers to **a style of programming, independent of a specific language**. This includes factors such as how code is [executed](#execution) (the *execution model*), how code is organised, and the style of [syntax](#syntax). 

There are many programming paradigms, most of which can be classified as either *imperative* or *declarative*. Imperative paradigms (e.g. [object-oriented programming](#object-oriented-programming) and [procedural programming](#procedural-programming)) use [statements](#statement) to change a program's [state](#state), and describe *how* a program operates. Declarative paradigms (e.g. [functional programming](#functional-programming) and [logic programming](#logic-programming)) express the logic of a computation but not its [control flow](#control-flow), and describe *what* the program should accomplish.

Languages can be classified into one or more paradigms. For example, Haskell is a purely functional language that supports functional programming, while C++ supports multiple paradigms (e.g. object-oriented programming and procedural programming).

## Pure function
A pure function is **a function that is [idempotent](#idempotence) (can be applied multiple times with the same input without changing the result) and has no [side effects](#side-effect) (modifications of non-local [state](#state))**. 

For example, a function that returns the maximum of two numbers may be a pure function. In contrast, a function that returns the current system time (no side effects but not idempotent) is not pure. Similarly, a function that requests the deletion of a database item (idempotent but has side effects) is not pure. See also: [functional programming](#functional-programming).

## Race condition
A race condition refers to **a situation where correct program behaviour depends on the sequence or timing of operations in [concurrent](#concurrency) [processes](#process) or [threads](#thread)** (which will typically depend on a process/thread scheduling algorithm). As a result, race conditions can lead to unpredictable bugs that are difficult to reproduce and resolve. Race conditions often occur when processes/threads depend on the [state](#state) of a shared resource (e.g. [data structure](#data-structure) or [variable](#variable)) that should be protected against concurrent access by a [critical section](#critical-section).

For example, if two concurrent threads in an investment app attempted to collectively (but not individually) spend more than the cash balance, this could either fail (as intended) or succeed (as a bug due to a race condition). If the balance check and purchase in one thread occurred before the balance check and purchase in the other, the second purchase would be declined. However, if both threads' balance checks occurred before both threads' purchases, both purchases would continue despite the second bringing the balance below zero.

[Synchronisation](#synchronisation) and other concurrency control techniques can be used to avoid race conditions. See also: [deadlock](#deadlock) and [resource starvation](#resource-starvation).

## Recursion
Recursion refers to **the ability of a [subroutine](#subroutine) to call itself**, and is typically used to [decompose](#decomposition) a problem into smaller parts. As with other subroutine calls, recursion is managed via the [call stack](#call-stack). Recursion is a natural solution to some problems, e.g. for implementing a merge sort [algorithm](#algorithm), and is commonly used in [functional programming](#functional-programming). 

Valid recursive subroutines require at least one *base case* (a stopping condition without recursion) and at least one *recursive case* (also known as a *general case*). The result contributed by the first item within the current [data structure](#data-structure) can then be combined with the result of the recursive call(s) to produce the overall solution. *Single recursion* uses only one recursive case, in contrast to *multiple recursion*. *Indirect recursion* or *mutual recursion* involves one subroutine calling another, which then calls the original subroutine (directly or indirectly via other subroutines).

*Iteration*, implemented by loops, is often contrasted with recursion. Problems that can be solved with recursion can also be solved via iteration, and vice versa, although the efficiency and readability of the solutions may vary. For example, a list/array can either be iterated over via a loop or operated on recursively based on the data structure having a *head* (the current item) and *tail* (all remaining items).

## Relational database
A relational database is **a widely-used type of [database](#database) based on the *relational model*, consisting of a set of named *relations* (also known as *tables*) and the data contained within them**. Each relation contains a set of named *attributes* (also known as *fields* or *columns*), each with an associated *type* (also known as *domain*), and *tuples* (also known as *records* or *rows*) that contain a set of values corresponding to each attribute. For example, for the attributes `name` (string) and `id` (integer), a tuple might have the corresponding values `"Bob"` and `123`. 

A *key* is an attribute that is comprised of unique values, i.e. no tuples have the same value for the attribute (e.g. `id`). Alternatively, multiple attributes whose combined values are unique can be used as a key. Keys can be used to identify specific tuples and to link/look up data across different relations (e.g. a customer ID within a customer relation and a transaction relation). The special value `NULL` is used where a value within a tuple is undefined.

*SQL* is the most widely used language for accessing/managing relational databases. SQL is a [declarative language](#programming-paradigm), i.e. syntax is used to declare *what* the desired outcome is rather than describe *how* it should be achieved.

## Resource starvation
Resource starvation refers to **a [concurrency](#concurrency) issue where a [process](#process) is continually denied one or more resources that it requires to progress**. Starvation is often caused by an overly simple or poorly designed scheduling algorithm, where higher-priority processes are continually prioritised at the expense of lower-priority ones. Resource starvation can be avoided by incorporating *ageing*, i.e. considering a process' current waiting time when assessing its priority.

A *livelock* can be considered a special type of resource starvation, where two or more processes continually repeat the same interactions/state changes in response to each other, but do not progress in a meaningful way. Livelock can be avoided by ensuring that only one process is allowed to take action. See also: [deadlock](#deadlock).

## Reverse engineering
Reverse engineering is **a process that aims to understand how an application functions, without or in addition to reading its [source code](#source-code)**. This process may be used as part of competitor analysis or to otherwise improve understanding of an application. Reverse engineering can also be used to identify vulnerabilities, for security analysis or malicious purposes. [Decompilers](#decompiler) and [disassemblers](#disassembler) may be used to aid reverse engineering, while [obfuscation](#obfuscation) can make the process more difficult.

## Scope
Scope refers to **the part of a program in which a given name binding (an association of an identifier to an entity, e.g. a [variable](#variable)) is valid**, i.e. where the name can be used to refer to the entity. Outside of this scope, the same name may not be defined (*unbound*) or may refer to a different entity (i.e. have a different binding, e.g. [variable shadowing](#variable-shadowing)). This concept is important for [name resolution](#name-resolution). The scope of a name binding is also known as the *visibility* of an entity.

Scope can also refer more broadly to the set of all name bindings that are valid within a part of a program or at a given point in a program, also (more correctly) known as *context* or *environment*. The "part of a program" typically refers to a portion of [source code](#source-code) (*lexical scope* or *static scope*), but this can also refer to a portion of run time during [execution](#execution) (*dynamic scope*).

Several different levels of program scope can exist, including *global scope* (valid everywhere), *local scope* (valid relative to the current code, e.g. a [subroutine](#subroutine)), *module scope*, *block scope*, *function scope*, and *[expression](#expression) scope*. See also: [global variable](#global-variable) and [local variable](#local-variable).

## Side effect
A side effect is **a modification of non-local [state](#state) by a [subroutine](#subroutine), [statement](#statement), or other operation**. In other words, some effect can be observed beyond the return of a [value](#value). Despite the name, a side effect is not necessarily unintentional. For example, changing the [value](#value) of a non-local [variable](#variable) or writing data to a file are both side effects. See also: [functional programming](#functional-programming) and [pure function](#pure-function).

## Source code
Source code refers to **human-readable code that is typically written in a [high-level language](#high-level-language)**. It is a somewhat generic term to describe the input for [translation](#translator) (via [compilation](#compiler) or [interpretation](#interpreter)) into a [low-level language](#low-level-language), i.e. [object code](#object-code) (the resulting product).

## Space complexity
Space complexity is **a description of the amount of [memory](#memory) space required to [execute](#execution) an [algorithm](#algorithm) or computer program, in relation to its input size**. This is important for assessing an algorithm's memory efficiency and usefulness. Space complexity is commonly represented by [big O notation](#big-o-notation). See also: [time complexity](#time-complexity).

## State
State refers to **the collection of information in [memory](#memory) at any given point during the [execution](#execution) of a program**. This information can include preceding events and user interactions, and helps to define the program's current condition. State typically refers more specifically to the data stored within [variables](#variable) at a given point. A system that is designed to have state can be described as *stateful*. A *state space* refers to the set of all possible configurations of a system.

[Programming paradigms](#programming-paradigm) can be categorised based on whether they directly modify program state (*imperative*) or not (*declarative*).

## Statement
A statement is **a unit of [syntax](#syntax) that can be [executed](#execution) to carry out a specific action**. Statements which cannot contain other statements are *simple* (e.g. assignments, [subroutine](#subroutine) calls, and return statements), while those which can are *compound* (e.g. conditional statements, loops, and exception handling). In contrast to statements, [expressions](#expression) are units of syntax that are *evaluated*.

## Subroutine
A subroutine is **a sequence of program instructions that performs a specific task, packaged as a unit**. This unit can then be used in programs wherever that particular task should be performed. *Subroutine* or *callable unit* can be used to refer to a function (returns at least one value), procedure (does not return a value), [method](#method) (associated with an object), or subprogram (a subroutine used as part of a larger program). Different languages may use different terms to describe these.

The use of subroutines is an important part of [decomposition](#decomposition); facilitates code reuse (i.e. to avoid repetition); allows for the use of [interfaces](#interface) and [information hiding](#information-hiding); makes programs easier to test, debug, and refactor; and improves readability.

## Synchronisation
Synchronisation refers to **a set of techniques to ensure that two or more [concurrent](#concurrency) [processes](#process) or [threads](#thread) do not simultaneously [execute](#execution) a [critical section](#critical-section)** (a portion of code where concurrent access must be avoided). Synchronisation techniques include *locks* and *semaphores*, and enforce *mutual exclusion*. Without effective synchronisation, [race conditions](#race-condition) and other concurrency issues may occur.

## Syntax
Syntax refers to **the set of rules that defines the combinations of symbols that are correctly structured [statements](#statement) or [expressions](#expression) in a given programming language**. The syntax required to achieve a given operation (e.g. printing "Hello, World!") typically differs between programming languages, even if the underlying approach/design is the same.

## Test-driven development
Test-driven development (TDD) is **a development process that involves requirements being converted to test cases *before* the associated functionality is fully developed**. During development, all test cases are run frequently. TDD can result in simpler and higher-quality code that better meets the original requirements.

More specifically, test-driven development involves the following steps: add a test based on requirements and use cases; run all tests and confirm that the new test fails; write code that passes the new test; confirm that all tests pass; refactor as needed for readability and maintainability while ensuring that tests continue to pass. 

## Thread
A thread is **the smallest sequence of program instructions that can be managed independently by a scheduler** (a process that manages resources and multitasking). Also known as a *thread of [execution](#execution)*. Depending on the operating system, multiple threads within the same [process](#process) can be executed [concurrently](#concurrency) and share resources such as [memory](#memory) (i.e. *multithreading*).

*Thread safety* refers to the vulnerability of code to [race conditions](#race-condition) as a result of multithreading. Thread-safe code manipulates shared resources (e.g [data structures](#data-structure)) in a way that ensures that all threads behave properly without unintended interaction, i.e. multiple threads executing the same code does not cause unexpected or unwanted consequences.

## Time complexity
Time complexity is **a description of how long it takes to run an [algorithm](#algorithm), in relation to its input size**. This is important for assessing an algorithm's time efficiency and usefulness. Time complexity usually represents the worst case scenario, i.e. the maximum running time for inputs of a given size (`n`), as represented by [big O notation](#big-o-notation). For example, if an item was being searched for linearly down a list, the worst case would be if the item was the final list item (or not present).

Time complexity can be estimated by counting the number of elementary operations performed by the algorithm (assuming that each operation takes a fixed amount of time), in relation to `n`. See also: [space complexity](#space-complexity).

## Translator
A translator is **a program that translates code written in one programming language (the [source code](#source-code)) into another (the [object code](#object-code))**. There are three common types of translator: [compilers](#compiler) ([high-level](#high-level-language) to [low-level](#low-level-language), translated all at once); [interpreters](#interpreter) (high-level to low-level, translated one [statement](#statement) at a time); and [assemblers](#assembler) ([assembly language](#assembly-language) to [machine code](#machine-code)).

## Tree
A tree is **a non-linear [data structure](#data-structure) comprised of linked *nodes* (connected by directed *edges*) that represent a hierarchical tree structure.** The topmost (beginning) node is the *root node*. *Parent nodes* link (contain references) to at least one *child node*. Every node except the root has a single parent. Every node has zero or more children (*leaf nodes*/*external nodes* and *internal nodes* respectively). A node's *degree* is its number of children; its *depth* is the count of edges to the root; and its *height* is the longest count of edges to a leaf.

Trees can be used to model real-world hierarchical systems, e.g. file systems. *Binary search trees* are ordered/sorted to facilitate efficient *binary search*. See also: [graph](#graph).

## Type signature
A type signature is a **comment or [syntax](#syntax) that defines the input(s) and output(s) of a [subroutine](#subroutine)**. More specifically, this includes the number, order, and [type](#data-type)(s) of [arguments](#argument) that are consumed and returned. A type signature can also include details of exceptions that may be raised and the availability (e.g. `public`) of the subroutine. Also known as a *type annotation*, *function signature*, or *method signature*. See also: [parameter](#parameter).

## Type system
A type system refers to **the set of rules in a language that assign [type](#data-type) to the entities of a program**, to formalise and enforce the categorisation of program elements. The main purpose of a type system is to reduce bugs, by associating a type with computed [values](#value)/[variables](#variable) and checking that no *type errors* can occur. Type errors are defined by the type system, but generally involve a given type being operated on in an invalid way (e.g. using division on a string). Type errors are often the result of misused [interfaces](#interface).

A *statically typed* language (e.g Java) uses *static type checking* of a program's [source code](#source-code), typically during [compile time](#compiler), to identify type errors *before* [run time](#execution). In contrast, a *dynamically typed* language (e.g. Python) uses *dynamic type checking* of a program *during* run time. Statically typed languages may also utilise some dynamic type checking. In general, static typing is considered safer but stricter, while dynamic typing is considered more flexible but also more vulnerable to unexpected errors.

Type systems can also be classed as *strongly typed* or *weakly typed*, corresponding to the strictness of typing rules, though this is often subjective. For example, this can relate to whether variables need to be assigned a type or to the ability to add a numeric string to an integer (e.g. `2 + '2'`). *Duck typing* uses an object's [methods](#method) and/or [attributes](#member-variable) rather than its type to determine the validity of an operation (*"If it walks like a duck..."*). *Type safety* is the extent to which a language discourages or prevents type errors.

## Unified Modelling Language
Unified Modelling Language (UML) is a **general-purpose modelling language that is used to create standardised visualisations relating to program design**. UML diagrams represent either structural (static) or behavioural (dynamic) information.

A *class diagram* is a common type of structural diagram, and describes a system's classes, their attributes, their methods, and the relationships between them. A *sequence diagram* is an example of a behavioural diagram, and describes how objects interact over time.

## Value
A value is **the representation of an entity that can be manipulated by a program**. Values have an associated [data type](#data-type) (e.g. integer or string), and can be stored in [variables](#variable) and as [constants](#constant).

## Variable
A variable is **a storage location (identified by a [memory address](#memory)) with an associated name, which contains a [value](#value) that can be modified during program [execution](#execution)**. In other words, a variable is a container for changeable data, which can be referenced by the variable name within a program. In contrast, a [constant](#constant) cannot be modified. 

Associating the storage location with a value is called *assignment*, or [initialisation](#initialisation) if it is the first assignment. A variable's *extent* or *lifetime* describes when in a program's execution the variable has a (meaningful) value, or can refer to the extent of a specific value. The extent of a *static variable* is the entire program execution, in contrast to an *automatic variable*.

A *scalar variable* is a variable that holds a single value, in contrast to a more complex object or [data structure](#data-structure) (e.g. an array). A variable can be categorised based on [scope](#scope) as a *[global variable](#global-variable)* or a *[local variable](#local-variable)*. A variable that is associated with an object is called a *[member variable](#member-variable)*. A variable used in a function that is neither a local variable nor passed by a [parameter](#parameter) of the function (i.e. a variable defined in an enclosing scope) is called a *free variable*.

## Variable shadowing
Variable shadowing refers to a situation where **a [variable](#variable) has the same name as another variable within the wider [scope](#scope)**, i.e. the outer variable is *shadowed by* the inner variable or the inner variable *shadows* the outer variable. Modification of the inner variable will not modify the outer variable. The ways in which shadowing can occur (e.g. within code blocks) differs by language.

Variable shadowing can be confusing and can increase the likelihood of introducing a bug (e.g. referencing the wrong variable or failing to rename all instances of the local variable), especially in large or complex functions. As such, it is often discouraged.

## Virtual machine
A virtual machine (VM) is **a program that emulates a computer system such as an operating system (*system virtual machine*) or a platform-independent environment (*process virtual machine*)**. 

This allows a single computer hardware system to be more flexible, i.e. by (indirectly) supporting multiple different systems and associated programs/functionality. Due to their isolation from the real system hardware, VMs can also be used to safely test an early version of a program (that could contain severe bugs) or analyse potentially malicious software.
