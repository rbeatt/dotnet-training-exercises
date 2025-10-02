# .NET Training Exercises

This repository contains the materials for a 12-day .NET training course used by Kainos staff.

## Who this is for
Kainos staff enrolled in the .NET training course. Each participant completes exercises and submits solutions separately.

## What you'll achieve
- Build a set of small .NET projects exercising core C# language features, testing, persistence (EF Core), and web APIs.
- Produce a working solution and basic tests for each exercise.

## Quick links
- Course outline: [DotNet_Training_Course_Outline.md](DotNet_Training_Course_Outline.md)
- Full exercises: [DotNet_Training_Exercises_Full.md](DotNet_Training_Exercises_Full.md)

## Worksheets (quick links)
- Day 1: FizzBuzz + Calculator — [materials/day-01-fizzbuzz-calculator/worksheet.md](materials/day-01-fizzbuzz-calculator/worksheet.md)
- Day 2: Twitcher — [materials/day-02-twitcher/worksheet.md](materials/day-02-twitcher/worksheet.md)
- Day 3: Log Analyser — [materials/day-03-log-analyser/worksheet.md](materials/day-03-log-analyser/worksheet.md)
- Days 4–5: Bank — [materials/day-04-05-bank/worksheet.md](materials/day-04-05-bank/worksheet.md)
- Day 6: API Consumer — [materials/day-06-api-consumer/worksheet.md](materials/day-06-api-consumer/worksheet.md)
- Day 7: Web API — [materials/day-07-web-api/worksheet.md](materials/day-07-web-api/worksheet.md)
- Day 8: MVC — [materials/day-08-mvc/worksheet.md](materials/day-08-mvc/worksheet.md)
- Days 9–10: AI — [materials/day-09-10-ai/worksheet.md](materials/day-09-10-ai/worksheet.md)
- Days 11–12: Todo — [materials/day-11-12-todo/worksheet.md](materials/day-11-12-todo/worksheet.md)

## Requirements
- .NET SDK (install the latest stable SDK available to you)
- Visual Studio Code (recommended) with the C# extension

## Quick start
1. Verify .NET is installed:

```bash
dotnet --version
```

2. Create and run a simple console project for an exercise (example for Day 1):

```bash
dotnet new console -o Day01.FizzBuzz
dotnet run --project Day01.FizzBuzz
```

3. Create a test project and run tests:

```bash
dotnet new xunit -o Day01.Tests
dotnet test Day01.Tests
```

Project naming suggestion: DayXX.ShortName (for example: Day01.FizzBuzz).

## Course structure
- The course materials live in `DotNet_Training_Course_Outline.md` and `DotNet_Training_Exercises_Full.md`.
- Each exercise is described in the outline; implement your solution in a separate project/repository as described below.

## Workflow for participants
- Create a new project/repository for each exercise or solution (one repo per exercise). This keeps submissions isolated and easy to review.
- Make small, focused commits with clear messages.
- Optionally add CI (GitHub Actions) to run builds and tests on push.

## How to submit / share
- Push your exercise repository to your own GitHub account (or internal Git host) and share the repo URL with the course lead or via the course submission mechanism.

## Contributing (for maintainers)
- If you want to contribute changes to these materials, open a pull request against this repository explaining the change.

## License
- This repository is licensed under the MIT License — see the `LICENSE` file for details.
