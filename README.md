# Book Library Management App

## Overview
A Flask web application for managing a personal book library with full CRUD operations. Built with Flask-SQLAlchemy using SQLite database, it allows users to add books, view the collection, edit ratings, and delete entries. Features responsive templates and clean database management.

## Features
- View all books ordered by title on home page (`/`)
- Add new books with title, author, and rating (`/add`)
- Edit book ratings (`/edit?id=<book_id>`)
- Delete books (`/delete?id=<book_id>`)
- SQLite database (`books.db`) auto-created with proper schema
- ORM-based CRUD operations with SQLAlchemy

## Tech Stack
- **Backend**: Flask, Flask-SQLAlchemy (ORM)
- **Database**: SQLite (`books.db`)
- **Models**: SQLAlchemy `Book` model with id, title, author, rating
- **Templates**: Jinja2 (index.html, add.html, editrating.html)
- **SQL**: DeclarativeBase, mapped_column for modern SQLAlchemy

## Quick Setup
1. Install dependencies:
2. Run the app:
3. Open `http://localhost:5000`
4. Database `books.db` created automatically[attached_file:14]

## Routes
| Route | Description | Method |
|-------|-------------|--------|
| `/` | View all books | GET |
| `/add` | Add new book form | GET/POST |
| `/edit?id=<id>` | Edit book rating | GET/POST |
| `/delete?id=<id>` | Delete book | GET |

## Database Schema
Book Table:

id (Integer, Primary Key)

title (String 250, Unique, Not Null)

author (String 250, Not Null)

rating (Float, Not Null)


## File Structure
project/
├── main.py # Flask app, models, routes, CRUD operations
├── books.db # SQLite database (auto-created)
├── templates/
│ ├── index.html
│ ├── add.html
│ └── editrating.html
└── README.md # This file
