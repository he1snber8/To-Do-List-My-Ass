# To-Do-List-My-Ass

Description

Create a web-based to-do-list application where users can add, edit, and delete daily objectives. The front-end is built with Angular and the back-end is powered by ASP.NET Core Web API.

## Tech Stack

- ASP.NET Core
- Angular

## Requirements

- Design RESTful API endpoints for ToDo operations (Refer to ASP.NET Core Web API docs)
- Implement CRUD operations in both the ASP.NET Core API and Angular front-end
- Manage UI state in Angular using component properties or RxJS
- Validate user input in Angular forms (using ReactiveFormsModule)
- Handle and display errors from HTTP requests (using RxJS catchError)
- Write unit tests for API controllers and Angular components (using xUnit and Jasmine/Karma)
- Follow best practices like dependency injection and logging (Inject ILogger<T> via constructor)

## Installation

### Backend (ASP.NET Core)

1. Clone the repository:
   git clone https://github.com/your-username/To-Do-List-My-Ass.git
2. Navigate to the API directory:
   cd To-Do-List-My-Ass/Api
3. Restore dependencies:
   dotnet restore
4. Build the project:
   dotnet build
5. Configure environment variables in appsettings.json (e.g., connection strings)
6. Run the API:
   dotnet run

### Frontend (Angular)

1. Navigate to the Angular project:
   cd To-Do-List-My-Ass/ClientApp
2. Install dependencies:
   npm install
3. Start the development server:
   ng serve --open

## Usage

- Access the Angular application at http://localhost:4200.
- The API endpoints are available at https://localhost:5001/api/todo.
- Use the UI to add, edit, and delete to-do items. Errors will be displayed inline when operations fail.

## Implementation Steps

1. Initialize an ASP.NET Core Web API project.
2. Define the ToDo model and configure DbContext for data access.
3. Register services and ILogger<T> in Startup.cs for dependency injection.
4. Implement CRUD endpoints in ToDoController following REST conventions.
5. Create an xUnit test project and write unit tests for each controller action.
6. Scaffold a new Angular application using the Angular CLI.
7. Import HttpClientModule and ReactiveFormsModule in AppModule.
8. Generate a ToDo service and implement methods (getAll, getById, create, update, delete) with HttpClient and catchError.
9. Create ToDo list and form components, implement reactive forms with validation.
10. Manage component state with BehaviorSubject or component variables, subscribe to the ToDo service.
11. Display data and handle error messages in the UI.
12. Write Jasmine/Karma tests for components and services to ensure functionality.

## API Endpoints

- GET    /api/todo       : Retrieve all to-do items
- GET    /api/todo/{id}  : Retrieve a single to-do item by ID
- POST   /api/todo       : Create a new to-do item
- PUT    /api/todo/{id}  : Update an existing to-do item
- DELETE /api/todo/{id}  : Delete a to-do item