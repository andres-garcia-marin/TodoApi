# TodoApi

A RESTful web API built with ASP.NET Core for managing a collection of To-Do items. This application leverages Entity Framework Core for data management via a standard repository context architecture.

---

## 🚀 Features

* **Complete CRUD Capabilities**: Full support for Creating, Reading, Updating, and Deleting tasks.
* **Entity Framework Integration**: Implements a dedicated `TodoContext` to abstract data layers cleanly.
* **Robust Data Model**: Uses a strict structure defined by `TodoItem` to enforce data types.
* **JSON Serialization**: Ready-to-consume payloads natively supported by web/mobile frontends.

---

## 🛠️ Tech Stack

* **Framework**: .NET Core (ASP.NET Core Web API)
* **ORM**: Entity Framework Core (EF Core)
* **Language**: C#

---

## 🏁 Getting Started

Follow these steps to run the Web API locally on your development system.

### Prerequisites

Ensure you have the required runtime installed on your machine:
* [.NET SDK](https://microsoft.com) (Version corresponding to your `.sln` configuration)

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com
   cd TodoApi
   ```

2. **Restore dependencies:**
   ```bash
   dotnet restore
   ```

### Running the Application

To spin up the web server locally, execute the following command in the directory containing the project:

```bash
dotnet run --project TodoApi
```

The application will launch and expose local endpoints, typically visible at:
* `https://localhost:5001` or `http://localhost:5000` 
* (Check your `Properties/launchSettings.json` file to confirm your local ports)

---

## 🛣️ API Endpoints

### Tasks Resource

| HTTP Method | Route Endpoint | Action Description | Default Response |
| :--- | :--- | :--- | :--- |
| **GET** | `/api/TodoItems` | Fetch all available tasks | `200 OK` |
| **GET** | `/api/TodoItems/{id}` | Fetch a specific task by its unique ID | `200 OK` / `404 Not Found` |
| **POST** | `/api/TodoItems` | Create and store a new task | `201 Created` / `400 Bad Request` |
| **PUT** | `/api/TodoItems/{id}` | Modify an existing task by its ID | `204 No Content` / `400 Bad Request` |
| **DELETE** | `/api/TodoItems/{id}` | Permanently destroy a task from storage | `200 OK` / `404 Not Found` |

### Sample JSON Request Body (`POST /api/TodoItems`)

```json
{
  "name": "Complete repository documentation",
  "isComplete": false
}
```

---

## 📂 Project Architecture

* **`TodoApi.sln`**: The parent Visual Studio solution routing.
* **`TodoContext.cs`**: The data layer bridge managing database context mapping.
* **`TodoItem.cs`**: The C# model schema regulating task payloads.
* **`TodoApi/`**: Main application source files directory.

---

## 🤝 Contributing

1. Fork the Project.
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`).
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the Branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.
