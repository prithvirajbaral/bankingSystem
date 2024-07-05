# Banking System

This is a simple banking system project implemented in Java. It allows users to register, login, open bank accounts, and perform various banking operations such as credit, debit, transfer money, and check balance.

## Features

- User registration and login
- Open new bank accounts
- Debit money from accounts
- Credit money to accounts
- Transfer money between accounts
- Check account balance

## Requirements

- Java 8 or higher
- MySQL Database
- IntelliJ IDEA or any other Java IDE

## Database Setup

1. Install MySQL and create a database named `banking_system`.
2. Create the necessary tables using the following SQL statements:

   ```sql
   CREATE TABLE accounts (
      account_number BIGINT PRIMARY KEY,
      fullname VARCHAR(255),
      email VARCHAR(255) UNIQUE,
      balance DECIMAL(10, 2),
      security_pin CHAR(4)
   );

   CREATE TABLE users (
      fullname VARCHAR(255),
      email VARCHAR(255) PRIMARY KEY,
      password VARCHAR(255)
   );



## Configuration

1. Open the `BankingApp.java` file.
2. Update the database connection details:
   ```java
   private static final String url = "jdbc:mysql://localhost:3306/banking_system";
   private static final String username = "root";
   private static final String password = "yourpassword";

Replace yourpassword with your MySQL root password.


## Running the Project

1. Clone this repository to your local machine.
2. Open the project in IntelliJ IDEA or any other Java IDE.
3. Ensure the MySQL server is running.
4. Run the `BankingApp.java` file.

## Project Structure
      ```src
         src
            └── Banking_System
            ├── AccountManager.java
            ├── Accounts.java
            ├── BankingApp.java
            └── User.java





## Usage

1. Register a new user.
2. Login with the registered email and password.
3. Open a new bank account if one doesn't already exist.
4. Perform various banking operations:
   - Debit money
   - Credit money
   - Transfer money
   - Check balance
