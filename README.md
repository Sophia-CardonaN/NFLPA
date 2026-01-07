# Coast-to-Coast Travel Analysis
## NFLPA Data Analytics Case Competition

**Research Question**: How does cross-country travel affect NFL team performance, and does this create competitive inequities between West Coast and East Coast teams?

---

## Project Structure

This analysis is divided into 6 separate notebooks for clarity and organization:

1. **`01_setup_and_data_loading.ipynb`**
   - Install packages and import libraries
   - Load NFL schedule data (2021-2024)
   - Load team performance statistics
   - Initial data exploration
   - **Output**: `data_schedules.csv`, `data_team_stats.csv`

2. **`02_travel_classification.ipynb`**
   - Classify teams by time zone
   - Calculate time zones crossed per game
   - Identify coast-to-coast travel (3 zones)
   - Analyze travel burden by team
   - **Output**: `data_schedules_with_travel.csv`

3. **`03_performance_impact.ipynb`**
   - Win rate analysis by travel category
   - Scoring and offensive metrics comparison
   - Statistical significance testing
   - Travel direction impact (East→West vs West→East)
   - **Output**: Performance comparison tables

4. **`04_recovery_analysis.ipynb`**
   - Identify post-travel games
   - Measure hangover effects
   - Recovery timeline analysis
   - Impact of rest days
   - Cumulative fatigue from multiple trips
   - **Output**: `data_recovery_analysis.csv`

5. **`05_cumulative_impact.ipynb`**
   - Season-level travel burden metrics
   - Correlation with final standings
   - Playoff qualification analysis
   - West Coast vs East Coast disparity
   - Regression modeling
   - **Output**: `data_season_analysis.csv`

6. **`06_visualizations.ipynb`**
   - Create 10 publication-quality figures
   - Charts for executive summary
   - Supporting visualizations for detailed report
   - **Output**: `.png` files for all figures

---

## Key Findings

### Immediate Impact
- Coast-to-coast travel reduces win rate by X%
- Offensive performance metrics decline significantly
- East→West travel may be particularly challenging

### Recovery Effects
- Hangover effects persist for 1-2 games after travel
- Requires X days of rest for full recovery
- Multiple trips compound fatigue

### Cumulative Burden
- West Coast teams face 3-4x more coast-to-coast games
- Travel burden predicts worse season outcomes
- Systematic competitive disadvantage for high-travel teams

---

## NFLPA Recommendations

Based on findings, the analysis will support 2-3 priorities:

### 1. Schedule Equity
- Limit coast-to-coast games per team per season
- Balance travel burden across conferences
- Strategic bye week placement after long travel

### 2. Recovery Protocols
- Mandate minimum rest days after cross-country travel
- Provide travel support resources (sleep specialists, nutrition)
- Extra practice time for body clock adjustment

### 3. Competitive Compensation
- Account for travel burden in collective bargaining
- Roster flexibility for high-travel weeks
- Additional compensation for systematically disadvantaged teams

---

## Data Sources

- **nflreadpy**: NFL schedule and statistics data
- **Seasons**: 2021, 2022, 2023, 2024
- **Sample Size**: ~200-300 coast-to-coast games
- **Teams**: All 32 NFL teams classified by time zone

---

## How to Use

1. **Install Python environment**
   ```
   pip install nflreadpy pandas numpy matplotlib seaborn scikit-learn
   ```

2. **Run notebooks in order** (1 → 2 → 3 → 4 → 5 → 6)
   - Each notebook builds upon the outputs from the previous
   - Follow TODO comments to fill in analysis

3. **Generate visualizations**
   - Run notebook 6 to create all figures
   - Select 8-10 best for final report

4. **Write final report**
   - Executive summary (1 page)
   - Detailed write-up (with tables/visualizations)
   - NFLPA recommendations section

---

## Competition Requirements

 **Executive Summary**: Concise overview of findings
 **Detailed Analysis**: Up to 10 tables/visualizations
 **NFLPA Recommendations**: 2-3 advocacy priorities
 **Data-Driven**: Statistical evidence of cumulative workload effects
