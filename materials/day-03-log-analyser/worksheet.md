# Day 3 Worksheet: Log Analyser

For each sample log, compute:
- Count of INFO/WARN/ERROR.
- Top 3 most frequent ERROR messages (by message text).

Sample expectations (partial, verify with your implementation):

app-01.log
- INFO: 6
- WARN: 4
- ERROR: 6
- Top errors:
  1) "Timeout while calling downstream service" (3)
  2) "Database connection failed" (2)
  3) "NullReferenceException in HomeController.Index" (1)

app-02.log (intentionally malformed lines exist — skip lines that don't match your parser's pattern)
- INFO: 3
- WARN: 2 (one blank message still counts as WARN)
- ERROR: 4 (count only lines with a clear "[ERROR]" marker)
- Top errors:
  1) "Failed to parse request body" (3)
  2) "Unauthorized access" (1)
  3) others tied at 1 or excluded

server-2025-09-25.log
- INFO: 9
- WARN: 4
- ERROR: 11
- Top errors (by message):
  1) "Failed to parse request body" (5)
  2) "Database connection failed" (3)
  3) "Unauthorized" (2)

Note: Counts above are guidance and depend on your parsing rules. Document your assumptions.
