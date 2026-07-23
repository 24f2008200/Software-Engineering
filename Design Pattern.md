These four are among the most commonly used design patterns. Each solves a different kind of problem.

| Pattern      | Purpose                                    | Key Idea                                  |
| ------------ | ------------------------------------------ | ----------------------------------------- |
| **Builder**  | Construct complex objects step by step     | Separate construction from representation |
| **Adapter**  | Make incompatible interfaces work together | Convert one interface into another        |
| **Facade**   | Simplify a complex subsystem               | Provide one simple interface              |
| **Strategy** | Choose an algorithm at runtime             | Encapsulate interchangeable algorithms    |

---

# 1. Builder Design Pattern

## Purpose

Used when creating an object requires **many optional parameters** or multiple construction steps.

Instead of writing huge constructors, a **Builder** constructs the object step by step.

---

## Problem

Imagine creating a `Computer`.

It has:

* CPU
* RAM
* SSD
* GPU
* Keyboard
* Mouse
* WiFi
* Bluetooth

Without Builder:

```java
Computer c = new Computer(
    "Intel",
    16,
    512,
    "NVIDIA",
    true,
    true,
    true,
    false
);
```

Can you remember what each parameter means?

Not easily.

---

## Builder Solution

```java
Computer c = new Computer.Builder()
                    .setCPU("Intel")
                    .setRAM(16)
                    .setSSD(512)
                    .setGPU("NVIDIA")
                    .build();
```

Much easier to read.

---

## Real-life example

Ordering a pizza 🍕

Instead of saying:

```
Pizza("Large", true, false, true, false, true)
```

you say:

```
Large
+ Cheese
+ Mushroom
+ Olives
```

The chef (Builder) assembles the pizza.

---

## When to use

* Many optional parameters
* Complex object creation
* Immutable objects

---

# 2. Adapter Pattern

## Purpose

Allows two incompatible classes to work together.

Think of it as a **translator**.

---

## Problem

Suppose your laptop has:

```
USB-C
```

Your projector supports:

```
HDMI
```

They cannot connect directly.

Need:

```
USB-C → HDMI Adapter
```

---

## Software Example

Suppose your application expects

```java
Printer.print()
```

But an old printer provides

```java
OldPrinter.printDocument()
```

Instead of changing either class, create:

```java
class PrinterAdapter {
    OldPrinter printer;

    void print() {
        printer.printDocument();
    }
}
```

Now the application can use the old printer.

---

## Real-life examples

* Travel plug adapter
* USB-C to HDMI adapter
* Language translator

---

## When to use

* Integrating legacy code
* Third-party libraries
* Different APIs

---

# 3. Facade Pattern

## Purpose

Provides **one simple interface** to a complicated system.

Instead of calling many classes, the client calls one class.

---

## Problem

Starting a home theater requires:

```
Turn TV on
Turn speaker on
Turn amplifier on
Select HDMI
Dim lights
Start movie
```

Too many steps.

---

## Facade Solution

```java
HomeTheaterFacade.watchMovie();
```

Internally it performs all six operations.

---

## Software Example

Suppose a bank transfer requires:

```
Authenticate user
Check balance
Validate account
Transfer money
Send notification
Generate receipt
```

Instead of

```java
authenticate();

checkBalance();

transfer();

notify();

receipt();
```

You simply call

```java
bank.transferMoney();
```

---

## Real-life example

A car dashboard.

Press

```
Start Engine
```

Behind the scenes,

* Fuel system starts
* Battery supplies power
* Engine starts
* Sensors initialize

One button hides many operations.

---

## When to use

* Complex subsystems
* Simplifying APIs
* Reducing client complexity

---

# 4. Strategy Pattern

## Purpose

Allows changing an algorithm **without changing the client code**.

Different strategies can be selected at runtime.

---

## Problem

Suppose an e-commerce website supports:

* Credit Card
* UPI
* PayPal

Without Strategy:

```java
if(payment=="UPI")
...

else if(payment=="Card")
...

else if(payment=="PayPal")
...
```

Every new payment method requires modifying the code.

---

## Strategy Solution

Create an interface:

```java
interface PaymentStrategy {
    void pay();
}
```

Implement different strategies:

```java
class CreditCardPayment
implements PaymentStrategy

class UPIPayment
implements PaymentStrategy

class PayPalPayment
implements PaymentStrategy
```

Usage:

```java
PaymentStrategy p = new UPIPayment();

p.pay();
```

Tomorrow add:

```
ApplePay
```

Just create another strategy.

---

## Real-life example

Google Maps 🚗

You choose

* Driving
* Walking
* Cycling
* Public Transport

The app (context) stays the same.

Only the route-finding algorithm (strategy) changes.

---

## When to use

* Multiple algorithms
* Runtime selection
* Avoid large `if-else` or `switch` blocks

---

# Comparison

| Pattern      | Problem Solved                                      | Real-life Example           | Example in Software                                            |
| ------------ | --------------------------------------------------- | --------------------------- | -------------------------------------------------------------- |
| **Builder**  | Construct complex objects step by step              | Ordering a customized pizza | Building a `Computer`, `House`, or `Car` object                |
| **Adapter**  | Connect incompatible interfaces                     | USB-C to HDMI adapter       | Wrapping a legacy API to match a new interface                 |
| **Facade**   | Hide subsystem complexity behind a simple interface | Car's Start button          | `BankService.transferMoney()` coordinating multiple operations |
| **Strategy** | Swap algorithms without changing client code        | Google Maps travel mode     | Different payment, sorting, or compression algorithms          |

## Quick memory trick

* 🧱 **Builder** = **Build** complex objects step by step.
* 🔌 **Adapter** = **Adapt** one interface to another.
* 🏛️ **Facade** = A **front desk** that hides complexity behind a simple interface.
* 🎯 **Strategy** = Choose the best **strategy (algorithm)** for the current situation.
