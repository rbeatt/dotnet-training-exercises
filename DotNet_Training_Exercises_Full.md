# .NET Training Exercises

This document contains the updated, detailed exercises for the .NET training programme. Each exercise includes an introduction, challenge, stretch goals, and useful links. The course has been optimised for a realistic 12-day schedule.

Note: Some exercises optionally integrate Azure services. Students may need an Azure free subscription (or a Kainos-provided subscription). For authentication and persistence, prefer local databases by default (SQLite/LocalDB).

---

## Day 1: FizzBuzz + Calculator

### Introduction

Warm-up exercises to practise loops, conditionals, console I/O, and error handling.

### The Challenge

1. FizzBuzz: Write a C# console app that prints numbers from 1 to `n` with:

   * `Fizz` if divisible by 3
   * `Buzz` if divisible by 5
   * `FizzBuzz` if divisible by both 3 and 5
   
   Command-line arguments should only allow replacing the divisors for Fizz and Buzz (defaults: 3 and 5). For example: `--fizzDivisor 3 --buzzDivisor 5`. Identify and handle edge cases, including zero divisors (avoid modulo-by-zero by validating or defining a no-op behaviour), negative divisors (normalise or reject), and equal divisors.

2. Calculator: Implement `SimpleCalculator.Calculate(int a, int b, char op)` supporting `+`, `-`, `*`, `/` and handling invalid operations or division by zero.

### Stretch Goals

* xUnit tests: Write xUnit tests covering calculator operations and FizzBuzz edge cases (including zero divisors and negative inputs).
* Logging (optional): Add logging using Serilog for inputs and errors. Default to console logging. File logging is optional; if enabled, write to a local `./logs` folder (e.g., `./logs/app-.log` with rolling files) and keep it disabled by default.

### Useful Links

* [C# Iteration Statements](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/statements/iteration-statements)
* [Exceptions](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/exceptions/)
* [Console I/O](https://devm.io/csharp/c-sharp-console-app-167696)
* [Serilog](https://serilog.net/)

 

### Supporting Materials

- Worksheet: [materials/day-01-fizzbuzz-calculator/worksheet.md](materials/day-01-fizzbuzz-calculator/worksheet.md)

---

## Day 2: Twitcher

### Introduction

Practise array operations and LINQ by working through the classic bird counting kata.

### The Challenge

Implement a `Twitcher` class operating on an `int[]` of daily bird counts. Include six methods:

1. Today() → return today’s count
2. IncrementToday() → increment today’s count and return new value
3. HasDayWithoutBirds() → true if any day has zero
4. Total() → sum of counts
5. BusyDays(threshold) → number of days with counts >= threshold (e.g., 5)
6. CountForDay(index) → count for a given day index (0-based)

### Stretch Goals

* Use LINQ for calculations where appropriate.
* Add input validation (null/empty arrays, out-of-range indices).
* Add xUnit tests for each method.

### Useful Links

* [LINQ Queries](https://learn.microsoft.com/en-us/dotnet/csharp/linq/get-started/introduction-to-linq-queries)
* [xUnit](https://xunit.net/)

 

### Supporting Materials

- Worksheet: [materials/day-02-twitcher/worksheet.md](materials/day-02-twitcher/worksheet.md)

---

## Day 3: Log Analyser

### Introduction

Practise file I/O, parsing, and aggregation by analysing application logs.

### The Challenge

Build a console app that takes a log file path as input (argument or prompt). Read the file and:

1. Count the number of `INFO`, `WARN`, and `ERROR` messages.
2. Produce a summary of the top 3 most frequent error messages (by message text).
3. Output totals and the summary to the console.

### Stretch Goals

* Handle missing, empty, or malformed files gracefully.
* Output results to a CSV or JSON file alongside console output.
* Add xUnit tests for parsing and aggregation.

### Useful Links

* [File I/O in C#](https://learn.microsoft.com/en-us/dotnet/standard/io/)
* [xUnit](https://xunit.net/)

### Supporting Materials

- Logs: 
   - [materials/day-03-log-analyser/logs/app-01.log](materials/day-03-log-analyser/logs/app-01.log)
   - [materials/day-03-log-analyser/logs/app-02.log](materials/day-03-log-analyser/logs/app-02.log)
   - [materials/day-03-log-analyser/logs/server-2025-09-25.log](materials/day-03-log-analyser/logs/server-2025-09-25.log)
- Worksheet (expected counts and top-3 errors): [materials/day-03-log-analyser/worksheet.md](materials/day-03-log-analyser/worksheet.md)

---

## Day 4–5: Bank Account System

### Introduction

Simulate a banking system with EF Core persistence and testing. Use a local database (SQLite/LocalDB) — no Azure dependency required.

### The Challenge

1. Implement `Account` with deposits, withdrawals, and balance checks.
2. Add `IsOverdrawn` property.
3. Persist accounts using EF Core with SQLite (or LocalDB).
4. Seed sample accounts and transactions for testing.

### Stretch Goals

* Add a `Transaction` history table and statements.
* Add acceptance tests (end-to-end scenarios) using xUnit.
* Consider concurrency and validation rules (e.g., no negative deposits, prevent overdraft when not allowed).

### Useful Links

* [Entity Framework Core](https://learn.microsoft.com/en-us/ef/core/)
* [xUnit](https://xunit.net/)
* [SQLite EF Core provider](https://learn.microsoft.com/en-us/ef/core/providers/sqlite/)

### Supporting Materials

- Accounts dataset: [materials/day-04-05-bank/datasets/accounts.csv](materials/day-04-05-bank/datasets/accounts.csv)
- Transactions dataset: [materials/day-04-05-bank/datasets/transactions.csv](materials/day-04-05-bank/datasets/transactions.csv)
- Worksheet (scenarios & validations): [materials/day-04-05-bank/worksheet.md](materials/day-04-05-bank/worksheet.md)

---

## Day 6: API Consumer Challenge

### Introduction

Learn to consume external REST APIs with .NET.

### The Challenge

1. Use `HttpClient` to call [PokéAPI](https://pokeapi.co/).
2. Prompt the user for a Pokémon name.
3. Print its ID, types, and abilities.
4. Save the results to timestamped text files (one file per query) in a local `results/` folder.
 5. Optional: Implement a retry policy for transient HTTP failures using [Polly](https://www.thepollyproject.org/) with exponential backoff and small jitter. Retry on timeouts and 5xx status codes only; do not retry on 4xx (e.g., 404 Not Found).

### Stretch Goals

* Handle not-found and network errors gracefully.
* Extract the retry configuration (max attempts, base delay) to configuration and allow turning retries on/off.
* Unit tests are optional for this exercise.

### Useful Links

* [HttpClient](https://learn.microsoft.com/en-us/dotnet/api/system.net.http.httpclient)
* [Async Programming](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/async/)
* [File I/O in C#](https://learn.microsoft.com/en-us/dotnet/standard/io/)
* Retry policy (Polly, exponential backoff): https://learn.microsoft.com/en-us/dotnet/architecture/microservices/implement-resilient-applications/implement-http-call-retries-exponential-backoff-polly

 

### Supporting Materials

- Worksheet: [materials/day-06-api-consumer/worksheet.md](materials/day-06-api-consumer/worksheet.md)
- Sample output (format example): [materials/day-06-api-consumer/samples/pikachu-EXAMPLE.txt](materials/day-06-api-consumer/samples/pikachu-EXAMPLE.txt)

---

## Day 7: Web API Tutorial

### Introduction

Build a REST API with ASP.NET Core following Microsoft’s tutorial. Emphasise RESTful resource design.

### The Challenge

Follow the [Microsoft Web API tutorial](https://learn.microsoft.com/en-us/aspnet/core/tutorials/first-web-api?view=aspnetcore-8.0) and extend it:

* Add Swagger documentation.
* Add authentication using ASP.NET Core Identity or cookie-based authentication against a local DB (SQLite/LocalDB) — this is the expected approach for the course.
   - Optional: explore API key or JWT authentication as an advanced stretch if time permits.
* Make REST explicit: use correct HTTP verbs, status codes, and resource-based routes; provide JSON representations.

### Stretch Goals

* Add integration tests using an in-memory database.

### Useful Links

* [Swagger in ASP.NET Core](https://learn.microsoft.com/en-us/aspnet/core/tutorials/getting-started-with-swashbuckle)
* [Authentication overview](https://learn.microsoft.com/en-us/aspnet/core/security/authentication/)
* [ASP.NET Core Identity](https://learn.microsoft.com/en-us/aspnet/core/security/authentication/identity)
* [Cookie authentication in ASP.NET Core](https://learn.microsoft.com/en-us/aspnet/core/security/authentication/cookie)
* [REST basics](https://restfulapi.net/)
* Optional (deployment): [Secure app authentication with Azure App Service](https://learn.microsoft.com/en-us/azure/app-service/scenario-secure-app-authentication-app-service?tabs=workforce-configuration)

### Sample Requests/Responses

- GET /api/items → 200 OK with array of items
- POST /api/items → 201 Created with Location header
- GET /api/items/{id} → 200 OK or 404 Not Found

### Supporting Materials

- Worksheet: [materials/day-07-web-api/worksheet.md](materials/day-07-web-api/worksheet.md)

---

## Day 8: MVC Tutorial

### Introduction

Follow the Microsoft Learn tutorial to build an ASP.NET Core MVC app.

### The Challenge

Follow the official Microsoft Learn tutorial end-to-end to create an MVC application. Complete the steps as described in the tutorial.

### Stretch Goals

If time permits, continue to the “ASP.NET Core MVC with EF Core” tutorial series to add database persistence using EF Core (SQLite/LocalDB).

### Useful Links

* [Tutorial: Create a web app with ASP.NET Core MVC](https://learn.microsoft.com/en-us/aspnet/core/tutorials/first-mvc-app/start-mvc?view=aspnetcore-8.0)
* [ASP.NET Core MVC with EF Core - Tutorial series](https://learn.microsoft.com/en-us/aspnet/core/data/ef-mvc/intro?view=aspnetcore-8.0)

### Supporting Materials

- Worksheet: [materials/day-08-mvc/worksheet.md](materials/day-08-mvc/worksheet.md)

---

## Day 9–10: AI Tutorials (Cognitive Search + Vision)

### Introduction

Follow Microsoft tutorials to integrate Azure Cognitive Search skillsets and Azure AI Vision (Image Analysis) with .NET.

### The Challenge

1. Complete the Azure Cognitive Search skillset tutorial (C#, end-to-end): define a data source, skillset, index, and indexer; run the indexer.
2. Complete the Azure AI Vision Image Analysis quickstart (v4.0): analyse the provided sample images.
3. Save outputs (JSON or CSV) from both tutorials to the local `results/` folder for review.

### Stretch Goals

* Focus on completing both tutorials end-to-end (unit tests are not required for this module).
* Optional: wrap tutorial steps in a small .NET console app that reads config from environment variables and writes outputs to `results/`.

### Useful Links

* [Azure AI services](https://azure.microsoft.com/en-us/products/ai-services/)
* [Azure Cognitive Search: Build a skillset (C# tutorial)](https://learn.microsoft.com/en-us/azure/search/tutorial-skillset?pivots=csharp)
* [Azure AI Vision: .NET Image Analysis quickstart (v4.0)](https://learn.microsoft.com/en-us/azure/ai-services/computer-vision/quickstarts-sdk/image-analysis-client-library-40?tabs=visual-studio%2Cwindows&pivots=vision-studio)

### Supporting Materials

- Cognitive Search sample docs: [materials/day-09-10-ai/datasets/search-docs/](materials/day-09-10-ai/datasets/search-docs/)
- Vision sample images (placeholders): [materials/day-09-10-ai/datasets/images/](materials/day-09-10-ai/datasets/images/)
- Worksheet: [materials/day-09-10-ai/worksheet.md](materials/day-09-10-ai/worksheet.md)
- Example outputs (for validation): [materials/day-09-10-ai/example-outputs.md](materials/day-09-10-ai/example-outputs.md)

---

## Day 11–12: Todo App (Capstone)

### Introduction

Full-stack ASP.NET Core app with database persistence. Deployment is optional.

### The Challenge

1. Add filtering (completed/uncompleted tasks).
2. Add `DueDate` property.
3. Authentication is optional (ASP.NET Core Identity or cookie-based auth against a local DB such as SQLite/LocalDB).

### Stretch Goals

* Add integration tests using an in-memory database.
* Add sorting and basic pagination.
* Add logging with Serilog (console by default; optional local rolling file sink to `./logs`).
* Configuration: demonstrate reading a connection string from `web.config` when running locally (for learning purposes only; not recommended for production security). Prefer user-secrets or environment variables in real apps.

### Useful Links

* [ASP.NET Core Identity](https://learn.microsoft.com/en-us/aspnet/core/security/authentication/identity)
* [Entity Framework Core](https://learn.microsoft.com/en-us/ef/core/)
* Optional (deployment): [Secure app authentication with Azure App Service](https://learn.microsoft.com/en-us/azure/app-service/scenario-secure-app-authentication-app-service?tabs=workforce-configuration)

### Supporting Materials

- Seed tasks CSV: [materials/day-11-12-todo/seeds/tasks.csv](materials/day-11-12-todo/seeds/tasks.csv)
- Worksheet (filtering, due dates, sorting): [materials/day-11-12-todo/worksheet.md](materials/day-11-12-todo/worksheet.md)

---

## General Notes

- Course length: 12 days.
- Azure: Students may need an Azure free subscription (or Kainos-provided). Use local DBs by default, especially for authentication. When exercises call for authentication, the expected approaches are ASP.NET Core Identity or cookie-based authentication backed by a local DB (SQLite/LocalDB). Other mechanisms (API key/JWT) can be explored as optional advanced topics.
- Supporting materials: Every exercise includes or references logs, sample files, and worksheets to validate expected outputs.
   - Index: [materials/README.md](materials/README.md)