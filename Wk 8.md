Yes. Here's an exam-oriented summary of the uploaded lecture (Week 8: **Software Architecture, SOLID Principles, and Design Patterns**). I've organized it as a **revision sheet** emphasizing **definitions, key concepts, and typical exam questions** rather than every slide. 

---

# Week 8 Revision Notes

## 1. Software Architecture

### Definition

**Software Architecture** is the **way of organizing software** by defining:

* Software elements (modules/components)
* Relationships between them
* Properties of the elements and relationships

Think of architecture as the **high-level blueprint** of a software system. 

---

## 2. Architecture Styles

### A. Client-Server

**Definition**
A system where **clients send requests** and **servers process them**.

Examples

* Web applications
* Banking systems
* Gmail

Characteristics

* Centralized server
* Request-response model
* Easy to manage

---

### B. Pipe and Filter

**Definition**
Data flows through multiple components.
Each component **transforms or filters** the data before passing it to the next.

Examples

* Unix pipelines
* Compiler phases
* Image processing

Characteristics

* Independent processing stages
* Easy to reuse filters

---

### C. Peer-to-Peer (P2P)

**Definition**
A distributed architecture where every node can both **provide and consume resources**.

Characteristics

* No central server
* Nodes share storage, CPU, etc.

Examples

* BitTorrent
* Blockchain

---

### D. Model-View-Controller (MVC)

Separates an application into three parts.

### Model

Represents the data and business logic.

Example:
Database objects.

### View

Displays information to users.

Example:
HTML pages, GUI.

### Controller

Handles user input and coordinates between Model and View.

Benefits

* Separation of concerns
* Easier maintenance
* Easier testing



---

# 3. Components and Connectors

## Component

A module having a **well-defined responsibility**.

Examples

* Authentication service
* Payment service
* Database module

---

## Connector

Mechanism that enables communication between components.

Examples

* Function calls
* REST APIs
* Network protocols

Protocols define **rules** for communication.



---

# 4. Design Patterns

### Definition

Reusable solutions to common software design problems.

They describe

* communicating classes
* objects
* responsibilities
* collaborations

They are **templates**, not ready-made code.

---

## Design Smells

Warning signs indicating poor design.

Examples

* Large classes
* Duplicate code
* Too many responsibilities

---

## Refactoring

Improving internal code structure **without changing external behaviour**.

Typical refactoring includes

* Moving code
* Creating new classes
* Removing unnecessary classes



---

# 5. SOLID Principles

Probably the **highest-weight topic** in exams.

---

## S — Single Responsibility Principle (SRP)

> Every class should have **one responsibility**.

Meaning

A class should have **only one reason to change**.

Bad

```
Invoice class
    Calculates bill
    Prints bill
    Emails bill
```

Good

```
Invoice
InvoicePrinter
InvoiceMailer
```

Benefits

* Easier testing
* Easier maintenance

---

## O — Open-Closed Principle (OCP)

> Open for extension, closed for modification.

Meaning

You should **add new functionality** without modifying existing code.

Usually achieved by

* inheritance
* interfaces
* polymorphism

Example

Adding a new payment method should not require editing existing payment code.

---

## L — Liskov Substitution Principle (LSP)

> Derived classes should replace base classes without breaking the program.

Example

If

```
Bird
```

is replaced by

```
Sparrow
```

everything should still work.

If replacing with

```
Penguin
```

breaks flying behaviour,
LSP is violated.

---

## I — Interface Segregation Principle (ISP)

> Clients should not depend on methods they don't use.

Instead of

```
Animal
eat()
fly()
swim()
```

Use

```
Flyable
Swimmable
Eatable
```

Each class implements only relevant interfaces.

---

## D — Dependency Inversion Principle (DIP)

> Depend on abstractions, not concrete implementations.

Instead of

```
ShoppingCart
    uses PayTM
```

Use

```
PaymentInterface
```

Then implementations can be

* PayTM
* Google Pay
* UPI

without changing ShoppingCart.



---

# 6. Design Patterns

Three categories:

| Category    | Purpose                     |
| ----------- | --------------------------- |
| Creational  | Object creation             |
| Structural  | Organizing classes/objects  |
| Behavioural | Interaction between objects |



---

# Creational Patterns

## Factory Pattern

Problem

Object creation depends on conditions.

Instead of

```
new Truck()
new Bike()
new Car()
```

Use

```
VehicleFactory.createVehicle()
```

Advantages

* Hides object creation
* Supports OCP
* Supports SRP

Disadvantage

* More classes

---

## Builder Pattern

Problem

Objects have many optional parameters.

Instead of telescoping constructors

```
Book(...)
Book(...)
Book(...)
```

Use

```
BookBuilder
```

Advantages

* Step-by-step construction
* Cleaner code
* Easier readability

Disadvantage

* More classes



---

# Structural Patterns

## Facade Pattern

Provides a **simple interface** to a complex subsystem.

Example

One method

```
placeOrder()
```

internally performs

* Create order
* Notify seller
* Package
* Ship

Advantages

* Simplifies usage
* Hides complexity

Disadvantage

* Can become tightly coupled

---

## Adapter Pattern

Makes incompatible interfaces work together.

Example

Price stored in Dollars

Need Rupees

Adapter performs conversion.

Advantages

* Reuse existing code
* Supports OCP

Disadvantage

* Extra complexity



---

# Behavioural Patterns

## Iterator Pattern

Provides a standard way to traverse collections.

Java methods

* hasNext()
* next()

Advantages

* Collection independent
* SRP

---

## Observer Pattern

One object maintains subscribers.

Whenever state changes,
all observers are automatically notified.

Examples

* Email notifications
* YouTube subscriptions
* Stock price alerts

---

## Strategy Pattern

Encapsulates multiple algorithms into separate classes.

Instead of

```
if...
else...
else...
```

Use

```
Strategy Interface
```

Different implementations

* FIFO
* Priority
* Premium Customer

Advantages

* Easy to add new algorithms
* Supports OCP

Disadvantage

* Overkill if only one or two algorithms exist



---

# High-Probability Exam Definitions

Be able to write these in one or two sentences:

* Software Architecture
* Architecture Style
* Component
* Connector
* Protocol
* Design Pattern
* Design Smell
* Refactoring
* Factory Pattern
* Builder Pattern
* Facade Pattern
* Adapter Pattern
* Iterator Pattern
* Observer Pattern
* Strategy Pattern
* All five SOLID principles

---

# Mnemonics

### SOLID

* **S** → Single responsibility
* **O** → Open for extension
* **L** → Liskov substitution
* **I** → Interface segregation
* **D** → Dependency inversion

---

### Design Pattern Categories

**Create → Structure → Behave**

* Creational → Creates objects
* Structural → Connects objects
* Behavioural → Coordinates object interactions

---

# Most Important Topics (Exam Priority)

**★★★★★**

* SOLID Principles
* MVC Architecture
* Factory Pattern
* Builder Pattern
* Observer Pattern
* Strategy Pattern

**★★★★☆**

* Client-Server vs P2P vs Pipe-and-Filter
* Components and Connectors
* Facade and Adapter Patterns

**★★★☆☆**

* Design Smells
* Refactoring
* Iterator Pattern

This format should be sufficient for last-minute revision and covers the concepts, definitions, and distinctions most likely to appear in software engineering exams based on this lecture.
