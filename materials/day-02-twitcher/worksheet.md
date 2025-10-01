# Day 2 Worksheet: Twitcher

Given counts: [0, 2, 5, 3, 7, 8, 4]

Expected:
- Today() → 4
- IncrementToday() → 5 (today becomes 5)
- HasDayWithoutBirds() → true
- Total() → 29 (before increment) or 30 (after increment)
- BusyDays(5) → 3 (days with 5, 7, 8)
- CountForDay(2) → 5

Additional test arrays:
- [] → handle empty
- [0,0,0] → HasDayWithoutBirds() true, BusyDays(1) 0
- [1,1,1,1,1,1,1] → BusyDays(1) 7
