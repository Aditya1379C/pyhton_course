# 1. Most Demanded Skills for Top Data Roles in India

## Overview
This project analyses the most in-demand skills for the top 3 data roles in India's job market, using real-world job posting data. The goal is to identify which skills appear most frequently and what percentage of job postings request them.

## Methodology
1. **Clean skills column** — convert string representations of lists into actual list objects
2. **Explode skills** — expand each skill into its own row for analysis
3. **Count skills** — group by job title and skill, count occurrences
4. **Calculate percentages** — divide skill count by total job postings per role
5. **Visualise** — plot top 5 skills per role as horizontal bar charts

## Key Findings

### Skill Counts
![Counts of Skills Requested in IN Job Postings](images/skill_counts.png)

### Skill Likelihood
![Likelihood of Skills Requested in IN Job Postings](images/skill_likelihood.png)

| Role | Top Skill | % of Job Postings |
|---|---|---|
| Data Analyst | SQL | 52% |
| Data Engineer | SQL | 68% |
| Data Scientist | Python | 70% |

- **SQL and Python dominate** across all three roles
- **Data Engineers** additionally need cloud skills — Spark (38%), AWS (37%), Azure (36%)
- **Data Analysts** are the only role where Excel (35%) and Power BI (21%) feature prominently
- **Data Scientists** are the only role where R (33%) appears in the top 5

## Libraries Used
```python
import ast
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
from datasets import load_dataset
```

## How to Run
1. Install dependencies:
```bash
pip install pandas matplotlib seaborn datasets
```
2. Open `2_Skill_Demand.ipynb` in Jupyter or VS Code
3. Run all cells in order
