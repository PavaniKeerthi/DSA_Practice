# Machine Code, Compiler, and Interpreter

## What is Machine Code?

Computers understand only binary instructions:

```text
0s and 1s
```

This low-level binary language is called:

```text
Machine Code
```

Programming languages like:

* C++
* Java
* Python

cannot directly run on the CPU.

They must first be converted into machine code.

---

## What is a Compiler?

A compiler is a software program that:

```text
Converts the entire source code into machine code before execution.
```

### Flow

```text
Source Code → Compiler → Machine Code → Execute
```

### Characteristics

* Converts whole program at once
* Generates executable file
* Faster execution
* Shows multiple errors together
* Program runs only after successful compilation

### Example Languages

* C
* C++

---

## What is an Interpreter?

An interpreter is a software program that:

```text
Reads, translates, and executes code line by line.
```

### Flow

```text
Source Code → Interpreter → Execute Line by Line
```

### Characteristics

* Executes line by line
* No separate executable file
* Slower execution
* Stops at first error
* Easier testing and debugging

### Example Languages

* Python
* JavaScript

---

## Compiler vs Interpreter

| Feature         | Compiler                   | Interpreter                     |
| --------------- | -------------------------- | ------------------------------- |
| Translation     | Whole program at once      | Line by line                    |
| Speed           | Faster                     | Slower                          |
| Error Reporting | Shows many errors together | Stops at first error            |
| Output          | Executable machine code    | No separate executable          |
| Execution       | After compilation          | During translation              |
| Debugging       | Better for syntax checking | Better for step-by-step tracing |
| Examples        | C, C++                     | Python, JavaScript              |

---

## Key Takeaways

```text
Compiler → translates entire program before execution
Interpreter → translates and executes line by line
```
