# Tips & Pitfalls

- Use EF Core SQLite provider for local DB.
- Seed data from CSV or code during migration/startup.
- Validate amounts: > 0 for deposits; > 0 and <= available for withdrawals (unless overdraft allowed).
- Consider optimistic concurrency (rowversion) for safety.
