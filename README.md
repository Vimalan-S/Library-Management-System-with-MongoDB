# Library-Management-System-with-MongoDB

# Overview
This project demonstrates a basic CRUD (Create, Read, Update, Delete) application using MongoDB as the database. The application is built using Node.js with the Express framework for the backend, Handlebars for the templating engine, and MongoDB as the database.

# Technologies Used
Node.js: A JavaScript runtime that allows executing JavaScript code on the server side.
Express.js: A web application framework for Node.js that simplifies the creation of web applications.
Handlebars (hbs): A templating engine for Express.js that allows creating dynamic HTML templates.
MongoDB: A NoSQL database used to store and retrieve data for the application.
Project Structure
app.js
The main entry point of the application.
Sets up the Express application, configures Handlebars as the view engine, and defines routes for handling CRUD operations.
Uses the dbo module to interact with the MongoDB database.
db.js
A module responsible for connecting to the MongoDB database.
Uses the mongodb and MongoClient to establish a connection to the local MongoDB server.
Exports the getDatabase function to retrieve the MongoDB database instance and ObjectID for creating ObjectId instances.
views/main.hbs
The main Handlebars template for rendering the HTML views.
Displays a form for creating or editing books, a list of books, and messages for successful operations.
Uses conditional statements to determine whether to display the create or edit form.


# Control Flow
Server Startup (app.js):

Express server is started on port 8000.
Database Connection (db.js):

The getDatabase function is called to connect to the MongoDB database named 'library'.
If the connection is successful, the database instance is returned.
Route Handling (app.js):

GET /:
Retrieves all books from the 'books' collection in MongoDB.
Renders the main Handlebars template with the retrieved books, edit information, and messages.
POST /store_book:
Inserts a new book into the 'books' collection based on the form data.
Redirects to the home page with a status indicating a successful insertion.
POST /update_book/:edit_id:
Updates an existing book in the 'books' collection based on the form data and the provided edit_id.
Redirects to the home page with a status indicating a successful update.

# Handlebars Templates (views/main.hbs):

Renders the main HTML page with conditional logic to display either the create or edit form.
Lists all books with options to edit or delete each book.
