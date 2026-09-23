# Bank Management System

A console-based **Bank Management System** developed in **C++** as a practical application of programming, algorithms, file handling, and problem-solving concepts.

The project was initially based on the Bank Management System developed during **Programming Advices Courses 6 & 7**, and was then extended with additional features and improvements.

---

## Features

### Client Management

* Show all clients
* Add new clients
* Delete clients
* Update client information
* Find clients by Account Number
* Prevent duplicate Account Numbers

### Transactions

* Deposit money
* Withdraw money
* Validate withdrawal amount against account balance
* Show total balances

### User Management

* Add new users
* Delete users
* Update users
* Find users
* Prevent duplicate usernames
* Protect the `Admin` user from deletion

### Login System

* Username and password authentication
* Current user tracking
* Access control based on user permissions

### Permissions System

Users can be assigned different permissions for:

* List Clients
* Add New Client
* Delete Client
* Update Client
* Find Client
* Transactions
* Manage Users
* Full Access

The project uses a permission system based on **bitwise operations**.

---

## File Handling

The system stores its data using text files:

```text
Clients.txt
Users.txt
```

The application supports:

* Reading data from files
* Adding new records
* Updating records
* Deleting records
* Saving modified data
* Loading records into vectors for processing

---

## Technical Concepts

This project applies several C++ concepts, including:

* Structures
* Functions
* Enumerations
* Vectors
* Strings
* File I/O
* Searching
* Data validation
* Record conversion
* CRUD operations
* References
* Modular programming
* Bitwise operators
* Menu-driven programming

---

## Project Structure

```text
Bank/
│
├── Bank.cpp
├── Clients.txt
├── Users.txt
├── Bank.slnx
└── Bank.vcxproj
```

---

## Development & Improvements

The project was further developed by adding and improving:

* User Management System
* Login and authentication
* Permission-based access control
* User CRUD operations
* Deposit and Withdrawal transactions
* Total balance calculation
* Client and user validation
* Duplicate record prevention
* File-based data persistence
* Permission checks using bitwise operations
* Improved menu organization
* Additional functions for searching, updating, saving, and loading records

---

## Learning Path

This project represents the practical application of concepts learned through:

### Course 6

**Introduction to Programming Using C++ – Level 2**

Key concepts applied:

* Advanced C++ programming
* Functions
* Vectors
* File handling
* Data structures
* Memory and programming concepts
* Debugging and problem solving

### Course 7

**Algorithms – Level 3**

Key concepts applied:

* Problem solving
* Algorithms
* Searching
* Data processing
* Records
* Strings and vectors
* File-based data management

---

## Technologies

* **C++**
* **Visual Studio**
* **Git**
* **GitHub**
* Text File Storage

---

## Credits

This project was developed as part of my learning journey with:

**Programming Advices**
**Dr. Mohammed Abu-Hadhoud**

The project was extended and modified to apply additional concepts and features learned during the courses.

---

