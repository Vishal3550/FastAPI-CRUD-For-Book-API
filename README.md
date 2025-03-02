# FastAPI Book API

This is a simple CRUD API built using FastAPI for managing books. The API allows users to create, read, update, and delete book records.

## Web View
![FastAPI_Dashboard](https://github.com/Vishal3550/FastAPI-CRUD-For-Book-API/blob/main/FastAPI_View.png)

## Features

- **Create a Book** (`POST /book`)
- **Read a Book** (`GET /{id}`)
- **Update a Book** (`PUT /book/{id}`)
- **Delete a Book** (`DELETE /book/{id}`)

## Requirements

- Python 3.7+
- FastAPI
- Uvicorn

## Installation

1. Clone the repository:
   ```bash
   git clone <repository_url>
   cd <repository_name>
   ```

2. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On macOS/Linux
   venv\Scripts\activate  # On Windows
   ```

3. Install dependencies:
   ```bash
   pip install fastapi uvicorn
   ```

## Running the Application

Start the FastAPI server using Uvicorn:
```bash
uvicorn test:app --reload
```
- The API will be available at `http://127.0.0.1:8000`.
- The interactive Swagger UI can be accessed at `http://127.0.0.1:8000/docs`.

## API Endpoints

### 1. Create a Book
- **Endpoint:** `POST /book`
- **Request Body:**
  ```json
  {
    "title": "Book Title",
    "author": "Author Name",
    "publisher": "Publisher Name"
  }
  ```
- **Response:** Returns the updated book list.

### 2. Read a Book
- **Endpoint:** `GET /{id}`
- **Response:** Returns the book at the given ID.

### 3. Update a Book
- **Endpoint:** `PUT /book/{id}`
- **Request Body:** (Same as Create)
- **Response:** Returns the updated book details.

### 4. Delete a Book
- **Endpoint:** `DELETE /book/{id}`
- **Response:** Returns the updated book list.

## Notes
- The API stores book data in memory (list), meaning data will be lost when the server restarts.
- Error handling is minimal; it may raise errors for invalid IDs.

## Future Enhancements
- Implement database support (e.g., SQLite, PostgreSQL).
- Add authentication and authorization.
- Improve error handling.

