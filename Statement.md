# 📚 Project Statement: Library Management System

## Overview
This project implements a **Library Management System** in Python, designed to manage books and members efficiently. It provides functionality to add, remove, borrow, and return books, while keeping track of library members and their borrowed items.  

Additionally, the system can **fetch book data from a given URL** (in JSON format), ensuring flexibility in loading external datasets.

---

## Key Features
- 🔗 **Book Data Fetching**  
  - Retrieves book data from a specified URL (JSON format).  
  - Handles potential HTTP request errors and JSON parsing issues gracefully.  

- 📖 **Book Management**  
  - Add and remove books by ISBN.  
  - Track availability (borrowed vs. available).  
  - Prevent duplicate ISBN entries.  

- 👥 **Member Management**  
  - Add and remove members by unique ID.  
  - Track borrowed books per member.  
  - Prevent duplicate member IDs.  

- 📑 **Borrowing & Returning**  
  - Members can borrow available books.  
  - Borrowed books are tracked until returned.  
  - Error handling for invalid operations (e.g., borrowing unavailable books).  

- 🗂️ **Listing Functions**  
  - List all books, available books, and borrowed books.  
  - List all members with their borrowed books.  

- 🖥️ **Interactive Menu**  
  - Console-based menu for user interaction.  
  - Options to manage books, members, and borrowing seamlessly.  

---

## Error Handling
- ✅ **HTTP Errors**: Detects and reports issues like 404 or 500 when fetching book data.  
- ✅ **JSON Errors**: Reports invalid JSON format gracefully.  
- ✅ **Library Operations**: Prevents duplicate entries and invalid borrow/return actions.  

---

## Execution
Run the program directly in a Python environment:

```bash
python library_system.py
