Below are concise, exam-oriented revision notes for **Week 9 – Software Testing**, focusing on **definitions, key concepts, comparisons, and likely exam questions** rather than reproducing the lecture. 

---

# Week 9 Revision Notes – Software Testing

## 1. What is Software Testing?

### Definition

**Software Testing** is the process of executing software with the objective of finding defects and verifying that it behaves according to the specified requirements.

### Why is Testing Important?

* Detects defects before software is released.
* Improves reliability and quality.
* Prevents failures that may cause serious consequences.
* Reduces maintenance cost by finding bugs early.

Examples:

* Airport system failures
* Spacecraft failures



---

# 2. Basic Activities in Testing

A testing cycle consists of:

1. Provide inputs
2. Execute the program
3. Check outputs
4. Compare with expected outputs
5. Locate the error
6. Identify the cause
7. Fix the error
8. Test again

Testing is therefore an **iterative process**.



---

# 3. Test Case

### Definition

A **Test Case** is a triplet:

**[I, S, R]**

where

* **I** = Input
* **S** = State of the program when input is applied
* **R** = Expected Result

Example

```
Function:
min(x,y)

Input:
(5,3)

State:
Program started

Expected Result:
3
```

---

# 4. Test Suite

### Definition

A **Test Suite** is a collection of test cases designed to test a software system.

One program → Many test cases → One Test Suite.



---

# 5. Why Design Test Cases?

Random testing **does not guarantee** finding most bugs.

Since the input domain is huge, we need a **small but effective** set of test cases that can detect different categories of defects.

Goal:

* Maximum fault detection
* Minimum number of test cases



---

# 6. Example: Designing Test Cases

Suppose

```
if (x < y)
    min = x
else
    min = y
```

Instead of testing hundreds of values, identify important scenarios.

Test cases:

* First value is smaller
* Second value is smaller
* Both values equal

These represent different classes of behaviour.



---

# 7. Black-box Testing

### Definition

Testing based only on the **external behaviour** of the program.

The tester:

* does not see the source code
* checks only inputs and outputs

Focus:

> "Does the program produce the correct result?"

Example

Testing a calculator by giving

```
2 + 3
```

Expected output

```
5
```

without caring how addition is implemented.



---

# 8. White-box Testing

### Definition

Testing based on the **internal structure of the code**.

The tester examines

* logic
* branches
* loops
* conditions
* execution paths

Goal

Ensure every important path has been executed.

Important term:

### Test Coverage

Percentage of program paths executed by test cases.

Higher coverage generally increases confidence.



---

# Black-box vs White-box Testing

| Black-box           | White-box             |
| ------------------- | --------------------- |
| Tests functionality | Tests implementation  |
| Code not visible    | Code visible          |
| Input-output based  | Path/logic based      |
| User perspective    | Developer perspective |

---

# 9. Levels of Testing

Software is tested in stages.

---

## Unit Testing

### Definition

Testing individual functions or modules independently.

Who performs it?

Usually the **developer**.

When?

During coding.

Advantages

* Finds bugs early
* Easier debugging
* Independent of other modules



---

## Integration Testing

### Definition

Combining modules gradually and testing their interaction.

Purpose

Find interface problems between modules.

Example

```
Login Module
+

Database Module
```

may work individually but fail together.

---

## System Testing

### Definition

Testing the **entire integrated application**.

Checks

* Functional requirements
* Performance
* Security
* Reliability

---

### Alpha Testing

Performed by

* Internal testing team

Purpose

Find defects before release.

---

### Beta Testing

Performed by

* Selected customers

Purpose

Find real-world problems before official release.

---

## Acceptance Testing

### Definition

Performed by the customer.

Purpose

Determine whether the software satisfies business requirements and should be accepted.



---

# 10. Why Unit Testing?

Reasons

* Other modules may not yet be available.
* Easier to isolate bugs.
* Cheaper to fix defects early.
* Makes debugging simpler.

Without unit testing,

if the whole application fails,

finding the faulty module becomes difficult.



---

# 11. Testing Environment

To test one module, we often need supporting components.

### Stub

A **dummy module** that replaces a called function.

Characteristics

* Same interface
* Simplified behaviour

Used when the called module is not yet developed.

---

### Driver

A module that calls the unit under test.

Responsibilities

* Provides inputs
* Creates required data
* Starts execution

Memory Trick

**Driver calls**

**Stub gets called**



---

# Important Definitions

You should be able to write these in 2–3 lines:

* Software Testing
* Test Case
* Test Suite
* Black-box Testing
* White-box Testing
* Test Coverage
* Unit Testing
* Integration Testing
* System Testing
* Alpha Testing
* Beta Testing
* Acceptance Testing
* Stub
* Driver

---

# High-Probability Comparisons

### Black-box vs White-box Testing

| Black-box          | White-box               |
| ------------------ | ----------------------- |
| External behaviour | Internal code           |
| No code knowledge  | Code knowledge required |
| Functional testing | Structural testing      |

---

### Alpha vs Beta Testing

| Alpha                  | Beta                   |
| ---------------------- | ---------------------- |
| Internal team          | Customers              |
| Before beta            | Before final release   |
| Controlled environment | Real-world environment |

---

### Unit vs Integration Testing

| Unit              | Integration             |
| ----------------- | ----------------------- |
| Individual module | Multiple modules        |
| Easier debugging  | Finds interface errors  |
| Done first        | Done after unit testing |

---

### Stub vs Driver

| Stub                    | Driver                   |
| ----------------------- | ------------------------ |
| Simulates called module | Simulates calling module |
| Called by unit          | Calls the unit           |
| Bottom component        | Top component            |

---

# Exam Mnemonics

### Testing Levels

**UISA**

* **U** – Unit
* **I** – Integration
* **S** – System
* **A** – Acceptance

(Alpha and Beta are part of **System Testing**.)

---

### Test Case

**ISR**

* **I** – Input
* **S** – State
* **R** – Result

---

# Most Important Topics (Exam Priority)

**★★★★★**

* Test Case and Test Suite
* Black-box vs White-box Testing
* Levels of Testing (Unit, Integration, System, Acceptance)
* Stub and Driver

**★★★★☆**

* Test Coverage
* Designing Effective Test Cases
* Alpha vs Beta Testing

**★★★☆☆**

* Importance of Testing
* Testing Activities

These notes capture the core definitions, comparisons, and concepts emphasized in the Week 9 lecture and are well suited for last-minute revision.
