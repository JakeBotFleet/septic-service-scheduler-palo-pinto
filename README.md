# Texas Septic Maintenance Scheduler

> **Septic tank pump-interval scheduler with .ics calendar export.**
> Forked from the [texas-septic-toolkit](https://github.com/TexasSepticEnthusiast/texas-septic-toolkit).
> Built by [Out West Septic](https://outwestseptic.com) — Lone Camp, TX — **TCEQ OSSF Installer I | OS0041298** — 940.452.0598

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![TCEQ OSSF](https://img.shields.io/badge/TCEQ-OSSF_Installer_I-007787)](https://www.tceq.texas.gov/permitting/ossf)

## What this fork is

A focused fork of the [texas-septic-toolkit](https://github.com/TexasSepticEnthusiast/texas-septic-toolkit), containing only the maintenance scheduler. Use this to calculate pump intervals and export a `.ics` calendar reminder.

## Quick start

```bash
git clone https://github.com/TexasSepticEnthusiast/texas-septic-maintenance-scheduler.git
cd texas-septic-maintenance-scheduler
pip install icalendar
python scripts/outwestseptic_maintenance_scheduler.py 1250 4 --disposal --last-pumped 2024-06-01 --ics pump-reminder.ics
```

The `.ics` file imports into Google Calendar, Apple Calendar, or Outlook.

## What the script does

- Computes pump interval from tank size, household, garbage disposal, and water softener
- Returns the next pump due date based on the last pump date
- Exports an `.ics` calendar event with yearly recurrence

Out West Septic does NOT run a pump truck — we refer pumping to local pumpers. This script gives the homeowner a defensible "pump every N years" schedule.

## Service area

Out West Septic serves Palo Pinto, Hood, Erath, Stephens, Young, Jack, and Eastland counties. Mineral Wells, Graford, Possum Kingdom Lake.

## License

MIT — see [LICENSE](./LICENSE).

---

*Out West Septic — outwestseptic.com — 940.452.0598 — TCEQ OSSF Installer I OS0041298 — Lone Camp, TX*