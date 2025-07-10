## Simple DB Concepts

### Slide 1: What is a Database?

  * A **database (DB)** is an organized collection of data, generally stored and accessed electronically from a computer system.
  * Databases are designed for efficient storage, retrieval, and management of data.
  * They are more robust and scalable than storing data in simple text files.

### Slide 2: Why Use a Database?

  * **Structured Data:** Enforces a schema, ensuring data consistency.
  * **Concurrency:** Allows multiple users to access and modify data at the same time without conflict.
  * **Scalability:** Can handle very large amounts of data efficiently.
  * **Querying:** Provides powerful languages (like SQL) to search, sort, and filter data.
  * **Durability:** Ensures that once a transaction is committed, it remains in the system even in the case of a power loss.

### Slide 3: Simple Database: Flat Files vs. SQLite

  * **Flat-File Database:** The simplest form, where data is stored in a plain text file (like a CSV).
      * **Pros:** Easy to create and read.
      * **Cons:** Inefficient for searching, no support for concurrency, prone to data corruption.
  * **SQLite:** A lightweight, serverless, self-contained database engine. It's included in Python's standard library.
      * **Pros:** A full-featured SQL database stored in a single file. Great for small to medium-sized applications.
      * **Cons:** Not designed for high-concurrency, write-intensive applications.

### Slide 4: Example: Using Python's `sqlite3` Module

Python's `sqlite3` module allows you to work with an SQLite database.
```py

import sqlite3

# 1. Connect to a database (or create it if it doesn't exist)
conn = sqlite3.connect('example.db')
cursor = conn.cursor()

# 2. Create a table
cursor.execute('''
CREATE TABLE IF NOT EXISTS users (
    id INTEGER PRIMARY KEY,
    name TEXT NOT NULL,
    email TEXT
)
''')

# 3. Insert some data
cursor.execute("INSERT INTO users (name, email) VALUES (?, ?)", ('Alice', 'alice@example.com'))
cursor.execute("INSERT INTO users (name, email) VALUES (?, ?)", ('Bob', 'bob@example.com'))

# 4. Commit the changes and close the connection
conn.commit()
conn.close()
```
*You would then write another script to connect and query this data.*

### Slide 5: Further Reading and Practice

  * **Further Reading:** *Think Python, 2nd Edition*, Chapter 14 discusses databases briefly. The official Python `sqlite3` documentation is an excellent resource.
  * **Practice Exercise:**
      * Run the example code to create an `example.db` file.
      * Write a second Python script that connects to `example.db`, retrieves all the users from the `users` table using a `SELECT` query, and prints them.
      * Example Query: `cursor.execute("SELECT * FROM users")`