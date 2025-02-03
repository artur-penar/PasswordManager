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

## Project Structure

- `AddPasswordFrame.java`: Class responsible for the user interface for adding new passwords.
- `PasswordDataManager.java`: Class responsible for managing password data in the database.
- `DataManager.java`: Base class for `PasswordDataManager` and `UsersDataManager`, containing methods for opening and closing database connections.
- `RegistrationFrame.java`: Class responsible for the user interface for registering new users.
- `UsersDataManager.java`: Class responsible for managing user data in the database.
- `PasswordHashing.java`: Class responsible for hashing user passwords.
- `CipherMachine.java`: Class responsible for encrypting and decrypting data using the AES algorithm.

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
3. After registration, log in and add new passwords by entering application data, login, password, email, and URL.
4. You can also generate a random password by clicking the "Generate" button.
5. Encrypt and decrypt data using the `CipherMachine` class.

## Example Usage of `CipherMachine` Class

```java
public class Main {
    public static void main(String[] args) throws Exception {
        CipherMachine cipherMachine = new CipherMachine();
        
        String originalData = "SensitiveData";
        String encryptedData = cipherMachine.encrypt(originalData);
        String key = cipherMachine.getKey();
        String iv = cipherMachine.getIv();
        
        System.out.println("Original Data: " + originalData);
        System.out.println("Encrypted Data: " + encryptedData);
        System.out.println("Key: " + key);
        System.out.println("IV: " + iv);
        
        String decryptedData = cipherMachine.decrypt(encryptedData, key, iv);
        System.out.println("Decrypted Data: " + decryptedData);
    }
}
```

## Author

- Artur Penar

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
```
