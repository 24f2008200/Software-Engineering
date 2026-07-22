Yes. Based on these Week 1 lecture transcripts, here is an **exam-oriented summary** focusing on **definitions, key concepts, comparisons, and likely exam questions**.

---

# Software Engineering - Week 1 Exam Notes

## 1. What is Software Engineering?

### Definition

Software Engineering is the disciplined approach to developing software using **well-defined processes, models, tools and best practices**, instead of relying only on programming skill. It evolved from documenting the practices of good programmers into systematic development processes. 

### Three pillars of the course

* Software processes
* Software development tools
* Clean and maintainable code

These three together enable building reliable software systems. 

---

# 2. Software Development Life Cycle (SDLC)

### Definition

The SDLC is the sequence of stages through which software evolves from a customer's initial request into a completed software product.

### Phases

1. Requirement Specification
2. Software Design
3. Development (Coding)
4. Testing
5. Maintenance

Remember this order.

---

# 3. Requirement Specification

### Definition

Requirements are the **explicit goals and functionalities** that the software must provide.

They answer:

* What problem are we solving?
* Who will use the software?
* What should the software do?

Requirements are gathered **before** design or coding begins. 

---

### Client

A client is **any entity that uses the software or one of its components.**

Clients may be:

* External users
* Internal users
* Another software component

Example:

An e-commerce website is a client of a payment gateway.

---

### Important exam point

Requirements must satisfy client needs throughout development.

---

# 4. Software Design

### Definition

Software Design is the **big-picture blueprint** of the software system.

It specifies

* structure
* organization
* interaction among components

before coding starts.

---

### Why design before coding?

Without design,

* developers make incompatible decisions
* integration becomes difficult
* maintenance becomes expensive
* future changes become harder

The design phase provides structure to the whole system before implementation begins. 

---

# 5. Development

### Definition

Development is the implementation phase where developers write code according to

* requirements
* design

Large software is developed collaboratively by multiple programmers.

---

### Interface

One of the most important definitions.

**Interface**

An interface specifies

* what services a component provides
* accepted inputs
* produced outputs

without revealing how it is implemented.

Implementation may change while the interface remains unchanged. 

---

# 6. Testing

### Definition

Testing is the activity of verifying that software behaves according to its requirements.

Purpose:

* find bugs
* detect defects
* improve reliability

Testing is essential because undiscovered bugs may cause huge financial losses or catastrophic failures. 

---

### Types of Testing

Know these definitions.

### Unit Testing

Tests one isolated unit such as

* one function
* one class

---

### Integration Testing

Tests whether multiple modules work correctly together.

---

# 7. Maintenance

### Definition

Maintenance is the phase after deployment in which software is

* corrected
* updated
* improved
* adapted to new requirements

Maintenance continues throughout the software's lifetime.

---

# 8. Software Components

### Definition

A component is an independent part of a software system that performs a specific function.

Components

* reduce complexity
* enable parallel development
* hide implementation details
* communicate through interfaces

Examples in Amazon

* Inventory Management
* Payment Gateway
* Recommendation System
* Logistics
* Amazon Pay



---

# 9. Waterfall Model

### Definition

A sequential software development model in which each phase is completed before the next begins.

Sequence:

Requirements

↓

Design

↓

Development

↓

Testing

↓

Maintenance

---

### Why called Plan and Document?

Because

* everything is planned first
* every phase is documented
* progress is measured against the plan



---

### Advantages

* well organized
* disciplined
* documentation available
* suitable for stable requirements

---

### Drawbacks

Very important exam question.

Problems include

* changes become expensive
* customer may change requirements
* customer may not know exact needs initially
* feedback comes too late
* delays increase cost

---

# 10. Agile

### Definition

Agile is an iterative software development approach where software is delivered in small working increments with continuous customer feedback.

---

## Agile Manifesto

Know these four values exactly.

1. Individuals and interactions over processes and tools

2. Working software over comprehensive documentation

3. Customer collaboration over contract negotiation

4. Responding to change over following a plan



---

### Agile characteristics

* iterative
* incremental
* rapid feedback
* customer involvement
* embraces change
* continuous improvement

---

### Agile approaches

Know these names.

* Scrum
* Extreme Programming (XP)

XP includes

* Test Driven Development
* Pair Programming
* Behaviour Driven Development

---

# 11. Waterfall vs Agile

| Waterfall            | Agile                         |
| -------------------- | ----------------------------- |
| Sequential           | Iterative                     |
| Heavy documentation  | Lightweight documentation     |
| Fixed plan           | Flexible plan                 |
| Feedback at end      | Continuous feedback           |
| Changes expensive    | Changes expected              |
| Single final release | Multiple incremental releases |

---

# 12. Build-and-Fix Model

Early software development followed the Build-and-Fix approach.

Characteristics

* start coding immediately
* informal understanding of requirements
* fix problems later

Problems

* poor planning
* poor maintainability
* difficult scaling

It eventually evolved into Software Engineering processes. 

---

# 13. Key Definitions (Memorize)

**Software Engineering**

Disciplined development of software using processes, tools and best practices.

**Software Lifecycle**

The stages through which software evolves from requirements to maintenance.

**Requirement**

A goal or functionality that the software must satisfy.

**Client**

Any user or component that uses software services.

**Design**

The blueprint describing software structure before coding.

**Component**

An independent module performing a specific function.

**Interface**

Specification of inputs, outputs and services without implementation details.

**Testing**

Verification that software satisfies requirements.

**Maintenance**

Updating and correcting software after release.

**Waterfall**

Sequential software development process.

**Agile**

Iterative software development with continuous customer feedback.

---

# Likely Exam Questions

1. Define Software Engineering.

2. Explain the Software Development Life Cycle.

3. What is Requirement Specification?

4. Differentiate Design and Development.

5. Why is Software Design necessary?

6. Explain the importance of Testing.

7. What is Maintenance?

8. Define Software Component.

9. Explain the Waterfall Model.

10. List drawbacks of the Waterfall Model.

11. Explain the Agile Manifesto.

12. Compare Waterfall and Agile.

13. What is an Interface?

14. What is the role of Requirements in software development?

15. Explain Unit Testing and Integration Testing.

---

These notes cover the concepts that are most likely to be tested from the uploaded Week 1 transcripts and are organized for quick revision before an exam.
