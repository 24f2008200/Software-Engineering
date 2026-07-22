# Software Design — Exam Study Guide
*(Based on: Design Modularity, OOD Basic Concepts, UML Diagrams, VeriSIM, Week 5 Software Design)*

---

## 1. Foundations: What Is Design?

**Design** = a way of organising the code you will implement and providing structure to the software system.

**Outcome of the Design Process** (4 things):
1. **Components** — modules (collections of functions + shared data) that each accomplish a well-defined task.
2. **Interfaces** — how components communicate/exchange data with each other.
3. **Data structures** — how data is stored within individual components (arrays, lists, trees, etc.).
4. **Algorithms** — the logic that runs on the data to produce the desired result.

> Components + Interfaces = **Software Architecture** (the high-level design). Data structures + algorithms come at a lower level, after architecture is decided.

**Characteristics of a Good Software Design:**
| Characteristic | Meaning |
|---|---|
| **Correctness** | Correctly implements all functionalities — depends on requirements being unambiguous, non-conflicting, and complete |
| **Efficiency** | Manages resources (time, space, cost) well — e.g., embedded systems need to respect memory limits |
| **Maintainability** | Easy to change/update without redesigning from scratch |
| **Understandability** | Everyone on the team can follow the design (poor understandability → bugs, higher dev/maintenance cost) |

---

## 2. Modularity: Coupling and Cohesion

A **good design is modular**: the problem is decomposed into modules with only *limited interactions* with each other.

### Coupling
**Definition:** Measure of the degree of interaction (data/information sharing) between two modules.
- **High/tight coupling** — modules share a lot of data → hard to understand/maintain → **undesirable**
- **Low/loose coupling** — modules interact minimally → **desirable**

**Types of Coupling** (from loosest/best to worst, roughly):
| Type | Definition | Example |
|---|---|---|
| **Data coupling** | Modules communicate via primitive data types (int, float, etc.) passed as parameters | `view_inventory(seller_id)` |
| **Control coupling** | Data passed influences the internal logic/flow of the other module (flags/switches) | `perform_actions(OPERATION_FLAG)` where flag = 0/1/2 selects behavior |
| **Common coupling** | Modules share global data items | Both Seller and Inventory access a global `OPERATION_FLAG` variable — risk of unstable design from concurrent changes |
| **Content coupling** | One module directly refers to/modifies the internals of another module | Rare in procedural/OO languages (Python, Java) since data+methods are encapsulated |

### Cohesion
**Definition:** Measure of how well the functions within a single module cooperate to perform a **single objective**.
- **High cohesion** — functions serve one clear purpose → **desirable**
- **Low cohesion** — functions perform varied, unrelated operations → **undesirable**, hard to understand module's purpose

**Types of Cohesion** (best → worst):
| Type | Definition | Example |
|---|---|---|
| **Functional cohesion** (best) | All functions cooperate to complete a single specific task | Inventory module: `view_inventory()`, `add_item_to_inventory()`, `delete_item_from_inventory()` |
| **Sequential cohesion** | Functions execute in sequence; output of one feeds into the next | Order processing: `create_order()` → `check_availability()` → `place_order()` |
| **Communicational cohesion** | All functions refer to/update the same data structure | Single "Product" module handling add/edit/delete for one product list |
| **Procedural cohesion** | Activities related only by sequence, but serve entirely different purposes | Seller Portal doing `login() → add_product() → place_order() → logout()` — login/logout unrelated to order logic |
| **Coincidental cohesion** (worst) | Functions in a module have meaningless relationships to each other | Rare in good designs — an extreme/anti-pattern |

### Key Exam Point
**Ideal design = High Cohesion + Low Coupling.**
- High coupling + high cohesion, or low coupling + low cohesion are essentially contradictory/impossible in practice (high coupling generally implies low cohesion, and vice versa).
- **Low cohesion + high coupling** = worst practical case: modules do varied things AND share too much data.
- Reorganizing (moving functions between modules so each module handles one cohesive job) reduces inter-module communication → converts a "high coupling/low cohesion" design into a "low coupling/high cohesion" one.

---

## 3. Object-Oriented Design (OOD): Basic Concepts

Since good design = high cohesion + low coupling, we need a way to **represent** modules — this course uses the **object-oriented approach**.

### Object
- The key building block; software = interacting objects.
- Usually represents a tangible real-world entity (e.g., Product, Shopping Cart, Order, Payment).
- **Contains:**
  - **Data** — usually private, visible only to that object.
  - **Methods** — functions that operate on the data, usually visible to other objects.

### Encapsulation
- Bundling of data + methods together into one unit.
- Ensures **data hiding / data abstraction**: no object can directly access another object's data; access only via that object's methods.
- **Why it matters:** encapsulation is *why* OOD naturally produces high cohesion (related data & methods bundled together) and low coupling (interaction between objects minimized).

### Class
**Definition:** A template/blueprint for creating objects. All objects with similar attributes and methods constitute a class.
- Example: Electronics, Books, Clothing are all objects of type **Product**.

### Class Relationships
| Relationship | Definition | How to identify | Example |
|---|---|---|---|
| **Association** | Classes take each other's help to perform functions (one object invokes another's method) | "A delegates to B" / "A needs help from B" | Seller calls `view_inventory(seller_id)` on Inventory |
| **Composition (Aggregation)** | Whole–part relationship; one object contains other objects (composite object) | "B is a part of A" / "A contains B" / "A is a collection of B's" | Catalogue *has a* list of Products |
| **Inheritance** | New (derived) class extends features of an existing (base) class | "A is a kind of B" / "A is a specialisation of B" | Product (base) → Electronics, Books, Clothing (derived/sub-classes) |
| **Dependency** | Class B depends on Class A such that changes to A require changes to B | Common with interfaces: Class B implements Interface A | If Interface A changes, Class B (implementer) must also change |

---

## 4. UML (Unified Modeling Language) Diagrams

**Modeling** = creating an external, explicit representation of the system to be built.
**UML** helps represent software design via **multiple views** and varying levels of detail.

### Two Important Views
| View | Describes | Notes |
|---|---|---|
| **Structural View** | Structure/components of the system and their relationships (classes, data, functions) — *static*, not time-dependent | Main diagram: **Class Diagram** |
| **Dynamic Behavioural View** | Behaviour of the system *over time* | Sub-types: **State Machine View**, **Activity View**, **Interaction View** |

### Class Diagram (Structural View)
- The main building block of OO modeling.
- Each class is a box with **3 compartments**:
  1. Class name (top)
  2. Attributes/data members (middle)
  3. Operations/methods (bottom)
- Shows relationships: composition, inheritance, association, dependency (as covered above).

### Dynamic Behavioural View — Sub-types
- **State Machine View** — models the different states of an object of a class.
- **Activity View** — models flow of control among computational activities/workflow steps.
- **Interaction View** — models the sequence of message exchanges among parts of the system (gives a holistic view of behavior/flow of control across objects).

### Sequence Diagram (a type of Interaction View)
- Represents the behaviour for one specific requirement/user story.
- Components:
  - Boxes at top = objects/classes involved (e.g., User, UI Screen, Controller, Seller).
  - **Lifelines** = vertical dashed lines under each object showing its timeline.
  - **Horizontal arrows** = messages exchanged between objects, in the order they occur (these often correspond to method calls from the class diagram).

### Broader UML Diagram Family (for context — course focuses mainly on Class + Sequence diagrams)
- **Structure Diagrams**: Class, Component, Object, Profile, Composite Structure, Deployment, Package
- **Behavior Diagrams**: Activity, Use Case, State Machine, and Interaction Diagrams (Sequence, Communication, Interaction Overview, Timing)

### Purposes of UML Modelling (3 key purposes — common reflection/exam question)
1. **Vehicle for communication and idea generation** — facilitates discussion/collaboration with team members; not all details are needed upfront.
2. **Guides development of software** — initial models get progressively detailed and guide actual coding.
3. **Close correspondence with implementation (code)** — each class in the model can map to one or more classes in code; some tools can even auto-generate code from detailed UML diagrams.

> Key reminder from the lecture: Don't get bogged down in notation/diagram variety — use UML as a **thought tool** to reason about and engage with your design.

---

## 5. VeriSIM — Learning Environment

**VeriSIM** = **Veri**fying designs by **Sim**ulating scenarios.
- **Purpose:** helps develop an *integrated* understanding of Class diagrams and Sequence diagrams together.
- **Context example used:** An Automated Door Locking System with requirements like:
  1. If no passcode is set, user can register and set one.
  2. Choosing "lock" + correct passcode → door locks (incorrect passcode → stays unlocked).
  3. Choosing "unlock" + correct passcode → door unlocks (incorrect passcode → stays locked).

### Design Tracing Strategy
- Given a **scenario** (e.g., "door is locked, user selects unlock, enters correct passcode → door unlocks"), you **construct a State Diagram** that models it.
- **States** = snapshots of data variable values (taken from the **Class Diagram**, e.g., `optionSelected`, `userInputPasscode`, `systemPasscode`, `lock`).
- **Transitions** between states = **messages** (taken from the **Sequence Diagram**), e.g., "Set option to unlock," "Enters correct passcode," "Door unlocks."
- This exercise links static structure (class diagram) with dynamic behaviour (sequence diagram) into one coherent trace.

### Activities in VeriSIM (stages)
1. **Introduction** — learning objectives.
2. **Problem Understanding Stage** — understand requirements + design diagrams (with evaluation/reflection activities).
3. **Design Tracing Stage** — attempt challenges (in any order) to construct state diagrams from scenarios.
4. **Reflection Stage** — consolidate learning.

---

## Quick-Reference Cheat Sheet

- **Good design goal:** High Cohesion, Low Coupling.
- **Coupling types (worst→best is content>common>control>data... but exam framing is usually "low coupling desirable"):** Data → Control → Common → Content (increasing undesirability).
- **Cohesion types (best→worst):** Functional → Sequential → Communicational → Procedural → Coincidental.
- **OOD pillars:** Object, Class, Encapsulation (→ data hiding/abstraction).
- **Class relationships:** Association, Composition, Inheritance, Dependency.
- **UML views:** Structural (Class Diagram) vs. Dynamic Behavioural (State Machine, Activity, Interaction/Sequence Diagram).
- **Purposes of UML:** Communication tool, guide for development, correspondence to code.
- **VeriSIM:** ties Class + Sequence diagrams together via State Diagrams built through design tracing.
- **Design outcomes:** Components, Interfaces, Data structures, Algorithms (first two = Software Architecture).
- **Good design characteristics:** Correctness, Efficiency, Maintainability, Understandability.
