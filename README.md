*# 🔐 PASSWORD MANAGER CLI

A simple **Command-Line Password Manager and Password Generator** built with Python.

This project allows users to store and manage account credentials, as well as generate random password suggestions directly from the terminal.

## ✨ Features

* 🔐 Store account credentials
* 🔑 Generate random passwords
* 💡 Generate multiple password suggestions
* 👤 Change usernames
* 🔄 Change passwords
* 👀 Show stored credentials
* 🗑️ Delete accounts
* 🖥️ Interactive command-line interface
* ✨ Smooth text output effect

## 🛠️ Technologies Used

* **Python 3**
* `random`
* `time`
* `sys`

## 📂 Project Structure

```text
PASSWORD-MANAGER-CLI/
│
├── main.py
└── README.md
```

## 🚀 How to Run

### 1. Install Python

Make sure Python 3 is installed on your system.

Check your Python version:

```bash
python --version
```

### 2. Run the Program

Open the project folder in your terminal and run:

```bash
python main.py
```

## 📋 Available Options

When the program starts, you will see:

```text
1. Store password
2. Change password
3. Change username
4. Show password
5. Suggest Password
6. Delete account
7. Exit
```

### 🔐 1. Store Password

Stores an account name, username, and password.

```text
Enter account name: github
Enter username: myusername
Enter password: mypassword

Credentials for github stored.
```

### 🔄 2. Change Password

Changes the password for an existing account.

```text
Enter account name: github
Enter new password: newpassword

Password for github changed.
```

### 👤 3. Change Username

Changes the username for an existing account.

```text
Enter account name: github
Enter new username: newusername

Username for github changed to newusername.
```

### 👀 4. Show Password

Displays the stored account credentials.

```text
Account: github
Username: myusername
Password: mypassword
```

### 💡 5. Suggest Password

Generates **3 random password suggestions**.

Each password contains a combination of:

* Uppercase letters
* Lowercase letters
* Numbers
* Special characters

The default password length is **12 characters**.

Example:

```text
Password Suggestions:

G7@kLm2#xP9!
qR8$zT4&nK2@
M5!vLp9#Qa7$
```

### 🗑️ 6. Delete Account

Deletes an account from the password dictionary.

```text
Enter account name to delete: github

Account github deleted.
```

### 🚪 7. Exit

Closes the application.

```text
Exiting...
```

## 🔑 Password Generation

The project uses different character sets:

```python
numbers_string
lowercase_string
uppercase_string
special_symbols_string
```

These character sets are converted into lists and combined:

```python
all_chars = numbers_list + lowercase_list + uppercase_list + special_symbols_list
```

The password is generated using:

```python
password = ''.join(random.choice(all_chars) for _ in range(length))
```

By default:

```python
length = 12
```

## 🗃️ Credential Storage

Account information is stored in a Python dictionary:

```python
passwords = {
    "facebook": {
        "user_name": "name",
        "user_password": "password"
    },
    "gmail": {
        "user_name": "another_name",
        "user_password": "another_password"
    }
}
```

The data is stored **in memory only**.

Therefore, any changes made during execution will be lost when the program is closed.

## ✨ Smooth Terminal Output

The project includes a `smooth_flow()` function that prints text character by character.

```python
def smooth_flow(text, delay=0.05):
    for char in text:
        sys.stdout.write(char)
        sys.stdout.flush()
        time.sleep(delay)
    print()
```

This creates a simple typing-animation effect in the terminal.

## 📚 Python Concepts Used

This project demonstrates:

* Functions
* Dictionaries
* Lists
* Strings
* Loops
* Conditional statements
* Exception handling
* User input
* `random.choice()`
* String manipulation
* CRUD operations
* Python modules
* Command-line applications

## ⚠️ Security Notice

This is a **learning project** and should not be used as a production password manager.

The current version:

* Stores passwords in plain text
* Does not encrypt credentials
* Does not use a master password
* Stores data only while the program is running
* Uses `random.choice()` for password generation

For a real password-management application, secure encryption, authentication, persistent storage, and Python's `secrets` module should be considered.

## 🚀 Future Improvements

Possible improvements include:

* 🔒 Password encryption
* 🔑 Master password authentication
* 💾 SQLite database
* 🙈 Hidden password input
* 🎲 `secrets`-based password generation
* 📊 Password strength checker
* 🔍 Account search
* 📋 Copy password functionality
* 🖥️ GUI version

## 👨‍💻 Author

**Kunal Kumar**

A Python learning project focused on command-line applications, password generation, and basic credential management.

---

⭐ **If you found this project useful, consider giving the repository a star!**
**
