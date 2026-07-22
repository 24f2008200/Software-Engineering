# Software Engineering – Week 2 Exam Notes

## Requirements Gathering and Analysis (IITM BS - Exam Preparation)

Week 2 focuses entirely on **Requirements Engineering**, arguably the most important phase of software development. The central idea is:

> **Build the right software before worrying about building the software right.** 

---

# 1. Requirements Engineering

## Definition

Requirements Engineering is the process of

* identifying
* gathering
* analyzing
* documenting
* organizing

the needs and expectations of stakeholders before software development begins.

---

## Why are requirements important?

Without proper requirements:

* developers build the wrong system
* customer expectations differ
* rework increases
* development cost increases
* project delays occur

The purpose is to ensure

* developers understand customers
* customers agree with developers
* fewer costly changes later



---

# 2. Requirement Gathering

## Definition

Requirement Gathering is the activity of collecting user needs before design and implementation.

It is always performed before coding.

---

## Requirement Analysis

Definition:

Studying collected requirements to

* remove ambiguity
* identify conflicts
* prioritize
* organize

before development begins.

---

# 3. Stakeholders

## Definition

A stakeholder is **any person or organization affected by the software system.**

Stakeholders are not only customers.

Examples

* End users
* Managers
* Developers
* Banks
* Logistics companies
* Government agencies



---

# 4. Types of Users

Know these very well.

## Primary Users

Use the system directly and frequently.

Examples

* Sellers
* Authors
* Company sales teams

---

## Secondary Users

Support or administer the system.

Examples

* Advertising department
* Logistics managers

---

## Tertiary Users

Indirectly affected.

Examples

* Banks
* Government
* Auditors

---

# 5. Requirement Gathering Techniques

These are favourite exam questions.

---

## A. Questionnaire

### Definition

A questionnaire is a structured set of questions used to collect information from many users.

Best suited when

* many users
* geographically distributed
* specific questions

Advantages

* inexpensive
* fast
* large audience

Disadvantages

* limited interaction
* no follow-up clarification



---

## B. Interview

### Definition

A direct interaction with stakeholders to understand their needs.

Can be

* Face-to-face
* Telephone
* Online

Types

### Structured

Fixed questions.

Easy to compare responses.

---

### Unstructured

Open discussion.

Useful when requirements are unclear.

---

### Semi-Structured

Combination of both.

Most commonly used.



---

## Other techniques (Know the names)

* Observation
* Existing documentation
* Brainstorming
* Workshops
* Prototyping

---

# 6. Functional Requirements

## Definition

Functional Requirements specify

**what the software should do.**

They describe

* inputs
* processing
* outputs

Examples

* User can login
* Seller can add products
* Customer can delete cart items

Functional requirements behave like mathematical functions

Input → Processing → Output



---

# 7. Non-functional Requirements

## Definition

Non-functional requirements specify

**how well the system should work.**

They describe quality attributes.

Examples

* Response within 5 seconds
* 99.99% availability
* Secure login
* Easy to use
* Reliable

These describe behavior rather than functionality.



---

# Functional vs Non-functional Requirements

| Functional       | Non-functional                     |
| ---------------- | ---------------------------------- |
| What system does | How system performs                |
| Features         | Quality attributes                 |
| Inputs → Outputs | Performance, Security, Reliability |
| Login            | Login within 2 seconds             |
| Add Product      | Available 24×7                     |

---

# 8. Software Requirement Specification (SRS)

## Definition

SRS (Software Requirement Specification) is the formal document containing all software requirements in an organized structure.

It serves as an agreement between

* customers
* developers

In the Plan-and-Document approach, a system analyst gathers requirements and organizes them into the SRS. 

---

## Purpose of SRS

* Clear communication
* Avoid misunderstandings
* Guide design
* Guide testing
* Basis for maintenance

---

## Major Sections of SRS

### 1. Introduction

Contains

* Purpose
* Scope
* Definitions
* References

---

### 2. Overall Description

Contains

* Product perspective
* Product functions
* Constraints
* Assumptions
* Dependencies

---

### 3. Specific Requirements

Contains

* Functional requirements
* Non-functional requirements
* External interfaces
* System features



---

# External Interface Requirements

Know these four.

* User Interface
* Hardware Interface
* Software Interface
* Communication Interface

These specify how the software interacts with external entities.

---

# 9. Behaviour Driven Design (BDD)

BDD belongs to Agile.

## Definition

Behaviour Driven Design is an Agile requirement approach that focuses on the behaviour of the application before and during development.

Instead of writing large SRS documents once, requirements are refined continuously through stakeholder feedback. 

---

## Goals

* Better communication
* Less misunderstanding
* Continuous refinement
* Stakeholder collaboration

---

# 10. User Stories

This is one of the most important topics.

## Definition

A User Story is

> A short, informal description of a feature from the user's perspective.

Characteristics

* plain language
* small
* valuable
* completed within one sprint (1–2 weeks)



---

## Standard User Story Format

Memorize this exactly.

**As a** `<type of user>`

**I want** `<feature/action>`

**So that** `<benefit/value>`

---

### Example

As a seller

I want to view inventory

So that I know which products are running low.

---

Another example

As a seller

I want to view customer feedback

So that I understand product issues.



---

# Benefits of User Stories

* Lightweight
* Easy to understand
* Easy to prioritize
* Encourage discussion
* Focus on user value
* Suitable for Agile

They describe **what users need**, not **how developers will implement it**. 

---

# 11. SRS vs User Stories

| SRS                 | User Stories         |
| ------------------- | -------------------- |
| Large document      | Small cards          |
| Waterfall           | Agile                |
| Complete upfront    | Evolve continuously  |
| Formal              | Informal             |
| Heavy documentation | Lightweight          |
| Fixed requirements  | Continuously refined |

---

# 12. Most Important Definitions

### Requirement

A capability or condition needed by a user.

---

### Stakeholder

Anyone affected by the software.

---

### Functional Requirement

Specifies **what** the system should do.

---

### Non-functional Requirement

Specifies **how well** the system should perform.

---

### Requirement Gathering

Collecting stakeholder needs.

---

### Requirement Analysis

Understanding and organizing requirements.

---

### SRS

Formal document containing software requirements.

---

### Behaviour Driven Design (BDD)

Agile approach that captures and refines requirements through user behaviour and collaboration.

---

### User Story

Short description of a feature from the user's viewpoint.

---

### Sprint

A short Agile iteration (typically **1–2 weeks**) during which one or more user stories are implemented. 

---

# Likely Exam Questions

### Short Answer

1. Define Requirement Engineering.
2. Why is Requirement Gathering important?
3. Define Stakeholder.
4. Differentiate Primary, Secondary and Tertiary users.
5. Define Functional Requirement.
6. Define Non-functional Requirement.
7. What is an SRS?
8. What is Behaviour Driven Design?
9. What is a User Story?
10. Write the User Story template.

---

### Long Answer

1. Explain Requirement Gathering and Analysis.
2. Explain different Requirement Gathering Techniques.
3. Compare Functional and Non-functional Requirements.
4. Explain the structure of an SRS document.
5. Compare SRS and User Stories.
6. Explain Behaviour Driven Design with examples.
7. Explain the advantages of User Stories.

---

# One-Page Revision Sheet

* Requirement Engineering = Gather → Analyze → Document requirements.
* Stakeholders = Anyone affected by the software.
* Primary users = Direct users.
* Secondary users = Support users.
* Tertiary users = Indirect users.
* Questionnaire = Large audience.
* Interview = Detailed discussion.
* Functional = **What** the software does.
* Non-functional = **How well** it performs.
* SRS = Formal requirement document (Waterfall).
* BDD = Agile requirement approach.
* User Story = "As a... I want... So that..."
* Sprint = 1–2 weeks.
* User Stories are lightweight, customer-focused, and continuously refined.
