# 1. Most Demanded Skills for Top Data Roles in India

## Overview
This project analyses the most in-demand skills for the top 3 data roles in India's job market, using real-world job posting data. The goal is to identify which skills appear most frequently and what percentage of job postings request them.

## Methodology
1. **Clean skills column** — convert string representations of lists into actual list objects
2. **Explode skills** — expand each skill into its own row for analysis
3. **Count skills** — group by job title and skill, count occurrences
4. **Calculate percentages** — divide skill count by total job postings per role
5. **Visualise** — plot top 5 skills per role as horizontal bar charts using seaborn library.

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

# 2. Trend Analysis for In-demand skills in India

## Overview
This project analyzes the monthly demand for various data analytics skills within the data analyst job market in India . By assessing how the likelihood of specific skills appearing in job postings changes over time, this analysis provides insights for data professionals looking to align their skill sets with current market demands in the region .

## Methodology
The analysis was executed through the following structured process:
* **Data Acquisition & Cleaning:** Raw job posting data was retrieved from the Hugging Face `datasets` library via `lukebarousse/data_jobs` . Dates were cast into pandas datetime formats, and stringified skill arrays were securely converted into Python lists utilizing the `ast` library .
* **Data Filtering:** The dataset was filtered to include only postings where the `job_title` matches 'Data Analyst' and the `job_country` is strictly 'India' .
* **Aggregation:** Data entries were grouped by their posting month, and the list of skills was exploded to allocate an individual row to each skill . A pivot table was then generated to aggregate raw monthly frequencies .
* **Normalization:** Raw metrics were normalized into monthly percentages by dividing specific skill occurrences by the aggregate volume of data analyst openings for each respective month .
* **Visualization:** Data trends for the top five skills were plotted longitudinally across 12 months using `matplotlib` and `seaborn` .

## Visualizations
### Counts of Skills Requested
![Counts of Postings per month for the specified skill](images/skill_count.png)

### Skill Likelihood Trend
![Percentage of Postings per month for the specified skill](images/Skill_percent.png)

## Key Findings
* **Predominance of SQL:** Structured Query Language (SQL) consistently establishes itself as the primary programmatic prerequisite, appearing in **52% to 69%** of regional job postings over the tracked lifecycle .
* **High Demand for Python and Excel:** Python and Excel contend closely for the secondary position, with Python peaking around **45%** and Excel spiking to nearly **58%** of total listings in specific months .
* **Primary Technical Proficiencies:** The five most frequently demanded skills within the dataset are SQL, Python, Excel, Tableau, and Power BI .
* **Stable Market Requirements:** The underlying demand framework remains highly resilient. Data visualization tools (Tableau and Power BI) maintain strong and consistent inclusion, appearing in **18% to 41%** of job postings .

## Libraries
* `pandas`: Data cleaning, formatting, and mathematical pivoting .
* `matplotlib.pyplot` & `seaborn`: Data visualization, line-chart generation, and axis formatting .
* `datasets`: Remote dataset ingestion from Hugging Face .
* `ast`: Literal string-to-list evaluation .
"""

## How to run
* with open("README_India.md", "w") as f:
    f.write(readme_content_india)
