# 🎬 MCIT-MVC-Movies

This is a sample **ASP.NET Core MVC** web application built as part of the **MCIT** training.  
It allows users to manage a list of movies with basic Create, Read, Update, and Delete (CRUD) operations.

---

## 🧾 Features

- Add new movies with title, release date, genre, and price.
- Edit and delete existing movies.
- View details of a specific movie.
- Search movies by title or genre.
- Built using **Entity Framework Core** for database operations.

---

## 🛠️ Technologies Used

- ASP.NET Core MVC (.NET 8)
- Entity Framework Core
- Razor Views
- C#
- SQL Server / SQLite

---

## 💽 Requirements

- .NET SDK 8.0+
- Visual Studio 2022 or later / Visual Studio Code
- Local SQL Server or SQLite

---

## 🚀 How to Run

1. **Clone the repository**  
   Open terminal and run:

   ``` bash
   git clone https://github.com/your-username/MCIT-MVC-Movies.git
   cd MCIT-MVC-Movies
   ```
- Apply EF Migrations

```bash

dotnet ef migrations add InitialCreate
dotnet ef database update
```
(Optional) Seed Data
- In Program.cs, call the seeding method:

```csharp

using (var scope = app.Services.CreateScope())
{
    var services = scope.ServiceProvider;
    SeedData.Initialize(services);
}
```
- Run the application

```bash

dotnet run
```

###📁 Project Structure

```bash
MCIT-MVC-Movies/
│
├── Controllers/
│   └── MoviesController.cs
│
├── Models/
│   ├── Movie.cs
│   └── MvcMovieContext.cs
│
├── Views/
│   └── Movies/
│       ├── Index.cshtml
│       ├── Create.cshtml
│       ├── Edit.cshtml
│       ├── Details.cshtml
│       └── Delete.cshtml
│
├── Data/
│   └── SeedData.cs
│
├── Program.cs
├── appsettings.json
└── MCIT-MVC-Movies.csproj
```