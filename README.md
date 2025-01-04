# To-Do App with Employee Management

## Project Overview

This is a Blazor Server application for managing tasks and employees. The project allows administrators to create, view, assign, and delete tasks, as well as manage employee data. It serves as a practical demonstration of database management system (DBMS) concepts by integrating a SQLite database for task and employee management.

## Features

### 1. **Employee Management**
- **Create Employees**: Add new employees with a name and username.
- **View Employees**: View the list of existing employees.
- **Delete Employees**: Remove employees from the system.

### 2. **Task Management**
- **Create Tasks**: Add tasks to the to-do list.
- **View Tasks**: View a list of all tasks.
- **Update Tasks**: Mark tasks as complete or incomplete.
- **Delete Tasks**: Remove tasks from the system.

### 3. **Task Assignment**
- **Assign Tasks**: Assign tasks to employees using a dropdown menu.
- **View Assignments**: See which tasks are assigned to specific employees.

## Getting Started

### Prerequisites
- [.NET SDK](https://dotnet.microsoft.com/download) installed.
- A SQLite-compatible database viewer (optional, for inspecting the database).

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/todo-employee-management.git
   ```

2. Navigate to the project directory:
   ```bash
   cd todo-employee-management
   ```

3. Restore dependencies:
   ```bash
   dotnet restore
   ```

4. Build the project:
   ```bash
   dotnet build
   ```

### Running the Application
1. Start the application:
   ```bash
   dotnet run
   ```

2. Open your browser and navigate to `http://localhost:5000`.

## Usage

### Admin Login
To access the application, you must log in as an administrator. The admin status is managed using `ProtectedSessionStorage`.

### Adding Tasks
1. Enter the task name in the input field.
2. Click "Add Task" to add it to the list.

### Assigning Tasks
1. Select an employee from the dropdown menu.
2. Click "Assign" to assign the selected task to the chosen employee.

### Managing Employees
1. Navigate to the employee management section.
2. Add or delete employees as needed.

## Database Schema

### Tasks Table (`ToDo`)
| Column | Type | Description |
|--------|------|-------------|
| `Id` | INTEGER | Primary Key (Auto Increment) |
| `Task` | TEXT | Task description |
| `IsComplete` | INTEGER | Task status (0 = incomplete, 1 = complete) |
| `AssignedTo` | TEXT | Username of the assigned employee |
| `CreatedAt` | DATETIME | Timestamp when the task was created |
| `UpdatedAt` | DATETIME | Timestamp when the task was last updated |

### Employees Table
| Column | Type | Description |
|--------|------|-------------|
| `Name` | TEXT | Employee's full name |
| `Username` | TEXT | Unique username |

## Built With
* **Blazor Server**: For building the user interface.
* **SQLite**: For database management.
* **C#**: Programming language used.
* **Bootstrap**: For styling the UI.

## Future Improvements
* Implement search and filtering for tasks and employees
* Add task priority levels
* Include user authentication for multiple roles (Admin, Employee)

## License
This project is licensed under the MIT License.

## Author
**Precious Chidera Orjiude**
* GitHub: Precious's GitHub
* Email: precious@example.com
