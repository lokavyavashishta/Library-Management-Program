# 📚 Library Management System

A simple **Library Management System built using Python and Object-Oriented Programming (OOP)**. This project is designed as a beginner-friendly college project for understanding how classes, objects, functions, dictionaries, lists, and user input can be combined to create a working application.

---

## 👨‍💻 Project Information

**Project Name:** Library Management System
**Language:** Python
**Level:** 1st Semester College Project
**Programming Concepts:** Object-Oriented Programming (OOP), Functions, Lists, Dictionaries, Exception Handling
**Author:** Lokavya Vashishtha

---

## 📌 About the Project

The Library Management System is a **command-line based application** that allows a librarian to manage books and library members.

The system provides basic functionality such as:

* Adding books
* Adding library members
* Borrowing books
* Returning books
* Viewing all books
* Viewing available books
* Viewing borrowed books
* Viewing registered members
* Removing books
* Removing members

The project uses **Object-Oriented Programming** to represent books, members, and the library as separate objects.

---

## 🎯 Objectives

The main objectives of this project are:

1. To understand the fundamentals of Python programming.
2. To learn and implement **Object-Oriented Programming**.
3. To understand how classes and objects work.
4. To practice using Python lists and dictionaries.
5. To implement functions and conditional statements.
6. To handle basic errors using exception handling.
7. To create a functional command-line application.
8. To develop a project suitable for uploading and demonstrating on GitHub.

---

## 🛠️ Technologies Used

| Technology   | Purpose                             |
| ------------ | ----------------------------------- |
| **Python**   | Main programming language           |
| **Requests** | Fetching book data from a URL       |
| **JSON**     | Processing JSON-formatted data      |
| **GitHub**   | Project hosting and version control |

---

## 🧠 Python Concepts Used

This project demonstrates several important Python concepts:

### 1. Classes and Objects

The project contains three main classes:

* `Book`
* `Member`
* `Library`

For example:

```python
class Book:
    def __init__(self, title, author, isbn):
        self.title = title
        self.author = author
        self.isbn = isbn
        self.is_borrowed = False
```

Each book is represented as an object containing its title, author, ISBN, and borrowing status.

---

### 2. Encapsulation

The data and functions related to books, members, and the library are organized inside their respective classes.

For example, the `Library` class contains functions such as:

```python
add_book()
remove_book()
borrow_book()
return_book()
```

---

### 3. Lists

Lists are used to store the books borrowed by a member.

```python
self.borrowed_books = []
```

---

### 4. Dictionaries

Dictionaries are used to store books and members efficiently.

```python
self.books = {}
self.members = {}
```

Books are stored using their ISBN as the key, while members are stored using their member ID.

---

### 5. Conditional Statements

The program uses `if`, `elif`, and `else` to handle different situations.

For example, when borrowing a book, the program checks whether:

* The member exists.
* The book exists.
* The book is already borrowed.

---

### 6. Exception Handling

The program uses `try` and `except` when fetching book information from a URL.

```python
try:
    response = requests.get(url)
    response.raise_for_status()
    books_data = response.json()
except requests.exceptions.RequestException as e:
    print(f"Error fetching data from {url}: {e}")
```

This prevents the program from crashing when a network or request-related error occurs.

---

## 🏗️ Project Structure

The main components of the project are:

```text
Library Management System
│
├── Book
│   ├── Title
│   ├── Author
│   ├── ISBN
│   └── Borrowing Status
│
├── Member
│   ├── Name
│   ├── Member ID
│   └── Borrowed Books
│
└── Library
    ├── Books
    ├── Members
    ├── Add/Remove Books
    ├── Add/Remove Members
    ├── Borrow Books
    ├── Return Books
    └── Display Information
```

---

## ⚙️ Features

### 📖 1. Add Book

The user can add a new book by entering:

* Book title
* Author name
* ISBN

The system checks whether the ISBN already exists before adding the book.

---

### 👤 2. Add Member

A new library member can be registered using:

* Member name
* Member ID

The program prevents duplicate member IDs.

---

### 📕 3. Borrow Book

A registered member can borrow an available book by providing:

* Member ID
* Book ISBN

The system checks whether the member and book exist and whether the book is already borrowed.

---

### 📗 4. Return Book

A member can return a borrowed book using the member ID and ISBN.

The system verifies that the book was actually borrowed by that member.

---

### 📚 5. List All Books

Displays every book registered in the library along with its current status.

Example:

```text
'Python Programming' by John Smith (ISBN: 12345) (Available)
```

---

### 🟢 6. List Available Books

Displays only books that are currently available for borrowing.

---

### 🔴 7. List Borrowed Books

Displays books that are currently borrowed.

---

### 👥 8. List All Members

Displays all registered members and the number of books they have borrowed.

---

### 🗑️ 9. Remove Book

A book can be removed from the library using its ISBN.

---

### ❌ 10. Remove Member

A member can be removed using their member ID.

---

## 🖥️ How the Program Works

When the program starts, it asks the user to enter the name of the library.

```text
Enter the name of the library:
```

After that, the main menu is displayed:

```text
--- Library Menu ---
1. Add Book
2. Add Member
3. Borrow Book
4. Return Book
5. List All Books
6. List Available Books
7. List Borrowed Books
8. List All Members
9. Remove Book
10. Remove Member
11. Exit
```

The user selects an option by entering its number.

For example:

```text
Enter your choice: 1
Enter book title: Python Basics
Enter book author: John Smith
Enter book ISBN: 1001

Added book: Python Basics
```

---

## 🚀 Installation and Setup

### Step 1: Install Python

Download and install Python from the official Python website.

Make sure Python is added to your system PATH during installation.

Check the installation using:

```bash
python --version
```

---

### Step 2: Clone the Repository

Clone the project from GitHub:

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Move into the project directory:

```bash
cd Library-Management-System
```

---

### Step 3: Install Required Library

The project uses the `requests` package.

Install it using:

```bash
pip install requests
```

---

### Step 4: Run the Program

Run the Python file:

```bash
python library_management.py
```

The interactive library menu will then appear in the terminal.

---

## 📋 Example Workflow

A typical workflow could look like this:

```text
1. Add Book
   ↓
2. Add Member
   ↓
3. Borrow Book
   ↓
4. List Borrowed Books
   ↓
5. Return Book
   ↓
6. List Available Books
```

This demonstrates how the different components of the system interact with each other.

---

## 🔐 Error Handling

The program includes basic error handling to prevent invalid operations.

Examples include:

* Trying to add a book with an existing ISBN.
* Trying to add a member with an existing ID.
* Trying to borrow a book that does not exist.
* Trying to borrow an already borrowed book.
* Trying to return a book that was not borrowed.
* Entering a member ID that does not exist.
* Entering an ISBN that does not exist.
* Network errors while fetching JSON data.

Example:

```text
Error: Book with ISBN 1001 already exists.
```

---

## 🌐 Book Data Fetching

The project also contains a function called:

```python
load_books_from_url(url)
```

This function is designed to retrieve book data from a URL that provides JSON data.

It uses the `requests` library:

```python
response = requests.get(url)
```

The JSON response is then converted into Python data using:

```python
books_data = response.json()
```

### Note

The current interactive menu does **not automatically import the fetched books into the library**. The URL-loading function is currently a separate utility that can be integrated into the system in a future version.

---

## 📂 Suggested GitHub Repository Structure

A clean GitHub repository can be organized like this:

```text
Library-Management-System/
│
├── library_management.py
├── README.md
├── requirements.txt
└── LICENSE
```

### `requirements.txt`

You can create a `requirements.txt` file containing:

```text
requests
```

This allows other users to install the required dependency easily:

```bash
pip install -r requirements.txt
```

---

## 🔮 Future Improvements

This project can be expanded significantly as programming skills improve.

Possible future features include:

* 💾 Save books and members permanently using files.
* 🗄️ Add a database such as SQLite or MySQL.
* 🔐 Add librarian login and authentication.
* 📅 Add book return deadlines.
* 💰 Add late-return fines.
* 🔍 Add book search functionality.
* 📊 Add library statistics.
* 🌐 Create a web-based interface.
* 🖥️ Create a graphical user interface using Tkinter.
* 📱 Develop a more advanced application interface.
* 🌐 Automatically import books from an online API.
* 📝 Add transaction history for borrowed and returned books.

---

## 📚 What I Learned

Through this project, I learned and practiced:

* Python fundamentals
* Object-Oriented Programming
* Classes and objects
* Constructors
* Functions and methods
* Lists
* Dictionaries
* Conditional statements
* Loops
* Exception handling
* User input
* Basic API/JSON handling
* Organizing a Python project
* Using GitHub for project documentation

---

## 🎓 Academic Purpose

This project was created as a **1st-semester college programming project** to demonstrate practical understanding of Python fundamentals and Object-Oriented Programming.

It focuses on applying basic programming concepts to solve a real-world problem in a simple and understandable way.

---

## 👨‍💻 Author

**Lokavya Vashishtha**

🎓 1st Semester College Student
💻 Interested in Python, C/C++, Artificial Intelligence & Machine Learning

---

## ⭐ Acknowledgement

This project was developed for educational purposes as part of learning programming and software development fundamentals.

If you find this project useful, consider giving the repository a ⭐ on GitHub.

---

## 📄 License

This project is intended for educational and learning purposes. You may modify and improve the code for your own academic projects and practice.

---

### 🚀 Future Goal

> **Start simple. Learn the fundamentals. Build projects. Improve them step by step.**
