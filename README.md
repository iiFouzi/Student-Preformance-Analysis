# Student Performance Analysis 🚀

**Short description:**
A concise exploratory data analysis (EDA) of student performance across subjects (math, science, english, overall). The analysis cleans the data, creates useful features, and produces visualizations and summary insights in `code/Student_analysis.ipynb`.

---

## Project structure 📁
- `code/Student_analysis.ipynb` — main notebook with EDA, feature engineering, and visualizations
- `Student_Performance.csv` — raw dataset
- `Student_Performance_Cleaned.csv` — cleaned dataset written by the notebook
- `LICENSE` — project license

---

## Quick start 🔧
1. Create and activate a Python environment (Windows):
   ```bash
   python -m venv .venv
   .venv\Scripts\activate
   pip install pandas numpy matplotlib seaborn scipy jupyter
   ```
2. Open and run the notebook:
   ```bash
   jupyter notebook code/Student_analysis.ipynb
   ```
3. The notebook saves a cleaned CSV to `Student_Performance_Cleaned.csv`.

---

## What I did (high level) ✨
- Data inspection and cleaning (missing values, duplicates).
- Feature engineering: `Final_Decision` (Pass/Fail), `Catch-up_Sessions` (Yes/No), `Excluded` (attendance < 75%).
- Visualizations: boxplots, histograms, pie charts, and heatmaps for correlations.
- Basic descriptive statistics and short interpretations.

---

## Key findings & insights 🔍
- **No large gender gap**: medians and IQRs for overall score are similar across genders — typical students have comparable performance by gender.
- **Overall distribution**: unimodal distribution with most students clustered in the middle–high score range and a small tail of lower scores (students who might benefit from targeted support).
- **Across-subject correlation**: students who do well in one subject tend to do well in others (positive correlations).
- **Study hours**: higher study hours generally associate with higher overall scores.

---

## Fixes & notes ✅
- Fixed plotting: explicitly pass subplot axes to seaborn (e.g., `ax=axes[0]`) so the boxplot now appears in the intended subplot.
- Fixed boolean bug when creating `Catch-up_Sessions`: use elementwise OR (`|`) for Series comparisons instead of Python `or`.

---

## Next steps 🔭
- Run statistical tests (t-test / Mann–Whitney) to confirm group differences.
- Inspect and profile outliers (attendance, study hours, sociodemographic features).
- Consider a simple predictive model to flag students who may need interventions.

---

If you'd like, I can add a `requirements.txt` and commit this `README.md` for you. Want me to do that? ✅

