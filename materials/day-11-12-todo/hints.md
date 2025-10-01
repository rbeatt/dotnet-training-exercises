# Tips & Pitfalls

- Use EF Core with SQLite for persistence; migrations for schema.
- Keep authentication optional; if added, the expected approaches are ASP.NET Core Identity or cookie-based authentication with SQLite.
- Add integration tests with in-memory DB to verify filters/sorting.
 - Logging: Use Serilog (console by default); optional rolling file sink to `./logs` for local development.
 - Configuration (learning exercise): Show how to read a connection string from `web.config` when running locally. Note: this approach is not recommended for production security — prefer user-secrets or environment variables for sensitive config.
