For exams (especially **Software Engineering, UML, NPTEL, ISTQB**), you really only need to memorize about **8-10 UML relationships and symbols**. Here's a compact cheat sheet.

---

# 1. Association (Knows / Uses)

### Symbol

```text
ClassA -------- ClassB
```

or

```text
ClassA -------> ClassB
```

(navigable association)

### Meaning

One class **uses or knows about** another.

Example:

```text
Student -------- Course
```

A student enrolls in a course.

### Java example

```java
class Student {
    Course course;
}
```

Remember:

> Association = **"has a reference to."**

---

# 2. Aggregation (Weak HAS-A)

### Symbol

```text
ClassA ◇-------- ClassB
```

(Hollow diamond)

Diamond is on the **owner** side.

### Meaning

The part can exist independently.

Example

```text
Department ◇------ Employee
```

Employees still exist even if the department closes.

Java

```java
class Department {
    List<Employee> employees;
}
```

Employees can belong elsewhere.

### Memory trick

> Hollow diamond = Loose ownership

---

# 3. Composition (Strong HAS-A)

### Symbol

```text
ClassA ◆-------- ClassB
```

(Filled diamond)

### Meaning

The part cannot exist independently.

Example

```text
House ◆------ Room
```

Destroy the house, the rooms are gone.

Another example

```text
Human ◆------ Heart
```

### Java

```java
class House {

    private Room room = new Room();

}
```

House creates and owns the room.

### Memory trick

> Black diamond = Strong ownership

---

# 4. Inheritance (IS-A)

### Symbol

```text
       △
       |
Child ---- Parent
```

(Hollow triangle)

Actually drawn as

```text
Child --------▷ Parent
```

Example

```text
Car
   △
Vehicle
```

Means

```text
Car IS-A Vehicle
```

Java

```java
class Car extends Vehicle
```

### Memory trick

Triangle always means

> IS-A

---

# 5. Realization (Implements Interface)

### Symbol

```text
- - - -▷
```

Dashed line + hollow triangle

Example

```text
Printer --------▷ Printable
```

Java

```java
class Printer implements Printable
```

### Memory trick

Dashed triangle

=

implements

---

# 6. Dependency (Temporary Use)

### Symbol

```text
--------->
```

Dashed arrow

### Meaning

Uses temporarily.

Example

```java
void print(Book book)
```

Book isn't stored.

Only used.

### Memory trick

Dependency

=

uses for a while.

---

# 7. Multiplicity

Shows **how many objects** participate.

Example

```text
Teacher 1 -------- * Student
```

Means

One teacher

Many students

Common notations

```text
1

0..1

*

0..*

1..*

5

2..5
```

Examples

```text
Person 1 ---- 1 Passport

Company 1 ---- * Employee

Library 1 ---- * Book

Student * ---- * Course
```

---

# 8. Visibility Symbols

Inside a class

```text
+ public

- private

# protected

~ package/default
```

Example

```text
-------------------------
Employee
-------------------------
-id : int
+name : String
#salary : double
~address : String
-------------------------
```

---

# 9. Abstract Class

Class name

```text
Vehicle
```

is written

*italic*

or

```text
<<abstract>>
Vehicle
```

Method

```text
calculate()
```

also italic.

Java

```java
abstract class Vehicle
```

---

# 10. Interface

Shown as

```text
<<interface>>
Printable
```

or

```text
○ Printable
```

Java

```java
interface Printable
```

---

# Complete Memory Table

| UML Symbol                | Relationship          | Java Equivalent   | Memory Trick                       |
| ------------------------- | --------------------- | ----------------- | ---------------------------------- |
| `────`                    | Association           | Object reference  | Knows/Uses                         |
| `────>`                   | Navigable Association | One-way reference | Can access only one direction      |
| `◇────`                   | Aggregation           | Has-a (weak)      | Hollow diamond = independent       |
| `◆────`                   | Composition           | Has-a (strong)    | Black diamond = lifetime dependent |
| `────▷` (hollow triangle) | Inheritance           | `extends`         | IS-A                               |
| `- - -▷`                  | Realization           | `implements`      | Dashed = interface                 |
| `- - ->`                  | Dependency            | Temporary use     | Uses temporarily                   |
| `1`, `*`, `0..*`          | Multiplicity          | Number of objects | Cardinality                        |
| `+`                       | Public                | `public`          | Everyone                           |
| `-`                       | Private               | `private`         | Class only                         |
| `#`                       | Protected             | `protected`       | Family                             |
| `~`                       | Package               | default           | Same package                       |

---

# One-minute exam trick

If you see:

```text
◇
```

👉 Aggregation (weak has-a)

If you see:

```text
◆
```

👉 Composition (strong has-a)

If you see:

```text
△
```

👉 Inheritance (`extends`)

If you see:

```text
- - -▷
```

👉 Interface (`implements`)

If you see:

```text
-------->
```

👉 Dependency (temporary use)

If you see:

```text
--------
```

👉 Association

These six symbols alone cover **over 90% of UML relationship questions** that typically appear in software engineering exams.


The correct answer is:

✅ **Seller and Inventory have an association relationship.**

### Let's analyze the scenario

* The **Seller** class **uses** the `Inventory` class by calling:

  ```java
  Inventory.viewInventory(sellerID);
  ```
* This means the `Seller` class knows about and interacts with the `Inventory` class.

This is an **association** relationship.

---

### Why the other options are incorrect

#### ❌ Seller and Inventory have an inheritance relationship

Inheritance means one class extends another.

Example:

```java
class Seller extends Inventory
```

There is nothing in the question suggesting that `Seller` is a type of `Inventory`.

---

#### ✅ Seller and Inventory have an association relationship

Association means one class **uses** or **communicates with** another.

Example:

```java
class Seller {
    Inventory inventory;

    void showProducts(int sellerID) {
        inventory.viewInventory(sellerID);
    }
}
```

Here, `Seller` uses `Inventory`, so this is an association.

---

#### ❌ Inventory and InventoryInterface have a dependency relationship

The question states:

> **Inventory implements InventoryInterface**

In UML, **implementing an interface is a realization relationship**, not a dependency.

Example:

```java
interface InventoryInterface {
    void viewInventory(int sellerID);
}

class Inventory implements InventoryInterface {
    public void viewInventory(int sellerID) { ... }
}
```

So the relationship is **realization (implements)**, not dependency.

---

#### ❌ Seller and InventoryInterface have a composition relationship

Composition means one object **owns** another, and the owned object's lifetime depends on the owner.

Example:

```java
class House {
    private Room room = new Room();
}
```

If the `House` is destroyed, the `Room` is destroyed too.

There is nothing in the scenario indicating that `Seller` owns an `InventoryInterface` object.

---

## Final Answer

✅ **Seller and Inventory have an association relationship.**

### Quick revision of UML relationships

| Relationship                     | Meaning                                                      | Example                                   |
| -------------------------------- | ------------------------------------------------------------ | ----------------------------------------- |
| **Association**                  | One class uses or knows about another                        | `Seller` uses `Inventory`                 |
| **Inheritance (Generalization)** | "is-a" relationship                                          | `Car extends Vehicle`                     |
| **Realization**                  | A class implements an interface                              | `Inventory implements InventoryInterface` |
| **Dependency**                   | Temporary use, often as a method parameter or local variable | `print(Document d)`                       |
| **Composition**                  | Strong ownership ("part-of")                                 | `House` contains `Room`                   |


The correct answer is:

✅ **Interaction diagram**

### Explanation

The question asks:

> **Which diagram models the sequence of message exchanges among parts of a system?**

In UML, **Interaction diagrams** are specifically used to show **how objects or components communicate by exchanging messages**.

Interaction diagrams include:

* **Sequence Diagram** (shows messages in time order)
* **Communication (Collaboration) Diagram** (shows object interactions)

---

### Why the other options are incorrect

#### ❌ Class Diagram

Shows the **static structure** of the system:

* Classes
* Attributes
* Methods
* Relationships (association, inheritance, etc.)

It does **not** show message exchanges.

---

#### ❌ State Machine Diagram

Shows how an object changes **state** in response to events.

Example:

```text
New Order
    ↓
Processing
    ↓
Shipped
    ↓
Delivered
```

It models state transitions, not interactions between objects.

---

#### ❌ Activity Diagram

Shows the **workflow** or sequence of activities in a business process or algorithm.

Example:

```text
Login
  ↓
Validate User
  ↓
Show Dashboard
```

It focuses on activities, not object-to-object messages.

---

#### ✅ Interaction Diagram (Correct)

Shows:

* Which objects participate
* What messages they exchange
* The order in which messages are sent

Example:

```text
Customer → OrderService : placeOrder()

OrderService → Inventory : checkStock()

Inventory → PaymentService : processPayment()

PaymentService → OrderService : paymentSuccess()
```

This is exactly what the question describes.

---

## Quick Revision Table

| UML Diagram               | Purpose                                        |
| ------------------------- | ---------------------------------------------- |
| **Class Diagram**         | Static structure (classes and relationships)   |
| **State Machine Diagram** | States and transitions of an object            |
| **Activity Diagram**      | Workflow or business process                   |
| **Interaction Diagram** ✅ | Sequence of messages exchanged between objects |

### ✅ Correct Answer: **Interaction Diagram**
