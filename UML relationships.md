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
