# Software Engineering – Week 3 Exam Notes

## User Interface Design, Usability, Prototyping and Heuristic Evaluation

Week 3 introduces **Human-Computer Interaction (HCI)** concepts. The focus shifts from *what the software should do* (requirements) to *how users interact with it*. A good user interface should not only implement the required functionality but also provide a positive, intuitive user experience. 

---

# 1. User Interface (UI)

## Definition

A **User Interface (UI)** is the point of interaction between the user and the software system.

Examples

* Web pages
* Mobile apps
* Desktop applications
* ATM screens
* Self-service kiosks

A UI contains elements such as

* Buttons
* Text boxes
* Menus
* Navigation bars
* Icons

---

## Why is UI important?

Users judge software by its interface first.

A poor interface can make even a powerful system difficult to use.

Good UI should be

* Easy to learn
* Easy to use
* Intuitive
* Attractive
* Efficient



---

# 2. Interaction Design

## Definition

Interaction Design is the process of designing interactive products that satisfy user needs and provide a good user experience.

---

## Interaction Design Process

Memorize this sequence.

1. Identify needs and requirements
2. Develop alternative designs
3. Build interactive versions (prototypes)
4. Evaluate the interface



---

# 3. Usability

## ISO Definition

Usability is

> **The extent to which a product can be used by specified users to achieve specified goals effectively, efficiently, safely, with learnability and memorability.**



---

# 4. Usability Goals

There are **five major usability goals**.

Memorize all five.

---

## A. Effectiveness

### Definition

How well the system performs the intended task.

Questions

* Does it solve the user's problem?
* Does it provide the required functionality?

Examples

* Google Search
* Amazon Product Search

Characteristics

* Correct functionality
* Accurate results
* Completes intended work



---

## B. Efficiency

### Definition

Efficiency measures how quickly and easily users complete tasks.

Characteristics

* Few clicks
* Less typing
* Saves time
* High productivity

Example

Amazon stores

* address
* payment information

to reduce repeated work.



---

## C. Safety

### Definition

Protect users from

* dangerous situations
* accidental mistakes

Two aspects

### Physical Safety

Example

Medical systems

Chemical plants

Aircraft software

Example discussed

Therac-25 radiation therapy machine accident caused by software/interface problems.

---

### Protection from User Errors

Examples

* Undo
* Confirmation before delete
* Separate Save and Close buttons



---

## D. Learnability

### Definition

How easy it is for a new user to learn the system.

Good interfaces require

* little training
* obvious controls
* familiar layout

Example

Smartphone apps.

---

## E. Memorability

### Definition

How easily users remember the interface after not using it for some time.

Good UI should

* use consistent layout
* use familiar icons
* avoid confusing navigation

---

# Summary Table

| Goal          | Meaning            |
| ------------- | ------------------ |
| Effectiveness | Does the right job |
| Efficiency    | Does it quickly    |
| Safety        | Prevents mistakes  |
| Learnability  | Easy to learn      |
| Memorability  | Easy to remember   |

---

# 5. User Experience (UX)

UX is broader than usability.

It includes

* Enjoyment
* Satisfaction
* Emotional response
* Trust
* Aesthetics

Good UX means

Users enjoy using the product.

---

# 6. Why shouldn't we start coding immediately?

This is a common exam question.

Reasons

* Initial ideas may not be the best.
* Coding is expensive.
* Changes become costly.
* Users may reject the first design.
* Better to test ideas before coding.

Solution

**Build prototypes first.**



---

# 7. Prototype

## Definition

A prototype is an early version of the software used to test ideas before building the final product.

---

## Why Prototype?

Purposes

* Test technical feasibility
* Clarify vague requirements
* Obtain user feedback
* Evaluate interface
* Compare design alternatives



---

# 8. Fidelity

## Definition

Fidelity is the degree to which a prototype resembles the final product.

Low Fidelity

* Rough
* Hand drawn

High Fidelity

* Looks almost like final software



---

# 9. Types of Prototypes

Know these in order.

---

## Storyboards

### Definition

Hand-drawn comic showing

* Setting
* Sequence
* Satisfaction

Used to explain

* context
* workflow
* user interaction

Lowest fidelity.



---

## Paper Prototype

Made using

* paper
* sketches
* sticky notes

Advantages

* Cheap
* Quick
* Easy to modify

---

## Digital Mock-up

Created using software like

* Figma
* Photoshop
* PowerPoint

Looks similar to final product.

---

## Interactive Prototype

Clickable interface.

Users can actually interact.

Very close to final product.

---

## Prototype Progression

Storyboards

↓

Paper Prototype

↓

Digital Mock-up

↓

Interactive Prototype

↓

Final Product



---

# 10. UI Evaluation

Once a prototype is built, it must be evaluated.

Methods

1. Test with real users
2. Expert review
3. Heuristic Evaluation



---

# 11. Heuristic Evaluation

## Definition

Heuristic Evaluation is the inspection of a user interface using established usability principles (heuristics) instead of relying only on user testing.

Heuristics are practical design guidelines derived from experience. 

---

# 12. Nielsen's Design Heuristics

The course groups them into three categories.

---

# A. Understanding Heuristics

These help users understand the interface.

---

## 1. Consistency

Meaning

Same operations should behave similarly throughout the interface.

Example

Same icon

Same button colour

Same navigation.

---

## 2. Familiar Language

Use language users already know.

Avoid technical jargon.

Example

Use

"Delete"

instead of

"Deallocate Resource"

---

## 3. Clean and Functional Design

Avoid unnecessary information.

Minimal interfaces are easier to use.

Example

Google homepage.



---

# B. Action Heuristics

---

## 1. Freedom

Users should be free to

* Undo
* Redo
* Cancel
* Recover deleted items
* Explore features

Examples

* Ctrl + Z
* Trash recovery
* Browse products without login



---

## 2. Flexibility

Interface should support

* Beginners
* Experts

Examples

* Keyboard shortcuts
* Auto-complete
* Personalization

---

## 3. Recognition rather than Recall

Users should recognize options rather than remember commands.

Examples

* Menus
* Icons
* Suggestions
* Auto-complete

---

# C. Feedback Heuristics

---

## 1. Show Status

Always tell users

* Loading
* Progress
* Success
* Failure

Examples

* Progress bar
* Download percentage
* Loading spinner



---

## 2. Prevent Errors

Design should stop users from making mistakes.

Examples

* Disable invalid buttons
* Confirm delete
* Input validation

---

## 3. Support Error Recovery

If errors occur,

Help users recover.

Examples

* Undo
* Restore
* Retry

---

## 4. Provide Help

Offer

* Help pages
* Documentation
* Tooltips
* FAQs

---

# Summary of Heuristics

| Understanding     | Action                  | Feedback               |
| ----------------- | ----------------------- | ---------------------- |
| Consistency       | Freedom                 | Show Status            |
| Familiar Language | Flexibility             | Prevent Errors         |
| Clean Design      | Recognition over Recall | Support Error Recovery |
|                   |                         | Provide Help           |

---

# 13. Important Definitions

### User Interface

Point of interaction between user and software.

---

### Interaction Design

Designing interfaces that satisfy user needs.

---

### Usability

Extent to which users achieve goals effectively, efficiently and safely.

---

### Prototype

Early model of software.

---

### Fidelity

How closely prototype resembles final product.

---

### Storyboard

Hand-drawn sequence showing user interaction.

---

### Heuristic

Practical usability guideline derived from experience.

---

### Heuristic Evaluation

Evaluation of UI using usability principles.

---

# Comparison Questions

## Prototype vs Final Product

| Prototype      | Final Product       |
| -------------- | ------------------- |
| Early version  | Complete software   |
| Cheap          | Expensive           |
| Easy to modify | Difficult to modify |
| Testing ideas  | Used by customers   |

---

## Low Fidelity vs High Fidelity

| Low Fidelity | High Fidelity         |
| ------------ | --------------------- |
| Hand drawn   | Looks real            |
| Cheap        | Expensive             |
| Quick        | Detailed              |
| Storyboards  | Interactive prototype |

---

## Usability vs User Experience

| Usability    | User Experience |
| ------------ | --------------- |
| Ease of use  | Overall feeling |
| Objective    | Subjective      |
| Efficiency   | Satisfaction    |
| Learnability | Emotions        |

---

# Likely Exam Questions

### Short Answer

1. Define User Interface.
2. What is Interaction Design?
3. Define Usability.
4. List the five usability goals.
5. Define Prototype.
6. What is Fidelity?
7. What is a Storyboard?
8. What is Heuristic Evaluation?
9. What is Freedom heuristic?
10. What is Recognition over Recall?

---

### Long Answer

1. Explain the Interaction Design process.
2. Explain the five usability goals with examples.
3. Explain why prototyping is important.
4. Describe different types of prototypes.
5. Explain Nielsen's Heuristic Evaluation.
6. Explain heuristics for Understanding, Action and Feedback.
7. Compare Low-Fidelity and High-Fidelity prototypes.

---

# One-Page Revision Sheet

* UI = Interaction point between user and software.
* Interaction Design = Requirements → Design → Prototype → Evaluate.
* Usability = Effectiveness + Efficiency + Safety + Learnability + Memorability.
* UX = Overall user satisfaction.
* Prototype = Early version for testing ideas.
* Fidelity = Similarity to final product.
* Prototype order: Storyboard → Paper → Digital → Interactive → Final Product.
* Evaluate UI using: Users + Experts + Heuristic Evaluation.
* Understanding heuristics: Consistency, Familiar Language, Clean Design.
* Action heuristics: Freedom, Flexibility, Recognition over Recall.
* Feedback heuristics: Show Status, Prevent Errors, Support Recovery, Provide Help.
