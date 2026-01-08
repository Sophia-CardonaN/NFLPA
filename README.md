# Coast-to-Coast Travel Analysis
## NFLPA Data Analytics Case Competition

**Research Question:** Does cross-country travel create competitive inequities in the NFL?

---

## Analysis Overview

This study examines how 3-time-zone travel affects NFL performance using 4 seasons of data (2021-2024).

**Notebooks:**
1. **Setup & Data** - Load schedules and team stats from nflreadpy
2. **Travel Classification** - Map teams to time zones, identify coast-to-coast games
3. **Performance Impact** - Compare metrics during travel vs baseline
4. **Recovery Analysis** - Measure hangover effects and cumulative fatigue
5. **Cumulative Impact** - Season-level correlations and playoff analysis

---

## Key Findings

**Immediate Impact:**
- Rushing yards decrease during coast-to-coast travel (p=0.048)
- Win rate and other metrics show no significant effect

**Recovery Effects:**
- Hangover effect borderline (p=0.064) - teams perform worse in next game
- No evidence that rest days improve recovery
- Cumulative fatigue detectable but tiny (r=-0.052, p=0.012)


---

## Data Sources

**Primary:** nflreadpy library
- NFL schedules (2021-2024): game dates, teams, scores
- Weekly team stats: offensive/defensive performance metrics

**Derived:**
- Time zone mappings (Pacific, Mountain, Central, Eastern)
- Coast-to-coast flag (3 time zones crossed)

---

## Setup

- starting up a venv is reccomended for this step but not required
- to use simply run:

```bash
pip install -r "requirements.txt"
```

- Then run notebooks sequentially (01 → 05). Each generates CSV outputs used by later notebooks.