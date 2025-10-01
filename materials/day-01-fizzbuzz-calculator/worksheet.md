# Day 1 Worksheet: FizzBuzz + Calculator

Use these scenarios to validate your solution. Implement unit tests if you like.

## FizzBuzz Scenarios

- Input: n=16, fizz=3, buzz=5
  - Expected ending sequence: 13, 14, FizzBuzz, 16
- Input: n=14, fizz=2, buzz=7
  - Expected contains: Fizz (2), Buzz (7), FizzBuzz (14)
- Edge cases:
  - n=0 → outputs nothing
  - Negative n → handle gracefully (no output or error message)
  - fizz=buzz=1 → every number is FizzBuzz
  - fizz=0 or buzz=0 → decide how to handle. Options:
    - Validate and reject zero divisors (show a clear error), OR
    - Define behaviour (e.g., treat zero divisor as "disabled" so it never matches). Avoid modulo-by-zero.
  - Negative divisors (e.g., fizz=-3) → decide whether to accept (normalise with absolute value) or reject as invalid input.
  - fizz=buzz (e.g., both 3) → ensure FizzBuzz is printed when divisible by the shared divisor.

## Calculator Scenarios

- (a=3, b=5, op='+') → 8
- (a=10, b=0, op='/') → error (division by zero)
- (a=4, b=2, op='x') → error (invalid operator)
- (a=-7, b=3, op='-') → -10
- (a=6, b=7, op='*') → 42

## Optional: Logging Clarification

If you add logging (e.g., with Serilog):
- Default to console logging during development.
- File logging is optional; if used, write to a local project folder such as `./logs/app-.log` with daily rolling files. Do not write to system-level locations.
