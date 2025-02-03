# Password Manager

Password Manager is an application for managing passwords, written in Java using Swing for the user interface and SQLite as the database.

## Features

- Adding new passwords
- Generating random passwords
- Storing information about applications, logins, passwords, emails, and URLs
- Automatically creating database tables if they do not exist
- Supporting multiple users with relationships between tables
- Registering new users
- Encrypting and decrypting data
- User login and authentication
- Viewing and sorting stored passwords
- Menu navigation

## Project Structure

- `AddPasswordFrame.java`: Class responsible for the user interface for adding new passwords.
- `App.java`: Main application class.
- `CipherMachine.java`: Class responsible for encrypting and decrypting data using the AES algorithm.
- `DataManager.java`: Base class for `PasswordDataManager` and `UsersDataManager`, containing methods for opening and closing database connections.
- `LoginPageFrame.java`: Class responsible for the user interface for user login.
- `Main.java`: Entry point of the application.
- `MenuFrame.java`: Class responsible for the main menu interface.
- `PasswordDataManager.java`: Class responsible for managing password data in the database.
- `PasswordDataRow.java`: Class representing a row of password data.
- `PasswordHashing.java`: Class responsible for hashing user passwords.
- `PasswordsTableFrame.java`: Class responsible for displaying stored passwords in a table format.
- `RegistrationFrame.java`: Class responsible for the user interface for registering new users.
- `SortPasswordFrame.java`: Class responsible for the user interface for sorting passwords.
- `testClass.java`: Class for testing purposes.
- `UserDataRow.java`: Class representing a row of user data.
- `UsersDataManager.java`: Class responsible for managing user data in the database.

## Requirements

- Java 8 or newer
- SQLite

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/artur-penar/PasswordManager
   ```
2. Navigate to the project directory:
   ```sh
   cd PasswordManager
   ```

## Running the Application

1. Compile the project:
   ```sh
   javac -cp ".;sqlite-jdbc-<version>.jar" *.java
   ```
2. Run the application:
   ```sh
   java -cp ".;sqlite-jdbc-<version>.jar" RegistrationFrame
   ```

## Usage

1. Run the application.

2. Register a new user by entering a login and password, then clicking the "Register" button.
![alt text](/images/register.png)

3. After registration, log in and add new passwords by entering application data, login, password, email, and URL.
![alt text](/images/add-password.png)

4. You can also generate a random password by clicking the "Generate" button.

5. Encrypt and decrypt data using the `CipherMachine` class.

6. Search passwords in stored data.

    ![alt text](/images/show-passwords.png)


