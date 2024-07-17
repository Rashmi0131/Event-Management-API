# Event Management System

## Project Description
A robust event management system with user registration, role-based access control, and CRUD operations on events using JWT-based authentication and Entity Framework Core for data access.

## Features

### User Management
- **Register a new user**
- **Login/logout functionality**
- **Role-based access control** (Admin and User roles)

### Event Management
- **Add a new event** (admin only)
- **View all events**
- **Update event details** (admin only)
- **Delete an event** (admin only)
- **Search for events by name, date, or location**

## Entities

### User
- **Id**: int, Primary Key
- **Username**: string, unique
- **PasswordHash**: string
- **Role**: string (Admin or User)

### Event
- **Id**: int, Primary Key
- **Name**: string
- **Date**: DateTime
- **Location**: string
- **Description**: string
- **Organizer**: string

## API Endpoints

### For Users
- **POST /api/users/register**: Register a new user
- **POST /api/users/login**: Login a user
- **POST /api/users/logout**: Logout a user

### For Events
- **GET /api/events**: Retrieve all events
- **GET /api/events/{id}**: Retrieve a single event by ID
- **POST /api/events**: Create a new event (admin only)
- **PUT /api/events/{id}**: Update an existing event by ID (admin only)
- **DELETE /api/events/{id}**: Delete an event by ID (admin only)
- **GET /api/events/search**: Search for events by name, date, or location (using query parameters)

## Data Access Layer
- Use Entity Framework Core for database interactions.
- Implement a repository pattern for data access.

## Validation
- Validate input data for required fields and correct data types.

## Authentication and Authorization
- JWT-based authentication
- Role-based access control

## Testing
- Write unit tests for the controllers and services.

## Documentation
- Provide a README file with instructions on how to set up and run the application.
- Include API documentation (Swagger or any other tool).

## Setup Instructions

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/event-management-system.git
    cd event-management-system
    ```

2. **Set up the database**:
    - Ensure you have SQL Server or another compatible database set up.
    - Update the connection string in `appsettings.json`.

3. **Run database migrations**:
    ```bash
    dotnet ef database update
    ```

4. **Run the application**:
    ```bash
    dotnet run
    ```

5. **Access the application**:
    - The API will be accessible at `http://localhost:5000`.
    - Swagger documentation will be available at `http://localhost:5000/swagger`.

## License
This project is licensed under the MIT License. See the LICENSE file for details.
