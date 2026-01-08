# Coast-to-Coast Travel Analysis
## NFLPA Data Analytics Case Competition

Research Question: How does cross-country travel affect NFL team performance, and does this create competitive inequities between West Coast and East Coast teams?

---

## Project Structure

This analysis is organized into 5 notebooks:

1. 01_setup_and_data_loading.ipynb
   - Load NFL schedules (2021–2024) and weekly team stats via nflreadpy
   - Basic exploration and integrity checks
   - Outputs:
     - data_schedules.csv
     - data_team_stats.csv

2. 02_travel_classification.ipynb
   - Map teams to time zones (Pacific, Mountain, Central, Eastern)
   - Compute time zones crossed per game (tz_crossed)
   - Flag coast-to-coast games (3 zones)
   - Team burden summaries and visuals
   - Output:
     - data_schedules_with_travel.csv

3. 03_performance_impact.ipynb
   - Away win rate by travel category (0–3 zones) vs home baseline
   - Scoring and offensive metrics comparisons with t-tests
   - Directional analysis (East→West vs West→East)
   - Outputs:
     - performance_comparison.csv
     - statistical_tests.csv
     - direction_comparison.csv

4. 04_recovery_analysis.ipynb
   - Identify games following C2C travel (hangover effects)
   - Recovery timeline (Baseline, During C2C, 1 Game After)
   - Rest-days impact and recent multiple-trip fatigue
   - Outputs:
     - recovery_timeline.csv
     - rest_days_analysis.csv
     - cumulative_fatigue.csv

5. 05_cumulative_impact.ipynb
   - Season-level travel metrics (c2c_games, total_tz, avg_tz, max_tz)
   - Correlations with win%, points, point differential
   - Playoff qualification analysis and coast disparities
   - Simple regression (win% ~ C2C games)
   - Outputs:
     - season_analysis.csv
     - coast_comparison.csv
     - correlations.csv

---

## Current Findings

- 03 · Game-level performance (C2C vs home/other away)
  - Tested: win rate, scoring/offensive metrics (see statistical_tests.csv).
  - Significant at p < 0.05:
    - Rushing Yards: lower in C2C away games (p ≈ 0.0479).
  - Not significant in current run:
    - Other tested metrics (e.g., points, passing yards, turnovers, third downs, etc.) did not reach p < 0.05. See statistical_tests.csv for exact p-values.

- 03 · Directional effects (East→West vs West→East)
  - Tested: descriptive comparisons (direction_comparison.csv).
  - Status: differences summarized descriptively; no formal significance tests in-code.

- 05 · Playoffs and season aggregates
  - Tested: Playoff qualification vs travel burden.
    - Result: Playoff teams averaged slightly more C2C games (~0.83) than non-playoff teams (~0.74); small difference. T-test result printed; not compelling evidence that travel prevented playoff qualification.
---

## How to Run

1. Install dependencies (Windows/PowerShell):
   ```
   pip install nflreadpy pandas numpy matplotlib seaborn scikit-learn scipy pyarrow
   ```
2. Run notebooks in order (1 -> 5). Each notebook reads prior outputs.
3. Review generated CSVs:
   - performance_comparison.csv, statistical_tests.csv, direction_comparison.csv
   - recovery_timeline.csv, rest_days_analysis.csv, cumulative_fatigue.csv
   - season_analysis.csv, coast_comparison.csv, correlations.csv

---

## Data Sources

- nflreadpy (schedules and weekly team stats), seasons 2021–2024