# Tips & Pitfalls

FizzBuzz:
- Keep output formatting consistent (one per line or comma-separated as required).
- Use modulo to test divisibility.
- Validate command-line arguments; default to 3 and 5 when not provided.
 - Edge cases to consider:
	 - Zero divisors (avoid modulo by zero; either reject with a message or define that a zero divisor is disabled).
	 - Negative divisors (normalise or reject).
	 - When fizz and buzz divisors are equal.

Calculator:
- Decide whether to throw exceptions or return error codes/messages for invalid operations and division by zero.
- Consider integer division behaviour.

Logging (optional):
- If you use Serilog, default to console logging for development.
- File logging is optional; if added, write to a local `./logs` folder within the project (e.g., `./logs/app-.log` with rolling files).
