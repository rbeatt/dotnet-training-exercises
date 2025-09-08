# .NET Training Exercises (Optimised)

This document contains the updated, detailed exercises for the .NET training programme. Each exercise includes an introduction, challenge, stretch goals, and useful links. The course has been optimised for a realistic 14-day schedule.

---

## Day 1: FizzBuzz + Calculator

### Introduction

Warm-up exercises to practise loops, conditionals, console I/O, and error handling.

### The Challenge

1. FizzBuzz: Write a C# console app that prints numbers from 1 to `n` with:

   * `Fizz` if divisible by 3
   * `Buzz` if divisible by 5
   * `FizzBuzz` if divisible by both 3 and 5
2. Calculator: Implement `SimpleCalculator.Calculate(int a, int b, char op)` supporting `+`, `-`, `*`, `/` and handling invalid operations or division by zero.

### Stretch Goals

* Accept input from the command line.
* Add logging using Serilog.
* Write unit tests for calculator methods.

### Useful Links

* [C# Iteration Statements](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/statements/iteration-statements)
* [Exceptions](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/exceptions/)
* [Console I/O](https://devm.io/csharp/c-sharp-console-app-167696)
* [Serilog](https://serilog.net/)

---

## Day 2: BirdCount + Log Analyser

### Introduction

Practise LINQ queries, array operations, and file I/O.

### The Challenge

1. BirdCount: Implement methods to get today’s count, check for zero-bird days, and count busy days.
2. Log Analyser: Read a log file and count `INFO`, `WARN`, `ERROR` messages; find top 3 errors.

### Stretch Goals

* Use LINQ for calculations and grouping.
* Save results to CSV files.
* Handle missing or empty files gracefully.

### Useful Links

* [LINQ Queries](https://learn.microsoft.com/en-us/dotnet/csharp/linq/get-started/introduction-to-linq-queries)
* [File I/O in C#](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/file-system/how-to-read-and-write-to-a-text-file)

---

## Day 3-4: Bank Account System

### Introduction

Simulate a banking system with EF Core persistence and unit testing.

### The Challenge

1. Implement `Account` class with deposits, withdrawals, and balance checks.
2. Add `IsOverdrawn` property.
3. Store accounts in a database using EF Core.
4. Write xUnit tests for core functionality.

### Stretch Goals

* Add a `Transaction` history table.
* Create a simple API endpoint to list accounts.

### Useful Links

* [Entity Framework Core](https://learn.microsoft.com/en-us/ef/core/)
* [xUnit](https://xunit.net/)

---

## Day 5: API Consumer Challenge

### Introduction

Learn to consume external REST APIs with .NET.

### The Challenge

1. Use `HttpClient` to call [PokéAPI](https://pokeapi.co/).
2. Prompt the user for a Pokémon name.
3. Print its ID, types, and abilities.

### Stretch Goals

* Handle not-found errors.
* Save results to SQLite using EF Core.
* Mock API calls in unit tests.

### Useful Links

* [HttpClient](https://learn.microsoft.com/en-us/dotnet/api/system.net.http.httpclient)
* [Async Programming](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/async/)

---

## Day 6-7: Web API Tutorial

### Introduction

Build a REST API with ASP.NET Core.

### The Challenge

Follow the [Microsoft Web API tutorial](https://learn.microsoft.com/en-us/aspnet/core/tutorials/first-web-api?view=aspnetcore-8.0) and extend it:

* Add Swagger documentation.
* Add authentication (API key or JWT).

### Useful Links

* [Swagger in ASP.NET Core](https://learn.microsoft.com/en-us/aspnet/core/tutorials/getting-started-with-swashbuckle)
* [Authentication](https://learn.microsoft.com/en-us/aspnet/core/security/authentication/)

---

## Day 8-9: Todo App Exercise

### Introduction

Full-stack ASP.NET Core app with database persistence and Azure deployment.

### The Challenge

1. Add filtering (completed/uncompleted tasks).
2. Add `DueDate` property.
3. Deploy to Azure App Service.
4. Set up CI/CD with GitHub Actions.

### Stretch Goals

* Add user authentication.
* Write integration tests using an in-memory database.

### Useful Links

* [Azure Deployment](https://learn.microsoft.com/en-us/azure/app-service/quickstart-dotnetcore)
* [GitHub Actions for .NET](https://learn.microsoft.com/en-us/dotnet/devops/github-actions-dotnet)

---

## Day 10-11: AI Modules

### Introduction

Introduce AI integration with .NET applications using Azure AI services.

### The Challenge

1. Use Azure AI Language for sentiment analysis.
2. Use Azure AI Vision to analyse images.
3. Integrate outputs into console or web apps.

### Stretch Goals

* Integrate AI features into the Todo app or other exercises.
* Write unit tests for AI integration.

### Useful Links

* [Azure AI services](https://azure.microsoft.com/en-us/products/ai-services/)
* [Azure AI Language](https://learn.microsoft.com/en-us/azure/ai-services/language-service/)
* [Azure AI Vision](https://learn.microsoft.com/en-us/azure/ai-services/computer-vision/)

---

## Day 12-14: Final Project

### Introduction

Capstone project to consolidate all learning.

### The Challenge

1. Extend Todo App or build a new project (blog, expense tracker, etc.).
2. Include:

   * Database persistence
   * API endpoints
   * Unit tests
   * Deployment
3. Present your project to peers.

### Stretch Goals

* Add authentication and authorisation.
* CI/CD pipeline.
* Optional AI integration.
* Use cloud database (Azure SQL).

---