# Student Performance Analysis

Short summary  
Exploratory Data Analysis (EDA) of student performance (math, science, english, overall). The notebook cleans the data, creates intervention flags, and produces plots and summary insights.

Project structure
- code/Student_analysis.ipynb — main notebook (EDA, feature engineering, plots)
- Student_Performance.csv — raw dataset
- Student_Performance_Cleaned.csv — cleaned dataset (output)
- LICENSE

Quick start (Windows)
1. python -m venv .venv
2. .venv\Scripts\activate
3. pip install -r requirements.txt  # or: pip install pandas numpy matplotlib seaborn scipy jupyter
4. jupyter notebook code/Student_analysis.ipynb

What I did
- Data cleaning: dropped duplicates, removed a mislabeled study method row ("not es").
- Feature engineering:
  - `Final_Decision`: Pass/Fail from `final_grade` (a–d → Pass, e–f → Fail).
  - `Excluded`: attendance < 75% flag.
  - `Catch-up_Sessions`: `final_grade == 'e'` OR `overall_score <= 60` flag.
  - Converted categorical columns to `category` dtype.
- Visualizations: pie charts, bar charts, boxplots, histograms, and correlation heatmaps.
- Saved cleaned dataset to `Student_Performance_Cleaned.csv`.

Key findings
- No large gender gap in overall scores (medians and IQRs similar).
- Score distribution is unimodal with a small lower tail — a subset may need support.
- Strong positive correlation across subjects (math, science, english).
- Study hours correlate positively with overall score.
- Extra activities and study-method counts show no obvious negative effect; further testing needed.

Fixes & notes
- Use elementwise OR (`|`) for Series comparisons (for `Catch-up_Sessions`).
- Pass subplot axes to seaborn with `ax=...` to render subplots correctly.
- Use proportions and statistical tests (chi-square, ANOVA, t-test) when comparing groups.

Next steps
- Run statistical tests for significance and control for confounders.
- Profile and investigate outliers; refine intervention criteria.
- Optionally build a simple predictive model to flag at-risk students and add automated checks (requirements.txt, CI).

If you want, I can commit this update and add a requirements.txt file.// filepath: c:\Users\PC\Documents\GitHub\Student-Preformance-Analysis\README.md
# Student Performance Analysis

Short summary  
Exploratory Data Analysis (EDA) of student performance (math, science, english, overall). The notebook cleans the data, creates intervention flags, and produces plots and summary insights.

Project structure
- code/Student_analysis.ipynb — main notebook (EDA, feature engineering, plots)
- Student_Performance.csv — raw dataset
- Student_Performance_Cleaned.csv — cleaned dataset (output)
- LICENSE

Quick start (Windows)
1. python -m venv .venv
2. .venv\Scripts\activate
3. pip install -r requirements.txt  # or: pip install pandas numpy matplotlib seaborn scipy jupyter
4. jupyter notebook code/Student_analysis.ipynb

What I did
- Data cleaning: dropped duplicates, removed a mislabeled study method row ("not es").
- Feature engineering:
  - `Final_Decision`: Pass/Fail from `final_grade` (a–d → Pass, e–f → Fail).
  - `Excluded`: attendance < 75% flag.
  - `Catch-up_Sessions`: `final_grade == 'e'` OR `overall_score <= 60` flag.
  - Converted categorical columns to `category` dtype.
- Visualizations: pie charts, bar charts, boxplots, histograms, and correlation heatmaps.
- Saved cleaned dataset to `Student_Performance_Cleaned.csv`.

Key findings
- No large gender gap in overall scores (medians and IQRs similar).
- Score distribution is unimodal with a small lower tail — a subset may need support.
- Strong positive correlation across subjects (math, science, english).
- Study hours correlate positively with overall score.
- Extra activities and study-method counts show no obvious negative effect; further testing needed.

Fixes & notes
- Use elementwise OR (`|`) for Series comparisons (for `Catch-up_Sessions`).
- Pass subplot axes to seaborn with `ax=...` to render subplots correctly.
- Use proportions and statistical tests (chi-square, ANOVA, t-test) when comparing groups.
