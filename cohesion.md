The correct answer is:

✅ **Procedural cohesion**

### Step 1: Analyze the scenario

The module contains three functions:

* `UpdateStock()`
* `GenerateInventoryReport()`
* `SendLowStockNotification()`

The question states:

* They are **loosely related** in purpose.
* They perform **different tasks**.
* **They are executed one after the other.**

The key clue is **"executed one after the other."**

---

### Step 2: Match with cohesion types

#### ✅ Procedural Cohesion (Correct)

Procedural cohesion exists when:

* Elements are grouped because they **follow the same control sequence**.
* The tasks may be different, but they are executed in a particular order.

Example:

```text
Login User
↓
Load Dashboard
↓
Display Welcome Message
```

These tasks are different but are performed sequentially as part of one procedure.

This exactly matches the given scenario.

---

#### ❌ Coincidental Cohesion

Functions are grouped **without any meaningful relationship**.

Example:

```text
printInvoice()
calculateSalary()
playMusic()
```

These are unrelated and not grouped for any logical reason.

---

#### ❌ Communicational Cohesion

Functions operate on the **same data**.

Example:

```text
Read Employee Record
Update Employee Record
Print Employee Record
```

All work on the same employee data.

The question does not say the functions operate on the same data.

---

#### ❌ Sequential Cohesion

Sequential cohesion exists when:

* The **output of one function becomes the input of the next**.

Example:

```text
Read File
    ↓
Parse Data
    ↓
Generate Report
```

Each step depends on the previous one's output.

The question only says the functions are **executed one after another**, not that one function's output is used as the next function's input.

---

## Quick comparison

| Cohesion            | Meaning                                      | Key Phrase                  |
| ------------------- | -------------------------------------------- | --------------------------- |
| **Coincidental**    | Unrelated functions grouped together         | No logical relation         |
| **Procedural** ✅    | Different tasks executed in a specific order | Same procedure/control flow |
| **Communicational** | Functions use the same data                  | Shared data                 |
| **Sequential**      | Output of one function is input to the next  | Data flows between steps    |

### **Answer: ✅ Procedural cohesion**

> **Exam tip:**
>
> * **"Executed one after another"** → **Procedural cohesion**
> * **"Output of one becomes input of next"** → **Sequential cohesion**

The correct answer is:

✅ **The modules have high cohesion and are highly coupled.**

### Step 1: Analyze cohesion

The modules are:

* Product Listing Module
* Order Processing Module
* Payment Module

Each module performs **one specific task**.

This means each module has **high cohesion**.

> **High cohesion = A module focuses on a single, well-defined responsibility.**

---

### Step 2: Analyze coupling

The question states:

> **All modules need to access a shared order database** to retrieve and update order statuses, customer information, and payment details.

Since all modules depend on the same shared database, they are **dependent on a common resource**.

This indicates **high coupling** (specifically, common coupling).

---

### Why the other options are incorrect

#### ❌ Low cohesion and highly coupled

Incorrect because each module has a clear responsibility.

---

#### ❌ Low cohesion and loosely coupled

Incorrect because:

* Cohesion is high.
* They share a common database, so they are not loosely coupled.

---

#### ❌ High cohesion and loosely coupled

This would be true only if the modules interacted through well-defined interfaces or APIs without depending directly on a shared database.

In the given scenario, the shared database creates **high coupling**.

---

## Summary

| Concept      | Observation                                                                   |
| ------------ | ----------------------------------------------------------------------------- |
| **Cohesion** | Each module has one responsibility → **High cohesion**                        |
| **Coupling** | All modules depend on a shared database → **High coupling (common coupling)** |

### ✅ Correct Answer:

**The modules have high cohesion and are highly coupled.**

### Exam tip

* **One module = one task** → **High cohesion**.
* **Shared global data/database used by many modules** → **High coupling (common coupling)**.
* **Independent modules communicating via interfaces/APIs** → **Loose coupling**.
