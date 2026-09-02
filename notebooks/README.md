# Notebooks

This folder contains the main analysis notebooks for the Disney Animal Kingdom Wait Time & Guest Experience Analytics project.

## Included Notebooks

### `01_data_cleaning_and_wait_time_analysis.ipynb`

This notebook performs the main Python analysis for the project. It loads and combines multiple attraction-level CSV files, cleans invalid wait-time records, maps source file codes to readable attraction names, creates guest experience KPI fields, and analyzes posted wait-time patterns across attractions and time periods.

Key steps include:

- Loading raw attraction-level CSV files
- Combining files into one analysis-ready dataset
- Mapping attraction codes to attraction names
- Cleaning invalid wait-time values such as `-999`
- Creating time-based fields such as hour, day of week, and month
- Creating guest experience KPI fields
- Analyzing average posted wait times by attraction
- Analyzing high-wait rates and high-wait record counts
- Identifying hourly, weekly, and monthly wait-time patterns
- Summarizing key findings and business recommendations

## Notes

The raw CSV files are not included directly in this repository because some files are too large for standard GitHub browser upload. To reproduce the notebook, download the original dataset from the TouringPlans Disney Animal Kingdom Wait Times source repository and place the attraction-level CSV files in the local `data/raw/` folder.

The cleaned dataset may also be too large for GitHub upload. The notebook includes an optional export step so the cleaned file can be saved locally.

## Planned Notebooks

Future notebooks may include:

- `02_sql_wait_time_analysis.ipynb`
- `03_wait_time_prediction_model.ipynb`
