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
Here's a quick-reference set of concise definitions:

**Software Architecture** — The high-level structure of a software system, comprising its components, their relationships, and the principles governing its design and evolution.

**Architecture Style** — A named collection of design decisions and constraints (e.g., layered, client-server, microservices) that shapes the structure and interaction patterns of a system.

**Component** — A modular, replaceable unit of software that encapsulates its implementation and exposes functionality through well-defined interfaces.

**Connector** — The mechanism that enables communication, coordination, or data transfer between components (e.g., method calls, message queues, pipes).

**Protocol** — A set of rules defining how components or systems exchange data, including format, sequencing, and error handling.

**Design Pattern** — A reusable, general solution to a commonly occurring problem within a given context in software design.

**Design Smell** — A structural characteristic in code or design that indicates a possible violation of design principles and may hinder maintainability or extensibility.

**Refactoring** — The process of restructuring existing code to improve its internal structure and readability without changing its external behavior.

**Factory Pattern** — A creational pattern that provides an interface for creating objects without specifying their exact concrete classes.

**Builder Pattern** — A creational pattern that separates the construction of a complex object from its representation, allowing the same construction process to create different representations.

**Facade Pattern** — A structural pattern that provides a simplified, unified interface to a larger, more complex subsystem.

**Adapter Pattern** — A structural pattern that converts the interface of one class into another interface expected by clients, allowing incompatible interfaces to work together.

**Iterator Pattern** — A behavioral pattern that provides a way to sequentially access elements of a collection without exposing its underlying representation.

**Observer Pattern** — A behavioral pattern where an object (subject) maintains a list of dependents (observers) and notifies them automatically of any state changes.

**Strategy Pattern** — A behavioral pattern that defines a family of interchangeable algorithms, encapsulating each one and allowing the algorithm to vary independently of the clients that use it.

**SOLID Principles:**
- **Single Responsibility Principle** — A class should have only one reason to change, meaning it should have only one job or responsibility.
- **Open/Closed Principle** — Software entities should be open for extension but closed for modification, allowing behavior to be extended without altering existing code.
- **Liskov Substitution Principle** — Objects of a superclass should be replaceable with objects of a subclass without affecting the correctness of the program.
- **Interface Segregation Principle** — Clients should not be forced to depend on interfaces they do not use; prefer smaller, specific interfaces over large, general-purpose ones.
- **Dependency Inversion Principle** — High-level modules should not depend on low-level modules; both should depend on abstractions, and abstractions should not depend on details.

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
Here's a breakdown highlighting what makes each pattern distinct and how to spot which one to use:

## Creational vs Structural vs Behavioral — the first filter

- **Factory, Builder** → about **creating objects**
- **Facade, Adapter** → about **organizing/connecting existing structures**
- **Iterator, Observer, Strategy** → about **managing behavior/interaction**

---

## Factory vs Builder (both create objects — but differ in *what* problem they solve)

**Factory Pattern**
- **Key idea:** Decides *which class* to instantiate based on some input/condition. One-step creation.
- **Identify it when:** You have multiple related classes implementing a common interface, and you want to hide the "which one to pick" logic from the client.
- **Example:** `ShapeFactory.create("circle")` returns a `Circle` object; `create("square")` returns a `Square`. The client never calls `new Circle()` directly.

**Builder Pattern**
- **Key idea:** Constructs a *single complex object* step-by-step, when that object has many optional parts/configurations.
- **Identify it when:** A constructor would otherwise need 8+ parameters, or an object must be built in stages.
- **Example:** `new PizzaBuilder().setSize("large").addTopping("cheese").addTopping("olives").build()`.

**Core distinction:** Factory picks *which type*; Builder assembles *one complex object's parts*.

---

## Facade vs Adapter (both simplify interfaces — but differ in *purpose*)

**Facade Pattern**
- **Key idea:** Provides a single, simplified entry point to a complex subsystem with many classes.
- **Identify it when:** A client needs to make several calls across multiple subsystem classes just to do one task, and you want to hide that complexity.
- **Example:** `HomeTheaterFacade.watchMovie()` internally turns on the projector, dims lights, and starts the sound system — the client just calls one method.

**Adapter Pattern**
- **Key idea:** Converts one *incompatible interface* into another interface the client expects — enabling two mismatched systems to work together.
- **Identify it when:** You're integrating a third-party or legacy class whose interface doesn't match what your code expects.
- **Example:** A `EuropeanPlugAdapter` lets a US-style plug (interface A) fit into a European socket (interface B).

**Core distinction:** Facade *simplifies* (fewer calls, same underlying interfaces); Adapter *translates* (bridges mismatched interfaces).

---

## Iterator vs Observer vs Strategy (behavioral — differ in what "changes" or is decoupled)

**Iterator Pattern**
- **Key idea:** Provides a standard way to traverse elements of a collection without exposing its internal structure (array, tree, linked list, etc.).
- **Identify it when:** You need to loop through a custom collection uniformly, regardless of how it's stored internally.
- **Example:** `for (Book b : library)` — `library` could be backed by an array or a hashmap; the client doesn't care.

**Observer Pattern**
- **Key idea:** One-to-many dependency — when one object's state changes, all dependents are automatically notified.
- **Identify it when:** You need an event/notification system — multiple parts of your system must react to a change without tight coupling.
- **Example:** A `WeatherStation` (subject) notifies `PhoneDisplay` and `WebDisplay` (observers) whenever the temperature updates.

**Strategy Pattern**
- **Key idea:** Encapsulates interchangeable algorithms/behaviors, letting the client choose or switch behavior at runtime.
- **Identify it when:** You have several ways to perform the *same task* (e.g., sorting, payment processing) and want to swap between them without `if-else` chains.
- **Example:** `PaymentContext.setStrategy(new CreditCardPayment())` vs `setStrategy(new PayPalPayment())` — same `pay()` call, different behavior underneath.

**Core distinction:** Iterator = "how do I *move through* data"; Observer = "how do I *react* to a change elsewhere"; Strategy = "how do I *swap* an algorithm."

---

## Quick identification cheat-sheet

| Pattern | Ask yourself... |
|---|---|
| Factory | "Do I need to create one of *several possible types* without hardcoding `new`?" |
| Builder | "Am I constructing *one object* with lots of optional configuration steps?" |
| Facade | "Am I hiding *subsystem complexity* behind a simple API?" |
| Adapter | "Am I making two *incompatible interfaces* talk to each other?" |
| Iterator | "Do I need to *traverse* a collection without exposing its internals?" |
| Observer | "Do multiple objects need to be *notified* when one object changes?" |
| Strategy | "Do I need to *swap algorithms* interchangeably at runtime?" |

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
