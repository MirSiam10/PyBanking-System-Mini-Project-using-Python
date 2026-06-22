# 🏦 PyBanking System

<img width="499" height="305" alt="pybanking_UML" src="https://github.com/user-attachments/assets/e58a7a15-1cb4-4bff-81e4-c925828d26d3" />


## Overview

**PyBanking System** is a learning-focused banking simulation project built in Python to strengthen my understanding of **Object-Oriented Programming (OOP)** and modern Python development practices.

Rather than creating a simple CRUD application, I designed this project to explore how real-world systems can be modeled using classes, inheritance hierarchies, abstract base classes, encapsulation, and polymorphism.

Through the implementation of multiple account types, transaction management, money transfers, interest calculations, and bank-level operations, I gained practical experience in writing maintainable, scalable, and object-oriented code.

---

## What I Learned

This project helped me move beyond basic Python syntax and apply several important software engineering concepts:

### Object-Oriented Programming

* Class and Object Design
* Encapsulation using protected attributes and properties
* Inheritance for extending account behavior
* Polymorphism through different withdrawal implementations
* Method overriding
* Special methods (`__str__`, `__eq__`, `__len__`)

### Advanced Python Features

* Abstract Base Classes (`ABC`)
* Abstract Methods (`@abstractmethod`)
* Dataclasses (`@dataclass`)
* Immutable objects (`frozen=True`)
* Type Hints
* Class Variables
* Properties (`@property`)
* Exception Handling

### Software Design Concepts

* Separation of Responsibilities
* Domain Modeling
* Transaction Logging
* Account Lifecycle Management
* Reusable and Extensible Architecture

---

## System Architecture

### Transaction

An immutable transaction record implemented using a frozen dataclass.

Features:

* Transaction type tracking
* Amount recording
* Automatic timestamp generation
* Immutable transaction history

### Account (Abstract Base Class)

The foundation of all account types.

Responsibilities:

* Owner management
* Balance management
* Transaction history
* Deposit operations
* Statement generation
* Unique account numbering

Every account type must implement its own withdrawal logic.

---

## Account Types

### SavingsAccount

A traditional savings account.

Features:

* Deposits and withdrawals
* No overdraft support
* Interest calculation
* Interest application history

### CheckingAccount

A checking account with overdraft support.

Features:

* Withdraw beyond available balance
* Configurable overdraft limit
* Balance protection rules

### FixedDepositAccount

A fixed-term investment account.

Features:

* Monthly interest accumulation
* Maturity period enforcement
* Withdrawal restrictions before maturity
* Account maturity tracking

---

## Bank Management System

The `Bank` class acts as the central controller of the system.

Capabilities:

* Open new accounts
* Search accounts
* Transfer money between accounts
* Calculate total bank assets
* Identify the richest customer
* Generate complete bank summaries

---

## Key OOP Concepts Demonstrated

### Abstraction

The `Account` abstract base class defines common banking behaviors while forcing child classes to implement their own withdrawal logic.

### Encapsulation

Sensitive data such as balances and account information are protected and accessed through properties and controlled methods.

### Inheritance

All account types inherit shared functionality from the `Account` class.

### Polymorphism

Each account type implements withdrawals differently while exposing the same interface.

### Composition

The banking system stores and manages transaction objects inside accounts.

---

## Example Features

✔ Deposit Funds

✔ Withdraw Funds

✔ Transfer Money Between Accounts

✔ Interest Calculation

✔ Fixed Deposit Maturity Handling

✔ Transaction History Tracking

✔ Richest Customer Detection

✔ Bank Asset Calculation

✔ Account Statements

✔ Custom String Representations

✔ Equality Comparison Between Accounts

---

## Sample Output

* Open multiple account types
* Perform deposits and withdrawals
* Apply interest
* Execute transfers
* Generate account statements
* View complete bank summary

---

## Why I Built This Project

As part of my Python learning journey, I wanted to create a project that would help me understand how Object-Oriented Programming is used in real software systems.

This project allowed me to practice designing classes, modeling business rules, managing relationships between objects, and writing cleaner, more maintainable Python code.

More importantly, it transformed theoretical OOP concepts into practical experience by simulating a real-world banking environment.

---

## Technologies Used

* Python 3
* Object-Oriented Programming (OOP)
* Dataclasses
* Abstract Base Classes (ABC)
* Type Hinting
* Exception Handling

---

## Future Improvements

* Persistent storage using SQLite/PostgreSQL
* User authentication system
* Transaction search and filtering
* Interest scheduling automation
* REST API using FastAPI
* Web-based dashboard
* Unit and integration testing

---

### Educational Purpose

This project was built primarily for learning and experimentation. Its goal is to strengthen Python programming skills and develop a deeper understanding of object-oriented software design principles through a realistic banking system simulation.
