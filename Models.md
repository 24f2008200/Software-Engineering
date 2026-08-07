The correct answer is **✅ Agile model**.

The clues are **user stories, sprints, and Test-Driven Development (TDD)**. These are strongly associated with Agile software development.

> **Note:** It is **TDD**, not TTD: *Test-Driven Development*.

### 1. Agile Model 🏃

Agile develops software **incrementally and iteratively**, usually in short cycles called **sprints**.

Typical flow:

**Product idea → User stories → Prioritize backlog → Sprint planning → Design/Code → Testing (often TDD) → Review → Retrospective → Next sprint**

Key concepts:

* **User stories**: Describe requirements from the user's perspective.

  * Example: *"As a customer, I want to reset my password so that I can regain access to my account."*
* **Product backlog**: List of all desired features/tasks.
* **Sprint**: Short development cycle, commonly 1–4 weeks.
* **Daily stand-up**: Short team meeting to discuss progress/blockers.
* **TDD**: Write a test first → write code to pass it → refactor.
* **Sprint review**: Demonstrate completed work.
* **Sprint retrospective**: Discuss what went well and what should improve.

**Main idea:** Build → get feedback → improve → build again.

---

# Now compare it with the other models

A useful way to remember them is:

| Model         | Basic idea                                           | Typical sequence                                                       |
| ------------- | ---------------------------------------------------- | ---------------------------------------------------------------------- |
| **Waterfall** | Everything happens in a fixed sequence               | Requirements → Design → Coding → Testing → Deployment → Maintenance    |
| **Prototype** | Build a quick model to understand requirements       | Requirements → Prototype → User feedback → Refine → Build final system |
| **Spiral**    | Develop in cycles while managing risks               | Planning → Risk analysis → Engineering → Evaluation → Repeat           |
| **Agile**     | Develop in short iterations with continuous feedback | Backlog → Sprint → Build/Test → Review → Improve → Repeat              |

---

## 2. Waterfall Model 💧

Waterfall is a **sequential model**. One phase is substantially completed before moving to the next.

### Steps

**1. Requirements**

* Gather and document all requirements.
* Example: What should the banking application do?

⬇️

**2. System Design**

* Decide architecture, database, interfaces, modules, etc.

⬇️

**3. Implementation / Coding**

* Developers write the actual code.

⬇️

**4. Testing**

* Test the completed software for defects.

⬇️

**5. Deployment**

* Release the software to users.

⬇️

**6. Maintenance**

* Fix bugs and make necessary changes after release.

### Memory trick

**R → D → C → T → D → M**

> **Requirements → Design → Coding → Testing → Deployment → Maintenance**

### Important characteristic

Requirements are expected to be **relatively stable and well understood upfront**.

So if the customer suddenly says:

> "We actually need 15 more features!"

Waterfall can become painful because going backward to earlier phases is expensive.

---

# 3. Prototype Model 🧪

The Prototype model is useful when **requirements are unclear or difficult for users to express**.

Instead of spending a huge amount of time building the entire system, developers create a **quick prototype**.

### Steps

**1. Initial requirements**

⬇️

**2. Quick design**

Create a rough version of the system.

⬇️

**3. Build prototype**

For example, create a rough UI showing:

`Login → Dashboard → Account → Transfer Money`

⬇️

**4. User evaluation**

Users interact with it and say:

> "This button should be here."

> "We don't need this screen."

> "We need another option."

⬇️

**5. Refine prototype**

Modify it based on feedback.

⬇️

**6. Repeat**

Keep refining until requirements are sufficiently understood.

⬇️

**7. Develop the actual system**

Build the final product based on the clarified requirements.

### Memory trick

**Build → Show → Get feedback → Improve → Repeat**

### Why use it?

Suppose a customer says:

> "I need an easy-to-use hospital management system."

That's vague.

Instead of immediately building the whole thing, you can show them a prototype and discover what they actually mean.

---

# 4. Spiral Model 🌀

The Spiral model is particularly focused on **risk management**.

It combines ideas from iterative development and systematic development.

Each loop of the spiral represents another cycle of development.

### Four major activities in each spiral

**1. Planning**

Determine:

* Objectives
* Requirements
* Alternatives
* Constraints

⬇️

**2. Risk Analysis**

Identify and evaluate risks.

For example:

> "Can this technology handle 10 million users?"

> "Is the encryption approach secure enough?"

> "Can we integrate with the existing system?"

This is the **most distinctive feature of Spiral**.

⬇️

**3. Engineering / Development**

Develop and test the selected solution.

⬇️

**4. Customer Evaluation**

Get feedback and determine what should happen in the next cycle.

Then the spiral goes around again.

### Memory trick

**Plan → Risk → Build → Evaluate → Repeat**

---

# The key differences

Imagine you're building a **food-delivery application**.

### Waterfall

You say:

> "Let's determine EVERYTHING first."

Then:

**Requirements → Design → Code → Test → Release**

Changes later are difficult.

---

### Prototype

You say:

> "We're not really sure what the customer wants. Let's build a rough version first."

**Rough app → Customer sees it → Feedback → Improve**

The prototype helps **discover requirements**.

---

### Spiral

You say:

> "This project has serious technical and financial risks. Let's identify and tackle those risks in each cycle."

**Plan → Analyze risks → Develop → Evaluate → Repeat**

The focus is **risk management**.

---

### Agile

You say:

> "Let's deliver useful pieces quickly and continuously adapt based on feedback."

**Backlog → Sprint → Develop → Test → Review → Retrospective → Next sprint**

The focus is **incremental delivery + adaptability + continuous customer feedback**.

---

## ⭐ Exam-oriented comparison

| Feature                    | Waterfall              | Prototype                 | Spiral              | Agile            |
| -------------------------- | ---------------------- | ------------------------- | ------------------- | ---------------- |
| Sequential phases          | ✅                      | Partly                    | ❌                   | ❌                |
| Iterative                  | ❌                      | ✅                         | ✅                   | ✅                |
| User stories               | ❌                      | Not characteristic        | Not characteristic  | ✅                |
| Sprints                    | ❌                      | ❌                         | ❌                   | ✅                |
| TDD                        | ❌                      | ❌                         | ❌                   | ✅ Common         |
| Continuous feedback        | ❌                      | ✅                         | ✅                   | ✅                |
| Risk analysis emphasis     | ❌                      | ❌                         | **✅ Strong**        | Some             |
| Requirements known upfront | **✅ Usually**          | ❌                         | Not necessarily     | ❌                |
| Quick prototype            | ❌                      | **✅ Core idea**           | Sometimes           | Sometimes        |
| Frequent releases          | ❌                      | Usually not the main goal | Possible            | **✅**            |
| Best known for             | Sequential development | Requirement clarification | **Risk management** | **Adaptability** |

### 🎯 Quick identification rule

If the question mentions:

* **User stories**
* **Product backlog**
* **Sprints**
* **Daily stand-ups**
* **Scrum**
* **Sprint review**
* **Sprint retrospective**
* **TDD**
* **Continuous integration**
* **Frequent incremental releases**

👉 **Agile**

If it mentions:

* **Sequential phases**
* **Requirements → Design → Coding → Testing**
* **Fixed plan**
* **Minimal change**

👉 **Waterfall**

If it mentions:

* **Mock-up**
* **Quick working model**
* **User evaluates model**
* **Requirement clarification**

👉 **Prototype**

If it mentions:

* **Risk identification**
* **Risk analysis**
* **Risk-driven development**
* **Repeated cycles/loops**

👉 **Spiral**

So for your question:

> "Which model includes creating user stories, sprints, TDD, etc.?"

**Answer: ✅ Agile model.**
