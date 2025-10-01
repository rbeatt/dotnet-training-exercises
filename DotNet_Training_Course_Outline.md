# .NET Training Course Outline (12 Days)

This course provides a structured programme for graduate/associate software engineers to build solid .NET and ASP.NET Core skills over 12 days, with AI integration and a final capstone (Todo) app. Azure services are optional; prefer local databases (SQLite/LocalDB) by default.

---

## Day 1: FizzBuzz + Calculator
- **Objective:** Warm-up to practise loops, conditionals, console I/O, and error handling. Command-line arguments only replace Fizz/Buzz divisors. Students should identify and handle edge cases (e.g., zero/negative/equal divisors). Logging is optional. Tests use xUnit.
- **Key Skills:** Iteration/conditionals, console I/O, basic error handling, xUnit fundamentals, optional logging (Serilog, console by default; optional local file sink).

---

## Day 2: Twitcher (BirdCount)
- **Objective:** Practise array operations and LINQ with the Twitcher kata. Implement six methods (Today, IncrementToday, HasDayWithoutBirds, Total, BusyDays, CountForDay).
- **Key Skills:** Arrays, LINQ basics, input validation, unit testing with xUnit.

---

## Day 3: Log Analyser
- **Objective:** Build a console app that takes a file path input; count INFO/WARN/ERROR and summarise top errors. Handle malformed lines gracefully.
- **Key Skills:** File I/O, text parsing, grouping/aggregation, xUnit tests for parsing/aggregation.

---

## Day 4–5: Bank Account System
- **Objective:** Implement Account with deposits, withdrawals, balance checks, and IsOverdrawn. Persist with EF Core using SQLite/LocalDB. Replace API endpoint stretch with acceptance tests.
- **Key Skills:** Domain modelling, EF Core (SQLite), data seeding, validation rules, acceptance testing with xUnit.

---

## Day 6: API Consumer Challenge
- **Objective:** Use HttpClient with PokéAPI; print Pokémon details and save results to timestamped text files in a local results/ folder. Add a retry policy (Polly) with exponential backoff for transient failures. Unit tests optional.
- **Key Skills:** HttpClient, async/await, resilient calls (Polly retry/backoff), file I/O for outputs.

---

## Day 7: Web API Tutorial
- **Objective:** Follow the Microsoft Web API tutorial; add Swagger and authentication. Emphasise RESTful resource design (verbs, status codes, resource routes).
- **Key Skills:** Controllers/routing, REST principles, Swagger (OpenAPI), authentication (ASP.NET Core Identity or cookie-based as the expected approaches; API key/JWT optional), integration testing (optional).

---

## Day 8: MVC Tutorial
- **Objective:** Follow the Microsoft Learn MVC tutorial to build an ASP.NET Core MVC app. Optionally continue the EF Core series for persistence.
- **Key Skills:** MVC patterns (controllers/views/models), form handling/validation, optional EF Core (SQLite/LocalDB).

---

## Day 9–10: AI Modules
- **Objective:** Use Azure AI Language (sentiment), Azure AI Vision (image analysis), and add simple search enrichment. Show how to integrate AI into a previous exercise. Drop unit test stretch goals.
- **Key Skills:** Azure AI services, SDK usage, integrating AI into console/web apps, presenting enriched outputs.

---

## Day 11–12: Todo App (Capstone)
- **Objective:** Add filtering and DueDate. Deployment optional. Authentication optional (Identity or cookie-based) against a local DB. Stretch: add logging with Serilog and demonstrate reading a connection string from `web.config` when running locally (learning-only; prefer user-secrets or environment variables for sensitive values).
- **Key Skills:** CRUD + filtering, persistence (EF Core), optional authentication with Identity/cookies, logging (Serilog), configuration providers/connection strings, basic integration testing.

---

## Notes
- Exercises are progressive; early days build foundational skills for later exercises.
- Stretch goals are optional and tailored per day in the full exercises document.
- Azure usage is optional; students may need an Azure free subscription (or Kainos-provided). Prefer local databases by default.

---

## Recommended Learning Resources
- [C# Documentation](https://learn.microsoft.com/en-us/dotnet/csharp/)
- [ASP.NET Core Documentation](https://learn.microsoft.com/en-us/aspnet/core/)
- [Azure AI services](https://azure.microsoft.com/en-us/products/ai-services/)
- [xUnit.net](https://xunit.net/)
- [Entity Framework Core](https://learn.microsoft.com/en-us/ef/core/)
