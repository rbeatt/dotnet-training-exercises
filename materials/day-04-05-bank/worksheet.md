# Days 4–5 Worksheet: Bank Account System

Use these scenarios to validate your domain and persistence:

1. A001 after T001 and T002 → Balance: 1150
2. A002 after T003 and T004 → Allow overdraft true, intermediate negative allowed, final balance: 100
3. A003 T005 → Withdrawal should fail; balance remains 0
4. A004 T006 → Deposit of 0 should fail validation
5. A004 T007 → Withdrawal exceeding balance with overdraft not allowed should fail

Additional checks:
- IsOverdrawn property reflects negative balances only when allowed.
- Transaction history is recorded in order.
- Concurrency: parallel withdrawal attempts should not allow going below zero when not permitted.
