# JWT-SecureAPI

A .NET Core Web API that provides secure CRUD operations using JWT authentication.  
This project is fully tested using Postman and includes login and signup endpoints for authentication.

## 🔐 Features

- ✅ User Registration
- ✅ User Login with JWT
- ✅ Secure CRUD APIs
- ✅ Tested using Postman
- ✅ Swagger support
- ✅ SQL Server integration
- ✅ EF Core Migrations used to create tables in the database

## 🔧 Setup

### 1. Clone or Download

- Clone the repository or download it as a ZIP.
- Open the `.sln` file in Visual Studio.

### 2. Setup the Database

- **Option 1:** Run the included `SecureAPI_DB.sql` file using **SQL Server Management Studio (SSMS)** to create the database, tables, and insert sample data.
  
- **Option 2:** You can also use **EF Core Migrations** to create the tables. In **Package Manager Console** (PMC) or **dotnet CLI**, run:
    - `Add-Migration InitialCreate` (if migration is not already created)
    - `Update-Database` (to apply migration and create the database schema)

### 3. Run the API

- Open the solution in Visual Studio.
- Build and run the project.

## 📁 Folder Structure

- `Controllers/` – Contains API endpoints  
- `Models/` – Data models  
- `Data/` – DB context and seeding  
- `Migrations/` – EF Core migrations  
- `Program.cs` – Entry point  
- `appsettings.json` – Configuration  

## 📄 Sample `appsettings.json`

```json
{
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft.AspNetCore": "Warning"
    }
  },
  "AllowedHosts": "*",
  "ConnectionStrings": {
    "DefaultConnection": "Server=YOUR_SERVER;Database=YOUR_DB;Trusted_Connection=True;"
  },
  "JWT": {
    "Audience": "http://localhost:7104",
    "Issuer": "http://localhost:7104",
    "Key": "your_jwt_secret_here"
  }
}
