# Day 6 Worksheet: API Consumer

Requests:
- Input: "pikachu" → expect id=25; types include "electric"; abilities include entries like "static".
- Input: "missingno" → expect friendly error message and no output file (or an error file explaining failure).

Validation:
- Results are written to results/<name>-YYYYMMDD-HHMMSS.txt
- File content includes name, id, types (comma-separated), abilities (comma-separated)
 - If retries are enabled:
	 - 404 Not Found should not be retried; return a friendly message.
	 - Transient failures (e.g., timeouts, 5xx) should trigger a small number of exponential backoff retries.
	 - Retries should be configurable and clearly logged (attempt count and delay optional).
