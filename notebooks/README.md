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

### `02_sql_wait_time_analysis.ipynb`

This notebook uses SQLite and SQL queries to analyze the cleaned Disney Animal Kingdom wait-time dataset. It builds on the cleaned dataset created in the first Python notebook and demonstrates how SQL can be used to answer business questions about attraction wait-time pressure, high-wait risk, and time-based guest experience patterns.

Key steps include:

- Loading the cleaned Animal Kingdom wait-time dataset
- Creating a SQLite database connection
- Writing the cleaned dataset to a SQL table
- Inspecting the SQL table structure
- Calculating overall wait-time KPIs
- Analyzing average posted wait times by attraction
- Ranking attractions by high-wait record volume
- Analyzing posted wait-time patterns by hour of day
- Comparing wait-time patterns by day of week
- Identifying monthly and seasonal wait-time patterns
- Summarizing SQL-based key findings

### `03_wait_time_pressure_simulation.ipynb`

This notebook simulates how adding a new attraction could reduce guest experience pressure at Disney Animal Kingdom by redistributing a percentage of high-wait demand away from the park's highest-pressure attractions.

The goal of this notebook is not to predict exact future wait times, but to model possible operational impact under different demand redistribution scenarios.

Key steps include:

- Loading the cleaned Animal Kingdom wait-time dataset
- Defining baseline high-wait pressure
- Identifying target attractions for demand redistribution
- Building 5%, 10%, 15%, and 20% redistribution scenarios
- Estimating reductions in high-wait records
- Comparing simulated high-wait rates against the baseline
- Analyzing attraction-level impact under the 10% scenario
- Visualizing estimated scenario impact
- Summarizing key findings and business recommendations

## Notes

The raw CSV files are not included directly in this repository because some files are too large for standard GitHub browser upload. To reproduce the notebook, download the original dataset from the TouringPlans Disney Animal Kingdom Wait Times source repository and place the attraction-level CSV files in the local `data/raw/` folder.

The cleaned dataset may also be too large for GitHub upload. The notebook includes an optional export step so the cleaned file can be saved locally.

## Included Notebooks

### `01_data_cleaning_and_wait_time_analysis.ipynb`

Loads and combines attraction-level CSV files, cleans wait-time data, creates guest experience KPI fields, analyzes attraction-level and time-based wait-time patterns, and summarizes business recommendations.

### `02_sql_wait_time_analysis.ipynb`

Uses SQLite and SQL queries to analyze the cleaned Animal Kingdom wait-time dataset. This notebook calculates overall KPIs, attraction-level wait-time summaries, high-wait record counts, hourly wait-time patterns, day-of-week trends, and monthly seasonal patterns.

### `03_wait_time_pressure_simulation.ipynb`

Scenario simulation notebook that estimates how adding a new attraction could reduce high-wait exposure by redistributing demand away from the park's highest-pressure attractions.
