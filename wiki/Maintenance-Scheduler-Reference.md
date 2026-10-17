# Texas Septic Maintenance Scheduler Reference

> **Quick answer:** Out West Septic does NOT run a pump truck. We refer pumping to local pumpers and use `outwestseptic_maintenance_scheduler.py` to give homeowners a defensible "pump every N years" schedule.

## Pump interval table (Texas A&M AgriLife Extension guidance)

| Tank size × House | Base interval |
|-------------------|---------------|
| 1000 gal × 2 | 5.5 years |
| 1000 gal × 4 | 2.5 years |
| 1000 gal × 6 | 1.5 years |
| 1250 gal × 2 | 6.0 years |
| 1250 gal × 4 | 3.0 years |
| 1250 gal × 6 | 2.0 years |
| 1500 gal × 2 | 7.0 years |
| 1500 gal × 4 | 3.5 years |
| 1500 gal × 6 | 2.5 years |

Adjustments:
- Garbage disposal → divide interval by 1.40
- Water softener → divide interval by 1.15

## What the .ics export looks like

A yearly-recurring event in standard iCalendar format. Imports into Google Calendar, Apple Calendar, Outlook.

## Source

- Texas A&M AgriLife Extension septic publications

**last_verified:** 2026-10-17

---

*Out West Septic — outwestseptic.com — TCEQ OSSF Installer I OS0041298 — Lone Camp, TX — 940.452.0598*