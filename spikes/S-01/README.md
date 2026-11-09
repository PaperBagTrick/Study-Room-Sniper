# Spike S-01: read library availability without signing in

**Question:** Can a program read free/taken slots and capacity of all 17 McDermott
group study and smart rooms from the public LibCal pages, without signing in, using
one request per room per cycle, finishing a full cycle in under 60 s?

**Addresses:** R1, A1, A2, ADR-02, QAS-01, QAS-03, Q1.

## How to run
1. Copy `rooms.example.json` to `rooms.json`; fill lid/gid/eid from browser DevTools (logged out).
2. `python3 spike.py --minutes 60` (Python 3 stdlib only; no credentials used or stored).
3. `python3 summarize.py`

## Result (fill from the committed request_log.csv, real numbers only)
| Measure | Value |
|---|---|
| Run date/time, duration | |
| Rooms parsed out of 17 | |
| Capacity obtainable? How? | |
| Longest full cycle (s) | |
| Highest requests in any minute | |
| Failed requests | |
| Free-slot changes seen | |

## Conclusion
Yes / No, and what it means for A1, ADR-02, R1, Q1.

## Limitations
(e.g. run length, day of week, anything not tested)
