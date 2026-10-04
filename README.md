# API Analytics Dashboard

A Python analytics application that consumes multi-endpoint mock API data, aggregates member fitness and skill metrics, visualizes weekly activity via terminal bar graphs, and exports summarized analytics to structured JSON payload files.

---

## Core Architecture & Pipeline Steps

The application processes data through three distinct architectural stages:

### Step 1: Preview All Three Endpoints
Fetches raw data structures from mock API functions:
* **`fetch_members()`**: Individual fitness tracking data (steps, fasting protocols, sleep hours, cold shower adherence).
* **`fetch_weekly_summary()`**: Daily total step aggregations across a 7-day period (`2024-W47`).
* **`fetch_active_skills()`**: Skill enrollment records and instructor assignments.

### Step 2: Process Endpoint Datasets
Calculates summary statistics using optimized Python data structures and algorithms:
* **`process_members()`**: Computes step goal achievement ratios ($\ge 10,000$ steps), average daily activity, cold shower counts, protocol breakdowns (`OMAD` vs `2MAD`), and top performer identification.
* **`process_weekly()`**: Identifies peak activity days, computes total volume, and calculates weekly daily averages.
* **`process_skills()`**: Ranks skill popularity by enrollment counts and computes total active course numbers.

### Step 3: Terminal Display & JSON Serialization
Renders formatted summaries and ASCII bar charts directly to the terminal, and saves a serialized `output.json` export file.