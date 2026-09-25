# 🔐 Password Generator

A simple **command-line password generator** built with Python.

This project generates random passwords using uppercase letters, lowercase letters, numbers, and special characters.

## ✨ Features

* 🔐 Generate random passwords
* 🔤 Uppercase and lowercase letters
* 🔢 Numbers
* 🔣 Special characters
* 📏 Custom password length
* 💡 Generate multiple password suggestions
* 🖥️ Simple command-line interface

## 🛠️ Technologies Used

* **Python 3**
* `random`
* `string`

## 📂 Project Structure

```text
password-generator/
│
├── main.py
└── README.md
```

## 🚀 Getting Started

### 1. Install Python

Make sure Python 3 is installed.

Check your Python version:

```bash
python --version
```

### 2. Run the Program

```bash
python main.py
```

## 🔑 How It Works

The generator uses four different character sets:

```python
numbers_string = '12345678910'
lowercase_string = 'abcdefghijklmnopqrstuvwxyz'
uppercase_string = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'
special_symbols_string = "!@#$%^&*()-_+=[]{}|;:',.<>/?`~"
```

These characters are combined into a single list:

```python
all_chars = numbers_list + lowercase_list + uppercase_list + special_symbols_list
```

The program then randomly selects characters to create the password:

```python
password = ''.join(
    random.choice(all_chars)
    for _ in range(length)
)
```

The default password length is **12 characters**.

## 💡 Password Suggestions

The program can generate multiple password suggestions:

```python
suggestions = suggest_passwords()
```

By default, it generates **3 password suggestions**, each with a length of **12 characters**.

Example:

```text
Password Suggestions:
aG7@kP2!xL9#
Q8$mN2@vK7!z
pL4#xR8&nT2@
```

## 📋 Available Options

```text
1. Store password
2. Change password
3. Change username
4. Show password
5. Suggest Password
6. Delete account
7. Exit
```

> This README focuses specifically on the **password generation and suggestion functionality**.

## ⚠️ Security Note

This project is intended for **learning Python and password-generation concepts**.

The current implementation uses Python's `random.choice()`. For passwords that require cryptographically secure randomness, Python's `secrets` module is recommended.

Example:

```python
import secrets
import string

characters = string.ascii_letters + string.digits + string.punctuation

password = ''.join(
    secrets.choice(characters)
    for _ in range(16)
)
```

## 📚 Python Concepts

This project demonstrates:

* Python functions
* Lists
* Strings
* Loops
* `random.choice()`
* List concatenation
* String joining
* Function parameters
* Random password generation

## 👨‍💻 Author

**Kunal Kumar**

A beginner-friendly Python project for learning password generation and Python programming.

---

⭐ If you found this project useful, consider giving the repository a star!
