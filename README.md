# .NET Training Exercises

This repository contains a 14-day .NET training programme with daily objectives, exercises, stretch goals, and useful links.

Quick links
- Course outline: [DotNet_Training_Course_Outline.md](DotNet_Training_Course_Outline.md)
- Full exercises: [DotNet_Training_Exercises_Full.md](DotNet_Training_Exercises_Full.md)

Getting started
1. Install .NET SDK (required).
2. Use Visual Studio Code with the C# extension for editing and debugging.
3. Pick a day from the course outline and create a project, for example:
   - Create a console app: dotnet new console -o Day1.FizzBuzz
   - Run it: dotnet run --project Day1.FizzBuzz

Suggested workflow
- Work through the daily exercises in [DotNet_Training_Exercises_Full.md](DotNet_Training_Exercises_Full.md).
- Add unit tests with xUnit for core logic.
- Use EF Core and SQLite for persistence exercises.
- For web/API tasks, scaffold an ASP.NET Core project and enable Swagger for documentation.

Recommendations
- Use Git branches per day or feature.
- Add small commits and include concise PR descriptions.
- Optional: add CI (GitHub Actions) for build/test on push.

Contributing
- Edit the exercise files or add new example solutions in subfolders.
- Open a PR with a short description of changes.

License
- No license specified. Add a LICENSE file if you intend to publish

## JIRA CSV import

This repository includes a CSV for tracking progress: `dot_net_training_progress.csv`.

For a clean, supported import process (including field mapping and options) follow Atlassian's documentation: https://support.atlassian.com/jira-cloud-administration/docs/import-data-from-a-csv-file/