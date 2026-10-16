# CodeNova AI/ML Batch 01 — Task 1: Exploratory Data Analysis

## Project overview
This beginner-friendly EDA project profiles and cleans the public Titanic passenger dataset, visualizes numeric distributions and categorical counts, detects potential outliers using the IQR rule, computes a numeric correlation heatmap, and explores pairwise scatter plots. Each visualization is followed by an observation prompt or data-driven summary.

## Requirements
- Python 3
- pandas
- numpy
- matplotlib
- seaborn
- Jupyter Notebook or Google Colab

All tools are free. Google Colab is recommended for beginners because it runs in a browser.

## Dataset
The notebook loads the public Titanic CSV from:
https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv

An internet connection is needed to download the dataset when running the notebook.

## Run in Google Colab
1. Download `CodeNova_Task1_Exploratory_Data_Analysis.ipynb`.
2. Open https://colab.research.google.com/.
3. Choose **File → Upload notebook** and upload the `.ipynb` file.
4. Run cells in order from top to bottom using **Runtime → Run all**.
5. Review the printed observations and charts. Add your own final conclusions based on the actual outputs.
6. Run the last cell to create `codenova_task1_eda_outputs.zip`.
7. Download the output ZIP from Colab's Files panel if you want to include charts and CSV exports in your repository/report.

## Analysis workflow
1. Dataset ingestion and profiling: shape, data types, summary statistics, missing values and unique values.
2. Data cleaning:
   - Remove exact duplicate rows only.
   - Impute missing `Age` with medians grouped by passenger class and sex, then fall back to the overall median.
   - Fill missing `Embarked` values with the mode.
   - Exclude `Cabin` from the cleaned analysis because it is highly incomplete; the original data is preserved.
3. Visualizations: missingness bar chart, numeric histograms, categorical count plots, boxplots, correlation heatmap, pairwise scatter plots, and survival rate by passenger class.
4. Outlier detection: IQR fences flag potential outliers; the notebook does not automatically delete them.
5. Exports: high-resolution PNG figures (300 DPI), cleaned CSV, profiling CSV and outlier summary CSV.

## Important interpretation notes
- Imputation is a practical baseline, not a guarantee that filled values are correct.
- IQR outliers may be genuine observations and should not be removed without domain justification.
- Correlation does not prove causation.
- Titanic is a historical sample dataset; findings should not be generalized to all populations.
- Review the notebook output and write conclusions that are supported by the observed results.

## Repository structure
```text
codenova-task1-eda/
├── CodeNova_Task1_Exploratory_Data_Analysis.ipynb
├── README.md
└── eda_outputs/                 # generated when notebook runs
    ├── 01_missing_values.png
    ├── 02_distribution_*.png
    ├── 03_count_*.png
    ├── 04_boxplot_*.png
    ├── 05_correlation_heatmap.png
    ├── 06_pairwise_scatterplots.png
    ├── 07_survival_rate_by_class.png
    ├── titanic_cleaned.csv
    ├── final_data_profile.csv
    └── outlier_summary.csv
```

## Submission checklist
- [ ] Run every notebook cell successfully.
- [ ] Ensure outputs and charts are visible in the saved notebook.
- [ ] Read and personalize the conclusions based on your actual output.
- [ ] Include the notebook, README, exported figures and relevant CSV outputs in a public GitHub repository.
- [ ] Add a short project description and screenshots to the repository.
- [ ] Verify the repository is publicly accessible.
- [ ] Do not commit passwords, API keys or other secrets.

## Internship alignment
This project addresses the CodeNova Task 1 requirements: dataset ingestion and summary profiling, missing-value analysis, duplicate removal, outlier detection, correlation heatmap, feature distributions, boxplots, pairwise scatter plots, actionable observations, an executed notebook, exported visualization images and README documentation.
