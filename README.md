# 📚 Library Management System

A simple, beginner-friendly console-based Library Management System written in pure Python. No external libraries or dependencies are required.

## Features

- **Add a Book** — Register a new book with title, author, and number of copies.
- **View All Books** — Display a table of all books with their available copies.
- **Search for a Book** — Search by title or author (case-insensitive, partial match).
- **Issue a Book** — Lend a book to a borrower, tracked by name.
- **Return a Book** — Mark a previously issued book as returned.
- **Delete a Book** — Remove a book from the system (only if no copies are currently issued).

## Requirements

- Python 3.x (no external packages needed)

## How to Run

1. Save the script as `library_management.py`.
2. Open a terminal in the folder containing the file.
3. Run:

   ```bash
   python library_management.py
   ```

4. Follow the on-screen menu to interact with the system.

## Menu Overview

```
========================================
     LIBRARY MANAGEMENT SYSTEM
========================================
1. Add a Book
2. View All Books
3. Search for a Book
4. Issue a Book
5. Return a Book
6. Delete a Book
0. Exit
========================================
```

## How It Works

- Each book is stored in memory as a dictionary with the following fields:
  - `id` — a unique, auto-incrementing identifier
  - `title` — the book's title
  - `author` — the book's author
  - `copies` — total number of copies owned
  - `issued_to` — a list of borrower names currently holding a copy
- **Availability** is calculated as `copies - len(issued_to)`.
- A book can only be **deleted** if it has no copies currently issued.
- A borrower cannot issue the same book twice without returning it first.

## Data Persistence

⚠️ This version stores all data **in memory only**. Once the program exits, all book records are lost. There is no file, database, or external storage involved.

### Possible Future Enhancements

- Save/load book data to a file (e.g., JSON or CSV) so records persist between sessions.
- Add due dates and overdue tracking for issued books.
- Support editing existing book details.
- Add a simple GUI or web interface.

## Project Structure

```
library_management.py   # Main application file (all logic in one script)
README.md                # Project documentation
```

## License

This project is free to use, modify, and distribute for learning purposes.
