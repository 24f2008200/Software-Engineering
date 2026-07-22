Yes. These transcripts are well suited for building **exam-focused notes**, because they contain the instructor's definitions, examples, and emphasis. From the five lectures you uploaded, here is a consolidated study guide.

---

# Week 7 – Software Development Practices

---

# 1. Version Control Systems (VCS)

## Definition

A **Version Control System (VCS)** is a system that tracks and manages changes to source code (or documents) over time while maintaining different versions of the project. It is part of **Software Configuration Management (SCM)**. 

### Why do we need VCS?

Without version control:

* Multiple developers overwrite each other's work.
* Difficult to rollback to a working version.
* Hard to maintain many releases.
* Difficult to know **who changed what and when**.

The lecture illustrates these problems using team development and maintaining multiple versions for different customers.  

### Important Features

* Track changes
* Maintain version history
* Rollback to earlier versions
* Branching
* Merging
* Commit history
* Collaboration

---

# Git Concepts

Know these definitions.

### Repository

Database containing project history.

### Commit

Snapshot of current project.

### Branch

Independent line of development.

### Merge

Combines two branches.

### Clone

Copy repository to local machine.

### Pull

Download latest changes.

### Push

Upload local commits.

### Conflict

Occurs when two developers modify the same code.

---

# 2. Issue Tracking

## Definition

An **Issue** is a bug, feature request, or problem reported by a developer, tester, or user.

An **Issue Tracking System** stores, manages, prioritizes, and tracks issues until they are resolved. 

---

## Importance

Issue tracking helps

* Deliver higher-quality software
* Prioritize important bugs
* Reduce development cost
* Preserve issue history
* Improve testing
* Improve customer satisfaction
* Improve team communication



---

# Typical Issue Lifecycle

New

↓

Assigned

↓

In Progress

↓

Fixed

↓

Tested

↓

Closed

---

# GitHub Issues

The lecture demonstrates using GitHub for

* Creating issues
* Assigning issues
* Adding labels
* Commenting
* Closing issues

These help teams coordinate software development.

---

# 3. Code Review

## Definition

Code Review is the process of examining another developer's code before merging it into the project.

Purpose

* Detect bugs
* Improve readability
* Enforce coding standards
* Share knowledge
* Improve maintainability

---

## Pull Request

A Pull Request (PR) is a request to merge changes into the main branch after review.

Typical workflow

Developer

↓

Commit

↓

Push

↓

Pull Request

↓

Review

↓

Approve

↓

Merge

---

# Benefits of Code Review

* Better quality
* Fewer bugs
* Better design
* Knowledge sharing
* Consistent coding style

---

# 4. Debugging

## Important Definitions

The lecture clearly distinguishes four related terms:

### Error

Difference between **intended behaviour** and **actual behaviour**. 

---

### Failure

Observable manifestation of an error.

Examples

* Wrong output
* Exception
* Crash

---

### Fault

Actual line (or location) in the code responsible for the failure. 

---

### Debugging

Process of identifying the cause of a failure and correcting the code. 

---

# Debugging Process

Remember this sequence.

1. Reproduce problem
2. Find defect
3. Investigate fix
4. Implement fix
5. Test fix



---

# Debugging Techniques

The lecture discusses four common techniques.

### Logging

Insert print/log statements.

---

### Dump and Diff

Compare outputs between correct and incorrect executions.

---

### Debugger

Use breakpoints and step through execution.

---

### Profiling

Measure execution frequency and execution time.

Useful for performance-related bugs.



---

# Debugging Strategy

The instructor demonstrates **input manipulation**:

* Try different inputs
* Observe outputs
* Narrow down where the fault lies
* Fix the logic

This systematic approach is illustrated using a faulty prime-number program.  

---

# 5. Software Metrics

## Definition

Software Metrics are **quantitative measures** used to evaluate code quality and complexity. 

---

## Why Measure Code?

The lecture emphasizes that clean code is

* Easier for teammates to understand
* Easier to test
* Easier to maintain
* Easier to extend



---

# Examples of Metrics

* Lines of Code (LOC)
* Number of comments
* Cyclomatic Complexity

Radon (Python tool) is presented as a tool for computing such metrics. 

---

# Cyclomatic Complexity (CC)

## Definition

Cyclomatic Complexity =

**Number of decision points + 1**

Example

```
if (...)
```

Decision points = 1

Cyclomatic Complexity = 2



---

## Interpretation

Higher CC implies

* More complex code
* Harder testing
* Lower readability
* Higher maintenance effort

---

# 6. Writing Clean Code

The lecture notes that not all quality aspects can be measured numerically. Some poor coding practices are identified as **code smells**. 

---

# Code Smell

## Definition

A **Code Smell** is a characteristic in the code that suggests poor design or maintainability, even if the program works correctly. 

---

# Common Code Smells

### Redundant Comments

Avoid comments that merely restate the code.

Write comments explaining **why**, not **what**.

---

### Commented-Out Code

Delete unused code.

Version Control already preserves history.



---

### Long Functions

Functions should perform only one task.

---

### Too Many Parameters

Ideally

* 0
* 1
* 2
* at most 3 parameters

More parameters usually indicate poor design.

---

### Flag Arguments

Avoid Boolean flags that change function behavior.

Instead

Split into multiple functions.

---

### Dead Functions

Remove functions never called.



---

# DRY Principle

## DRY

**Don't Repeat Yourself**

Avoid duplicated code.

Instead

Extract repeated logic into reusable functions.



---

# Comparison Table

| Concept          | Purpose                             |
| ---------------- | ----------------------------------- |
| Version Control  | Manage source code history          |
| Git              | Popular Version Control tool        |
| Issue Tracking   | Manage bugs and feature requests    |
| Code Review      | Improve code quality before merging |
| Debugging        | Find and fix defects                |
| Software Metrics | Quantitatively measure code quality |
| Code Smell       | Indicates poor design               |
| DRY              | Avoid duplicated code               |

---

# Definitions to Memorize

* **Version Control System:** Tracks and manages changes to source code while maintaining versions.
* **Issue Tracking System:** Tool for recording and managing software issues.
* **Error:** Difference between intended and actual behavior.
* **Failure:** Observable manifestation of an error.
* **Fault:** Code location causing a failure.
* **Debugging:** Finding and fixing the cause of failures.
* **Software Metrics:** Quantitative measures of software quality.
* **Cyclomatic Complexity:** Number of decision points plus one.
* **Code Smell:** Characteristic suggesting poor code quality.
* **DRY:** Don't Repeat Yourself.

---

# High-Probability Exam Questions

1. What problems are solved by Version Control Systems?
2. Explain the advantages of Git in team software development.
3. What is an Issue Tracking System? Why is it important?
4. Explain the stages of debugging.
5. Differentiate **Error**, **Failure**, **Fault**, and **Debugging**.
6. Explain logging, profiling, and debugger-based debugging.
7. Define Software Metrics with examples.
8. What is Cyclomatic Complexity? How is it calculated?
9. What are Code Smells? Give examples.
10. Explain the DRY principle.
11. Why is clean code easier to maintain and extend?
12. Explain the purpose of Code Reviews and Pull Requests.

These notes capture the concepts and definitions that the instructors explicitly emphasize and are the most likely to appear in quizzes or theory exams.
