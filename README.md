# Cinema-App

- [Description](#description)
- [Features](#features)
- [Project Structure](#project-structure)
- [Technologies](#technologies)
- [How to Run and Test](#how-to-run-and-test)
- [API Endpoints](#api-endpoints)
- [Author](#author)

### Description
Cinema-App is a RESTful web application designed for demonstration purposes.
It provides a simulated cinema ticket reservation system. 
The application follows the principles of the REST architectural style, 
ensuring a stateless communication between clients and the server. 
Users can easily register and log in using their credentials, 
and the application offers role-based authorization for administrators 
and regular users.

### Features
- User registration, login, and role-based authorization
- Exception handling with descriptive messages
- Multiple endpoints with user and admin access

### Project Structure
The project follows a 3-layer architecture:

- Presentation layer (controllers)
- Application layer (services)
- Data access layer (DAO)

The project has the following package structure:

- `controllers`: Contains controllers for handling endpoints
- `dao`: Data access layer responsible for connecting with the database and performing CRUD operations
- `dto`: Data transfer objects for transferring data between layers
- `model`: Stores information about entities and their properties
- `security`: Defines access rights to users based on their roles
- `service`: Contains business logic services

### Technologies

| Technology        | Version |
| ----------------- |---------|
| Java              | 17      |
| Apache Maven      | 3.8.7   |
| Apache Tomcat     | 9.0.78  |
| MySQL             | 8.0.32  |
| Hibernate ORM     | 5.6.14  |
| Spring Framework  | 5.3.20  |
| Spring Security   | 5.6.10  |

### How to Run and Test
To run the Cinema-App project, follow these steps:

- ✅ Download and install JDK 17 for your IDE.
- ✅ Make sure you have Apache Tomcat and MySQL installed on your system.
- ✅ Clone the project repository to your local machine.
- ✅ Configure the database connection parameters in the `resources/db.properties` file.
- ✅ Set up a local Tomcat configuration in your IDE.
- ✅ Run the Tomcat configuration and deploy the application.
- ✅ Access the application using the specified URL.
- ✅ Use the provided credentials to test the application's functionalities.
---------
- Admin credentials:
    - Username: admin@i.ua
    - Password: 1234

- User credentials:
    - Username: user@i.ua
    - Password: 5678
----------
You can also use Postman to send requests to the application's endpoints.

### API Endpoints

Here are the available API endpoints for the Cinema-App:

- **Authentication:**
  - `POST: /register` - Register a new user. (Accessible to all)

- **CinemaHall:**
  - `POST: /cinema-halls` - Add a new cinema hall. (Accessible to ADMIN)
  - `GET: /cinema-halls` - Display all cinema halls. (Accessible to all)

- **Movie:**
  - `POST: /movies` - Add a new movie. (Accessible to ADMIN)
  - `GET: /movies` - Display all movies. (Accessible to all)

- **MovieSession:**
  - `POST: /movie-sessions` - Add a new movie session. (Accessible to ADMIN)
  - `PUT: /movie-sessions/{id}` - Update a movie session with the specified ID. (Accessible to ADMIN)
  - `DELETE: /movie-sessions/{id}` - Delete a movie session by ID. (Accessible to ADMIN)
  - `GET: /movie-sessions/available` - Display all available movie sessions. (Accessible to USER)

- **Order:**
  - `GET: /orders` - Display all orders. (Accessible to all)
  - `POST: /orders/complete` - Complete the current order. (Accessible to USER)

- **ShoppingCart:**
  - `GET: /shopping-carts/by-user` - Display the contents of the current user's shopping cart. (Accessible to USER)
  - `PUT: /shopping-carts/movie-sessions` - Add a movie session to the shopping cart. (Accessible to USER)

- **User:**
  - `GET: /users/by-email` - Find a user by email. (Accessible to ADMIN)

### Author
Artem Grunin
