# Bank Management System

A console-based **Bank Management System developed in C++**, designed to manage clients, banking transactions, system users, and access permissions.

The project started as a basic client management system and was progressively developed into a more structured banking administration application by applying programming, algorithms, data structures, file handling, authentication, and permission-control concepts.

---

## Project Overview

The Bank Management System provides a complete console environment for managing:

* Clients
* Bank accounts
* Deposits and withdrawals
* System users
* User authentication
* Permissions and access control
* Persistent data storage

The current version represents the latest development of the project, while the previous implementation is preserved inside the `Library` directory for reference and comparison.

---

## Project Evolution

### Previous Version

The original implementation focused mainly on client management and basic file handling.

It provided functionality such as:

* Adding clients
* Updating clients
* Deleting clients
* Finding clients
* Displaying client information
* Saving client records to a text file

The previous implementation is preserved in:

```text
Library/Previous-Version/
```

This allows the development history of the project to remain available without interfering with the current implementation.

---

### Current Version

The current implementation extends the original system with additional functionality and improved system organization.

The latest version includes:

* User authentication
* User management
* Permission management
* Bitwise permission control
* Client management
* Banking transactions
* Deposit and withdrawal
* Balance validation
* Total balance calculation
* Data persistence
* Improved validation
* Additional algorithms and programming concepts

---

# Main Features

## 1. Client Management

The system provides complete client management functionality.

### Available Operations

* Show Clients
* Add New Client
* Update Client
* Delete Client
* Find Client

Client information is stored and retrieved using local data files.

---

## 2. User Management

The system includes a dedicated user-management system.

### User Operations

* Show Users
* Add User
* Update User
* Delete User
* Find User

Users are stored separately from client records.

```text
Users.txt
```

---

## 3. Authentication

Before accessing the main system, the user must authenticate using:

```text
Username
Password
```

The authentication process determines whether the user is allowed to enter the system.

```text
Login
  │
  ▼
Authentication
  │
  ▼
Permission Check
  │
  ▼
Main Menu
```

---

## 4. Permission System

The system uses **Bitwise Operations** to manage user permissions.

Each permission is represented by a flag, allowing multiple permissions to be combined into a single integer value.

Example:

```cpp
Read        = 1;
Add         = 2;
Update      = 4;
Delete      = 8;
Transactions = 16;
ManageUsers = 32;
```

Permissions can then be combined using the bitwise OR operator:

```cpp
Permissions = Read | Add | Update;
```

This approach allows the system to determine whether a specific user has permission to perform a particular operation.

---

## 5. Administrator Protection

The system contains protection for the main administrator account.

The administrator has full system permissions and cannot be removed or have critical privileges removed through normal user-management operations.

---

## 6. Banking Transactions

The system supports basic banking transactions.

### Deposit

Adds money to a client's account.

### Withdraw

Removes money from a client's account after validating the available balance.

### Total Balances

Calculates the total balance across client accounts.

---

# Data Storage

The project uses local text files for persistent storage.

The main files are:

```text
Clients.txt
Users.txt
```

A custom delimiter is used to separate fields:

```text
#//#
```

---

## Client Record Format

```text
AccountNumber#//#PINCode#//#Name#//#Phone#//#AccountBalance
```

Example:

```text
A1001#//#1234#//#Abdulrahman#//#0999999999#//#1500
```

---

## User Record Format

```text
Username#//#Password#//#Permissions
```

Example:

```text
Admin#//#1234#//#-1
```

Where:

```text
-1 = Full Permissions
```

---

# System Flow

```text
                    ┌───────────────┐
                    │     Login     │
                    └───────┬───────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ Authentication      │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ Permission Check    │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │     Main Menu       │
                 └──────────┬──────────┘
                            │
             ┌──────────────┼──────────────┐
             ▼              ▼              ▼
        Clients       Transactions      Users
```

---

# Project Structure

```text
Bank/
│
├── README.md
├── .gitignore
│
├── Bank.slnx
│
├── Bank/
│   ├── Source Files
│   ├── Header Files
│   └── Data Files
│
└── Library/
    └── Previous-Version/
        └── Previous Source Code
```

### Current Version

The main project directory contains the latest implementation.

### Library

The `Library` directory contains the previous implementation for:

* Reference
* Comparison
* Development history
* Reviewing previous algorithms and implementation techniques

---

# Programming Concepts

This project applies several important C++ programming concepts:

* Functions
* Structures
* Enumerations
* Vectors
* File Handling
* String Processing
* Data Validation
* CRUD Operations
* Searching
* Algorithms
* Bitwise Operations
* Authentication
* Access Control
* Modular Programming
* Object-Oriented Programming concepts

---

# Algorithms & Problem Solving

The project was developed alongside the **ProgrammingAdvices** learning path.

The latest version includes improvements and additional algorithmic concepts introduced during the development of:

**Course 8 – Algorithms Level 4**

The project demonstrates how algorithmic concepts can be applied to a larger practical application rather than being implemented only as isolated exercises.

---

# Technologies

* C++
* Visual Studio
* Standard C++ Library
* File I/O
* `std::vector`
* Bitwise Operations
* Algorithms
* Data Structures

---

# Requirements

To build and run the project, you need:

* Windows
* Visual Studio
* C++ development tools
* A C++ compiler supporting the project's language features

---

# How to Run

1. Clone the repository.

2. Open the solution:

```text
Bank.slnx
```

3. Build the project.

4. Run the application.

5. Use the login credentials available in the project's data files.

> For security reasons, real passwords should not be committed to a public repository.

---

# GitHub Setup

## 1. Initialize Git

Open the project directory in Terminal or Git Bash:

```bash
cd "path/to/Bank"
```

Initialize Git:

```bash
git init
```

---

## 2. Check the Files

```bash
git status
```

Make sure temporary Visual Studio files are ignored.

The `.gitignore` file should prevent files such as:

```text
.vs/
Debug/
Release/
*.user
*.suo
*.VC.db
```

from being committed.

---

## 3. Add the Project

```bash
git add .
```

Check what will be committed:

```bash
git status
```

---

## 4. Create the First Commit

```bash
git commit -m "Initial commit - Bank Management System"
```

---

## 5. Create the GitHub Repository

Create a new repository on GitHub.

Suggested repository name:

```text
Bank-Management-System
```

Do not create another README on GitHub if your local project already contains `README.md`.

---

## 6. Connect the Local Repository

Replace the URL with your GitHub repository URL:

```bash
git remote add origin https://github.com/ABDRHMA41/Bank-Management-System.git
```

Verify:

```bash
git remote -v
```

---

## 7. Rename the Branch

```bash
git branch -M main
```

---

## 8. Push the Project

```bash
git push -u origin main
```

After the push completes, refresh the GitHub repository.

The README will automatically appear on the repository's main page.

---

# Updating the Project Later

When you make changes to the project:

```bash
git status
```

Then:

```bash
git add .
```

Create a meaningful commit:

```bash
git commit -m "Update Bank System - Add user permissions"
```

Then push:

```bash
git push
```

---

# Development History

The project follows an incremental development approach.

```text
Basic Client Management
        │
        ▼
File-Based Data Storage
        │
        ▼
Client CRUD Operations
        │
        ▼
Bank Transactions
        │
        ▼
User Management
        │
        ▼
Authentication
        │
        ▼
Bitwise Permissions
        │
        ▼
Algorithms & Improvements
```

The previous implementation remains available in the `Library` directory while the current implementation remains the main project.

---

# Future Improvements

Possible future improvements include:

* SQL Server database integration
* Secure password hashing
* Transaction history
* Audit logging
* Account statements
* Advanced role management
* Automated testing
* Graphical User Interface
* API integration

---

# Author

**Abdulrahman Aghbash**

GitHub:

```text
https://github.com/ABDRHMA41
```

---

# Learning Source

Developed as part of the learning journey with:

**ProgrammingAdvices**

The project is continuously improved by applying concepts learned throughout programming and algorithms courses.

---

## License

This project is intended primarily for educational and learning purposes.
