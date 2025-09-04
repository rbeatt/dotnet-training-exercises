# .NET Training Exercises

This repository contains the materials for a 14-day .NET training course used by Kainos staff.

## Who this is for
Kainos staff enrolled in the .NET training course. Each participant completes exercises and submits solutions separately.

## What you'll achieve
- Build a set of small .NET projects exercising core C# language features, testing, persistence (EF Core), and web APIs.
- Produce a working solution and basic tests for each exercise.

## Quick links
- Course outline: [DotNet_Training_Course_Outline.md](DotNet_Training_Course_Outline.md)
- Full exercises: [DotNet_Training_Exercises_Full.md](DotNet_Training_Exercises_Full.md)

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

## JIRA CSV import
- A CSV for tracking progress is included: `dot_net_training_progress.csv`.
- For import details, see Atlassian's documentation: https://support.atlassian.com/jira-cloud-administration/docs/import-data-from-a-csv-file/

## Contributing (for maintainers)
- If you want to contribute changes to these materials, open a pull request against this repository explaining the change.

## License
- This repository is licensed under the MIT License — see the `LICENSE` file for details.
