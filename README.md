Bank System (C++ Console Application)

An advanced console-based Bank Management System developed in C++.

This project evolved from a basic client management application into a more complete banking administration system. It includes client management, banking transactions, user management, authentication, and Bitwise-based permission control.

The project was continuously improved throughout the ProgrammingAdvices courses, with new algorithms, data structures, validation, and system-management features added over time.

⸻

Key Features

1. Client Management

* Show Client List: Display all registered clients in a formatted table.
* Add New Client: Add new clients with validation against duplicate Account Numbers.
* Update Client: Modify existing client information.
* Delete Client: Delete clients using the Mark for Delete pattern.
* Find Client: Search for a client using the Account Number.
* Client Data Validation: Validate account information before saving changes.

⸻

2. User Management & Permissions

The system includes a complete user-management and authentication system.

* Login System: Users must authenticate using a Username and Password.
* User CRUD Operations: Show, Add, Update, Delete, and Find users.
* Permission System: Control access to system operations using Bitwise permissions.
* Granular Permissions: Permissions can be combined to provide different levels of access.
* Admin Protection: The Admin superuser is protected from deletion or loss of full privileges.

Bitwise Permission System

Permissions are represented using integer flags and combined using bitwise operations.

For example:

Read        = 1
Add         = 2
Delete      = 4
Update      = 8
Transactions = 16
ManageUsers = 32

Multiple permissions can be combined into a single value:

Permissions = Read | Add | Update

The special value:

-1

grants full system access to the administrator.

⸻

3. Banking Transactions

The system provides basic banking transaction functionality.

* Deposit: Add money to a client’s account.
* Withdraw: Withdraw money after validating the available balance.
* Balance Validation: Prevent withdrawals that exceed the account balance.
* Total Balances: Calculate and display the total balance of all client accounts.
* Transaction Permissions: Access to transaction operations is controlled by user permissions.

⸻

4. Authentication & Access Control

The application follows an authentication-first workflow:

Username + Password
        │
        ▼
Authentication
        │
        ▼
Permission Validation
        │
        ▼
Main Menu
        │
        ├── Client Management
        ├── Transactions
        ├── User Management
        └── Logout

Users can only access operations allowed by their assigned permissions.

⸻

Algorithms & Programming Concepts

The project applies concepts learned throughout the ProgrammingAdvices courses, including:

* Object-oriented programming
* Functions and modular programming
* Structures and enumerations
* File handling
* Vectors and dynamic data
* Searching and filtering
* Data validation
* Record serialization and parsing
* CRUD operations
* Algorithmic problem solving
* Bitwise operations
* Permission flags
* Authentication and access control
* Data persistence

The project was also updated as part of Course 8 – Algorithms Level 4, where additional algorithmic concepts and improvements were applied to the existing Bank System.

⸻

Architecture & Data Handling

The application is organized into separate components responsible for different system operations.

Main Program
│
├── Login & Authentication
│
├── Client Management
│   ├── Show Clients
│   ├── Add Client
│   ├── Update Client
│   ├── Delete Client
│   └── Find Client
│
├── Transactions
│   ├── Deposit
│   ├── Withdraw
│   └── Total Balances
│
├── User Management
│   ├── Show Users
│   ├── Add User
│   ├── Update User
│   ├── Delete User
│   └── Find User
│
└── Permission System
    └── Bitwise Access Control

Data Persistence

The application stores data locally in text files and loads it into memory when required.

Data is separated using the custom delimiter:

#//#

The project uses std::vector for in-memory data management and rewrites the corresponding files when records are modified.

⸻

Data Storage

Clients.txt

Client records follow this format:

AccountNumber#//#PINCode#//#Name#//#Phone#//#AccountBalance

Example:

A1001#//#1234#//#Abdulrahman#//#0999999999#//#1500

Users.txt

User records follow this format:

Username#//#Password#//#Permissions

Example:

Admin#//#1234#//#-1

Where:

-1 = Full Permissions

⸻

Main Menu

After successful authentication, authorized users can access:

===========================
        MAIN MENU
===========================
[1] Client Management
[2] Transactions
[3] Manage Users
[4] Logout

The available operations depend on the permissions assigned to the logged-in user.

⸻

Project Evolution

Initial Version

The original project focused mainly on:

* Client management
* Adding clients
* Updating clients
* Deleting clients
* Searching for clients
* Reading and writing client data

Updated Version

The system was expanded with:

* User authentication
* User management
* Bitwise permissions
* Role-based access concepts
* Banking transactions
* Deposit and withdrawal
* Total balance calculation
* Permission-based menu access
* Administrator protection
* Additional algorithms and improvements

This transformation turned the project from a basic client-management application into a more complete Bank Management System.

⸻

Technologies

* C++
* Standard C++ Library
* File I/O
* std::vector
* Bitwise Operations
* Object-Oriented Programming
* Algorithms & Problem Solving

⸻

Learning Objectives

This project was developed as a practical application of programming and algorithmic concepts learned through the ProgrammingAdvices courses.

It focuses on transforming theoretical programming concepts into a real-world style application involving:

* Data management
* Authentication
* Authorization
* Algorithms
* File persistence
* Business logic
* Modular programming
* Problem solving

⸻

Future Improvements

Possible future improvements include:

* Database integration using SQL Server
* Password hashing and stronger authentication
* More advanced roles and permissions
* Transaction history
* Audit logs
* Account statements
* API integration
* Graphical User Interface
* Automated testing

⸻

Author

Abdulrahman Aghbash

GitHub: ABDRHMA41

⸻

Course

ProgrammingAdvices

Project developed and continuously improved while progressing through the programming and algorithms courses.

⸻

License

This project is intended for educational and learning purposes.
