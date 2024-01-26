# Bookstore API

### BlueKyte AI Assignment 2 (RESTful API Development)

This is a RESTful API for an online bookstore. The API is built using Express.js for the backend, MongoDB for the database, and includes a simple front-end application using HTML, CSS, and JavaScript. The API supports various operations to manage the book inventory.

## Table of Contents

- Features
- Project Structure
- Installation
- Usage
- Front-end Application
- API Documentation
- Environment Variables
- Contributing
- License

## Features


1. Book Management:

- Authenticated users can add new book listings with details such as title, author, price, etc.
- CRUD operations for managing book listings (Create, Read, Update, Delete).

2. Error Handling:

- Centralized error handling middleware to handle 404 and 500 errors.

3. Health Check Endpoint:

  - `/health` endpoint to check the status of the server and the database.

## Project Structure

  - `index.js`: Main entry point for the application.

  - `routes/`: Contains route definitions.

    - `bookRoute.js`: Defines routes for book-related operations.

  - `controllers/`: Contains controller functions for handling requests.

    - `books.js`: Controller functions for book-related operations.

  - `models/`: Defines Mongoose schemas for BookListing.

  - `config/`: Contains configuration files.

  - `README.md`: Documentation file.

## Installation

1. Clone the repository:

  - `git clone https://github.com/lavanyamishra/BookStore-backend.git`

2. Navigate to the project directory:

  - `cd Book-Store-Project`
  -  `cd Backend`

3. Install dependencies:

  - `npm install`

4. Create a .env file in the root directory and set your environment variables. You can use the provided .env.example as a template.

## Usage

1. Start the server:

  - `npm run dev`

2. The server will be running at `http://localhost:your-port`.

3. Use API endpoints to manage book listings.

## Front-end Application

- The front-end application is a simple HTML-based interface to interact with the API. Open the (https://book-store-frontend-tau.vercel.app/) file in a web browser to access the application.

- The front-end application github repository link is ((https://github.com/lavanyamishra/BookStore-Frontend))

## API Documentation

### Retrieve Books

  - `GET /books`: Get a list of all books.

### Add a New Book

- `POST /books`: Add a new book.
  - Request Body: `{ "title": "Book Title", "author": "Author Name", "publishYear": 2022, "otherDetails": "Additional Information" }`

### Update Book Details

- PUT /books/:id: Update details of a specific book.

- Request Body: `{ "title": "Updated Title", "author": "Updated Author", "publishYear": 2023, "otherDetails": "Updated Information" }`

### Delete a Book

  - `DELETE /books/:id`: Delete a specific book.

### Health Check

- GET /health: Check the status of the server and the database.

## Environment Variables

- `PORT`: Port on which the server will run.
- `mongoDBURL`: MongoDB connection string.

## Contributing

If you would like to contribute to this project, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License.
