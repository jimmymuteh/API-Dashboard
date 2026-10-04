# API Analytics Dashboard

A Python utility that fetches mock API data for member fitness metrics and course enrollments, prints an ASCII activity chart to the terminal, and exports the summary to `output.json`.

## Pipeline Overview

1. **Fetch Raw Data**: Calls mock endpoints for member tracking (`fetch_members`), 7-day step totals (`fetch_weekly_summary`), and skill enrollments (`fetch_active_skills`).
2. **Data Aggregation**:
   - Calculates step goal progress (>= 10,000 steps), sleep averages, and protocol split (OMAD vs 2MAD).
   - Identifies peak activity days across the week.
   - Ranks skills by total enrollment.
3. **Display & Export**: Prints formatted tables and ASCII bar graphs to the terminal, then writes the full report to `output.json`.

## Output Preview

- **Terminal Output**: Displays summary statistics and ASCII activity graphs.
- **JSON Export**: Saves aggregated results to `output.json`.

## Setup & Execution

```
python main.py
