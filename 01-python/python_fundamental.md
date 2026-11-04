# Python Fundamentals for Data Science & Algorithmic Thinking
**Course Syllabus & Execution Roadmap**

This curriculum builds the core programming foundation required for scientific computing, statistical analysis, interactive visualization, and algorithmic problem-solving.

---

## Module 1: Environment, Syntax, & Core Variables
*   **1.1 Development Workflow**
    *   Python execution model (interpreted vs. compiled concepts, CPython)
    *   Virtual environments (`venv`, `conda`) and package managers (`pip`)
    *   Interactive development with Jupyter Notebooks, IPyKernel, and VS Code
    *   Script execution from CLI (`python main.py`)
*   **1.2 Variables & Dynamic Typing**
    *   Naming conventions (PEP 8 standard)
    *   Dynamic typing system, variable binding, and object references
    *   Garbage collection basics and `id()` introspection
*   **1.3 Scalar Data Types & Operations**
    *   Integers (`int`) and floating-point arithmetic (`float`)
    *   Floating-point representation errors and IEEE 754 standard
    *   Booleans (`bool`) and truthy/falsy evaluation rules
    *   Type casting and explicit conversions
*   **1.4 Basic I/O & Formatting**
    *   Formatted string literals (f-strings) and formatting specifications
    *   Standard input handling (`input()`) and casting

---

## Module 2: Data Structures & Memory Concepts
*   **2.1 Sequences: Lists & Tuples**
    *   Indexed access, negative indexing, and extended slicing `[start:stop:step]`
    *   Mutability vs. immutability
    *   List operations, appending, extending, popping, and sorting ($O(n \log n)$ Timsort)
    *   Tuple packing/unpacking and immutability advantages
*   **2.2 Key-Value Mapping: Dictionaries**
    *   Hash map mechanics: keys, values, and key immutability requirements
    *   Dictionary lookup, insertion, deletion performance ($O(1)$ average time complexity)
    *   Dictionary methods (`.keys()`, `.values()`, `.items()`, `.get()`, `.setdefault()`)
*   **2.3 Unordered Sets**
    *   Set theory operations: union (`|`), intersection (`&`), difference (`-`), symmetric difference (`^`)
    *   Deduplication techniques and set performance ($O(1)$ lookup)
*   **2.4 Deep vs. Shallow Copies**
    *   Reference copying (`a = b`)
    *   Shallow copies (`copy.copy()`) vs. deep recursive copies (`copy.deepcopy()`)

---

## Module 3: Control Flow & Algorithmic Foundations
*   **3.1 Conditional Logic**
    *   `if`, `elif`, `else` branching
    *   Short-circuiting in boolean evaluation (`and`, `or`)
    *   Ternary conditional expressions (`x if condition else y`)
    *   Structural Pattern Matching (`match-case` statements in Python 3.10+)
*   **3.2 Iteration Mechanics**
    *   `while` loops and break/continue control
    *   `for` loops over iterables
    *   Loop utilities: `range()`, `enumerate()`, `zip()`, and `reversed()`
    *   Loop `else` clause pattern
*   **3.3 Comprehensions & Expressions**
    *   List comprehensions with filtering syntax
    *   Dictionary and set comprehensions
    *   Generator expressions (memory-efficient iteration)

---

## Module 4: Functional Programming Principles
*   **4.1 Function Design & Scope**
    *   Function definition (`def`), parameters, and `return` statements
    *   Positional arguments, keyword arguments, default parameter values
    *   Variadic parameters: `*args` and `**kwargs`
    *   LEGB Scope Rule (Local, Enclosing, Global, Built-in)
    *   `global` and `nonlocal` declarations
*   **4.2 First-Class Functions & Lambda Expressions**
    *   Passing functions as arguments and returning functions
    *   Anonymous functions (`lambda`) for concise inline logic
    *   Functional helpers: `map()`, `filter()`, `reduce()` (`functools`)
*   **4.3 Higher-Order Functions & Decorators**
    *   Closures and state preservation
    *   Building custom decorators (`@decorator_name`)
    *   Preserving metadata with `functools.wraps`
    *   Decorators with arguments and logging/timing execution wrappers
*   **4.4 Generators & Iterators**
    *   The Iterator Protocol (`__iter__`, `__next__`)
    *   Generator functions using `yield`
    *   Memory optimization for processing large data pipelines

---

## Module 5: Object-Oriented Programming (OOP)
*   **5.1 Classes, Instances, & Attributes**
    *   Class definitions (`class`), instantiation, and the `self` parameter
    *   Instance attributes vs. class attributes
    *   Constructor methods (`__init__`)
*   **5.2 Encapsulation & Properties**
    *   Access modifiers conventions (public, `_protected`, `__private` name mangling)
    *   Managed attributes using `@property`, `@setter`, and `@deleter`
*   **5.3 Inheritance & Polymorphism**
    *   Single and multiple inheritance patterns
    *   Method overriding and calling `super()`
    *   Method Resolution Order (MRO) and C3 Linearization
    *   Abstract Base Classes (`abc.ABC`, `@abstractmethod`)
*   **5.4 Magic Methods (Dunder Methods)**
    *   String representation: `__str__` vs. `__repr__`
    *   Operator overloading (`__add__`, `__eq__`, `__lt__`, etc.)
    *   Container emulate methods (`__len__`, `__getitem__`, `__setitem__`)
    *   Context management (`__enter__`, `__exit__`)

---

## Module 6: Modules, Packages, & File I/O
*   **6.1 System Modules & Namespace Imports**
    *   `import` mechanisms, `sys.path`, and module search order
    *   Absolute vs. relative imports
    *   Understanding `__name__ == "__main__"` execution protection
*   **6.2 Custom Packages**
    *   Directory structures, `__init__.py` files, and package exposure
*   **6.3 File System & Data I/O**
    *   Reading/writing plain text files using `with open(...)` context managers
    *   Path manipulation using `pathlib.Path` (cross-platform path resolution)
    *   Structured data serialization: `json`, `csv`, and binary `pickle`
*   **6.4 Exception & Error Handling**
    *   The Python exception hierarchy (`Exception`, `BaseException`)
    *   Handling runtime errors (`try`, `except`, `else`, `finally`)
    *   Raising exceptions (`raise ExceptionType(...)`)
    *   Defining custom application-specific exceptions

---

## Module 7: Python for Algorithmic Thinking & Complexity
*   **7.1 Built-in Time & Space Complexity**
    *   Big-O analysis of built-in operations (lists vs. sets vs. dicts)
    *   Memory efficiency overhead of standard Python objects
*   **7.2 Specialized Data Structures (`collections` Module)**
    *   `deque`: Double-ended queues ($O(1)$ appends and pops)
    *   `Counter`: Hash-based frequency counting
    *   `defaultdict`: Dictionaries with default value factories
    *   `namedtuple` & `dataclasses`: Clean record-style data models
*   **7.3 Priority Queues & Sorting (`heapq` & `bisect`)**
    *   Binary heaps using `heapq` (Min-heap implementation)
    *   Binary search on sorted lists using `bisect`
*   **7.4 Type Hinting & Static Analysis**
    *   Type annotations (`typing` module: `List`, `Dict`, `Tuple`, `Optional`, `Union`)
    *   Static type checking workflow using `mypy`

---

## Module 8: Code Quality, Testing, & Production Practices
*   **8.1 Code Style & Formatting**
    *   PEP 8 standards adherence
    *   Automated formatting with `black` and linting with `flake8` or `ruff`
*   **8.2 Automated Testing**
    *   Assertions (`assert`) and test design
    *   Unit testing framework with `pytest`
    *   Test fixtures, parametrization, and basic test coverage analysis
*   **8.3 Debugging & Profiling**
    *   Interactive debugging with `pdb` and `breakpoint()`
    *   Performance profiling using `cProfile` and memory profiling basics
