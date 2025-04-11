# 🧪 Practical 20 - ASP.NET Core MVC Application

## Prerequisites

### Connection String Configuration

Add the following connection string to your `appsettings.json` file:

```xml
 "ConnectionStrings": {
   "DefaultConnection": "Server=SF-CPU-0226\\SQLEXPRESS;Database=Practical_20;Trusted_Connection=True;TrustServerCertificate=True"
 },
```

In program file while you running update data base comment out the following code 

```csharp
builder.Logging.AddProvider(new DatabaseLoggerProvider(builder.Services.BuildServiceProvider()));
```

> **Note:** Modify the connection string according to your SQL Server configuration if needed.

## Database Migration

For each project, you need to apply the migrations to create the database schema:

1. Open the Package Manager Console (Tools > NuGet Package Manager > Package Manager Console)
2. Select the appropriate project in the "Default project" dropdown
3. Run the following command:
   ```
   Update-Database
   ```
Once you done the migration then re enable in program.cs
```csharp
builder.Logging.AddProvider(new DatabaseLoggerProvider(builder.Services.BuildServiceProvider()));
```

**Log Entries**
![image](https://github.com/user-attachments/assets/1f64f57d-8129-4bc0-80b6-e1da4d816a90)


