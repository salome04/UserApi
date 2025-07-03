Build a simple API for managing users with clean validation, mapping, and error handling.

Model:
Define one model class: User

User Class Properties:

Id
Type: Integer

FirstName
Type: String

LastName
Type: String

Email
Type: String

DTO:
Create a request model: CreateUserRequest
This class will be used to accept user creation data from the client.

FluentValidation
Create a validator class for CreateUserRequest.
Apply rules like required fields and valid email format.

Mapster
Use Mapster to map CreateUserRequest to the User model inside your controller.

Middleware
Create a custom middleware that catches all unhandled exceptions.

If an exception occurs, return a JSON response with an error message and status code.

Exception Handling
Throw an exception from the controller when an invalid condition occurs (e.g., empty email).

Controller:
Create a UsersController with endpoints:

POST /api/users
Accepts a CreateUserRequest, validates it, maps it to User, and returns the created user

Register FluentValidation, Mapster, and your middleware in the program.
File upload:
Add an endpoint that allows user to upload a file
Save the uploaded file to a local folder inside the Project.
