# Days 11–12 Worksheet: Todo App

Scenarios:
- Filter: show only completed; expect 1 item (Pay bills)
- Filter: show only uncompleted; expect 4 items
- Add DueDate to existing tasks; ensure sorting by due date ascending works
- Sorting: by priority then due date
- Pagination: show 2 items per page (optional)
 - Optional: Logging present (Serilog) → console output for key actions; file logging if enabled writes to ./logs with daily rolling files
 - Optional: When running locally, app reads connection string from web.config (document the key name)

States after operations:
- Mark "Buy milk" completed → completed count increases by 1
- Set due date for "Plan trip" to 2025-10-15 → appears after 2025-10-01 in sorted list
