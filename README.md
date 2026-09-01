# Bank System - C++

A simple **Bank Management System** developed using **C++**.

The project is a console-based application that allows users to manage bank clients and their account information using a text file as a simple database.

## Features

The system provides the following operations:

1. **Show Client List**

   * Display all registered clients.
   * Show account number, PIN code, name, phone number, and account balance.

2. **Add New Client**

   * Add a new client to the system.
   * Check whether the account number already exists.
   * Store the client information in `Clients.txt`.

3. **Delete Client**

   * Search for a client using the account number.
   * Display the client's information.
   * Ask for confirmation before deletion.

4. **Update Client**

   * Search for a client using the account number.
   * Display the current information.
   * Update the client's PIN, name, phone, and balance.

5. **Find Client**

   * Search for a specific client by account number.
   * Display the complete client information.

6. **Exit**

   * Close the program.

## Technologies Used

* C++
* Standard Template Library (STL)
* `vector`
* `fstream`
* `string`
* File Handling
* Structures
* Functions
* Enumerations
* Basic CRUD Operations

## Data Storage

Client information is stored in a text file:

```text
Clients.txt
```

Each client is stored as a single line using the following separator:

```text
#//#
```

Example:

```text
A1001#//#1234#//#Abdulrahman#//#0999999999#//#1500.000000
```

The data represents:

```text
Account Number
PIN Code
Name
Phone
Account Balance
```

## Project Structure

```text
Bank-System/
│
├── BankSystem.cpp
├── Clients.txt
└── README.md
```

## Client Structure

The project uses a structure to represent a bank client:

```cpp
struct sClient
{
    string AccountNumber;
    string PinCode;
    string Name;
    string Phone;
    double AccountBalance;
    bool MarkForDelete = false;
};
```

## Main Menu

The application provides the following menu:

```text
===========================================
        Main Menu Screen
===========================================
    [1] Show Client List.
    [2] Add New Client.
    [3] Delete Client.
    [4] Update Client Info.
    [5] Find Client.
    [6] Exit.
===========================================
```

## Program Concepts

This project demonstrates several important C++ programming concepts:

### Structures

Used to group client information into one object.

### Vectors

Used to temporarily store multiple clients in memory.

### File Handling

The project uses `fstream` to read and write client data.

### String Processing

The `SplitString()` function separates client data using a custom delimiter.

### Type Conversion

`stod()` converts the account balance from `string` to `double`.

### CRUD Operations

The project implements:

```text
Create → Add Client
Read   → List / Find Client
Update → Update Client
Delete → Delete Client
```

## How the System Works

The general data flow is:

```text
              Clients.txt
                   │
                   ▼
       Load Clients From File
                   │
                   ▼
             vector<sClient>
                   │
        ┌──────────┼──────────┐
        ▼          ▼          ▼
       Find      Update     Delete
        │          │          │
        └──────────┼──────────┘
                   ▼
          Save Data To File
                   │
                   ▼
              Clients.txt
```

## Learning Objectives

This project was developed to practice:

* C++ functions
* Structures
* Vectors
* File input/output
* String manipulation
* Searching
* Updating records
* Deleting records
* Menu-driven applications
* Basic software organization

## How to Run

### 1. Clone the Repository

```bash
git clone YOUR_REPOSITORY_URL
```

### 2. Open the Project

Open the project using a C++ development environment such as:

* Visual Studio
* Visual Studio Code
* Code::Blocks
* CLion

### 3. Compile

Using g++:

```bash
g++ BankSystem.cpp -o BankSystem
```

### 4. Run

```bash
./BankSystem
```

On Windows:

```bash
BankSystem.exe
```

## Future Improvements

Possible improvements include:

* Password/PIN validation
* Deposit and withdrawal operations
* Transfer money between accounts
* Transaction history
* User authentication
* Better input validation
* Database integration using SQL
* Separation into multiple `.h` and `.cpp` files
* Object-Oriented Programming version
* Graphical User Interface

## Author

**Abdulrahman Agbsh**

C++ Programming Project

## License

This project is created for **educational and learning purposes**.

