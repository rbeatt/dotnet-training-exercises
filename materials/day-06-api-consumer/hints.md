# Tips & Pitfalls

- Use a single HttpClient instance.
- Handle 404 Not Found and network failures (timeouts, DNS) gracefully.
- Serialise output consistently; ensure results/ directory exists.
- Consider cancellation tokens.

Retry policy (optional but recommended):
- Use [Polly](https://www.thepollyproject.org/) to add retries with exponential backoff and small jitter.
- Retry only on transient failures: HTTP 5xx and timeouts; do not retry on 4xx (e.g., 404).
- Keep total retry time bounded (e.g., 3–5 attempts, backoff 200ms → 400ms → 800ms + jitter).
- Make retries configurable (enable/disable, attempts, base delay) via app settings or environment variables.
