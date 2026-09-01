# Bank System - C++

A console-based **Bank Management System** developed using **C++**.

The project allows managing bank clients, storing their information in a text file, and performing basic banking transactions such as **Deposit, Withdraw, and Total Balance**.

## Features

### Client Management

The main menu provides the following operations:

* **Show Client List**
* **Add New Client**
* **Delete Client**
* **Update Client Information**
* **Find Client**
* **Transactions**
* **Exit**

### Banking Transactions

The Transactions menu provides:

* **Deposit**
* **Withdraw**
* **Show Total Balances**
* **Return to Main Menu**

The project includes validation when withdrawing money to prevent the withdrawal amount from exceeding the client's current balance.

## Technologies Used

* C++
* Standard Template Library (STL)
* `struct`
* `vector`
* `string`
* `fstream`
* File Handling
* Functions
* `enum`
* `switch`
* Basic CRUD Operations

## Data Storage

Client data is stored in:

```text
Clients.txt
```

The project uses the following separator:

```text
#//#
```

A client record contains:

```text
Account Number
PIN Code
Name
Phone
Account Balance
```

The `sClient` structure represents a client in the program.

## Example Data Format

```text
A1001#//#1234#//#Abdulrahman#//#0999999999#//#1500
```

The program converts records between text lines and `sClient` objects using:

```text
ConvertLinetoRecord()
ConvertRecordToLine()
```

The line-to-record conversion also converts the balance from `string` to `double`.

## Project Architecture

The project follows a simple layered flow:

```text
User
 │
 ▼
Main Menu
 │
 ├── Client Management
 │     ├── List Clients
 │     ├── Add Client
 │     ├── Delete Client
 │     ├── Update Client
 │     └── Find Client
 │
 └── Transactions
       ├── Deposit
       ├── Withdraw
       └── Total Balances
                │
                ▼
          Clients.txt
```

## Client Management

### Add Client

When adding a client, the program asks for:

* Account Number
* PIN Code
* Name
* Phone
* Account Balance

The system also checks whether the account number already exists before accepting the new client.

### Find Client

The system searches for a client using the account number and displays the client's complete information if found.

### Update Client

The system allows updating:

* PIN Code
* Name
* Phone
* Account Balance

The account number remains unchanged.

### Delete Client

The project uses a **Mark for Delete** approach.

Instead of immediately removing an element from the vector, the client is marked:

```cpp
MarkForDelete = true;
```

When the file is saved, marked clients are excluded from the rewritten file.

## Transactions

### Deposit

The user enters an account number and deposit amount.

The amount is added to the client's balance:

```cpp
C.AccountBalance += Amount;
```

The updated data is then saved to the file.

### Withdraw

The user enters an account number and withdrawal amount.

Before processing the transaction, the program checks that:

```text
Withdrawal Amount <= Account Balance
```

The withdrawal is then performed by sending a negative amount to the balance update function.

Conceptually:

```text
Balance = Balance - Withdrawal Amount
```

### Total Balances

The system calculates the total balance of all clients:

```cpp
TotalBalances += Client.AccountBalance;
```

and displays the final total.

## File Handling

The project uses `fstream` to manage the `Clients.txt` file.

### Reading

```cpp
ios::in
```

is used to read existing client records.

### Writing

```cpp
ios::out
```

is used when rewriting the file.

### Appending

```cpp
ios::out | ios::app
```

is used to add a new client at the end of the file.

## Main Menu

```text
===========================================
        Main Menue Screen
===========================================
    [1] Show Client List.
    [2] Add New Client.
    [3] Delete Client.
    [4] Update Client Info.
    [5] Find Client.
    [6] Transactions.
    [7] Exit.
===========================================
```

## Transactions Menu

```text
===========================================
        Transactions Menue Screen
===========================================
    [1] Deposit.
    [2] Withdraw.
    [3] Total Balances.
    [4] Main Menue.
===========================================
```

These menus are implemented using enumerations and `switch` statements.

## Program Flow

The application starts from:

```cpp
int main()
{
    ShowMainMenue();
    system("pause>0");
    return 0;
}
```

The main menu then directs the user to the appropriate operation.

## Core Concepts Demonstrated

This project demonstrates several important C++ programming concepts:

```text
Structures
    ↓
Vectors
    ↓
Functions
    ↓
File Handling
    ↓
String Processing
    ↓
Searching
    ↓
CRUD Operations
    ↓
Transactions
    ↓
Menu-Driven Application
```

## How to Run

### Clone the Repository

```bash
git clone https://github.com/ABDRHMA41/Bank-.git
```

### Enter the Project Directory

```bash
cd Bank-
```

### Compile

Using `g++`:

```bash
g++ BankSystem.cpp -o BankSystem
```

### Run

Windows:

```bash
BankSystem.exe
```

Linux/macOS:

```bash
./BankSystem
```

> Make sure `Clients.txt` is available in the appropriate working directory when running the program.

## Future Improvements

Possible future improvements include:

* Input validation
* Login and authentication system
* Transaction history
* Transfer between accounts
* Better error handling
* SQL database integration
* Object-Oriented Programming version
* Separation into `.h` and `.cpp` files
* Improved user interface
* Transaction reports

## Author

**Abdulrahman Agbsh**

C++ Programming Project

## Purpose

This project was created for **learning and practicing C++ programming**, especially:

* File Handling
* Data Structures
* Functions
* CRUD Operations
* Client Management
* Basic Banking Transactions

## License

This project is intended for **educational purposes**.
