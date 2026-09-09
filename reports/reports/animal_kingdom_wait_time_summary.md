# Disney Animal Kingdom Wait Time & Guest Experience Analytics Report

## Executive Summary

This project analyzed Disney Animal Kingdom attraction wait-time data to identify guest experience pressure points, time-based wait-time patterns, and potential operational improvements.

The analysis found that wait-time pressure was concentrated around a small number of high-demand attractions, especially Avatar Flight of Passage and Na'vi River Journey. Wait-time pressure also varied by time of day and month, with posted waits peaking around midday and December showing the highest monthly average wait time.

In addition to descriptive analysis, this project used SQL to validate key wait-time patterns and built a scenario simulation to estimate how adding a new attraction could reduce long-wait exposure by redistributing demand away from the park's highest-pressure attractions.

## Business Problem

Theme parks rely on attraction wait-time data to understand guest experience, crowd flow, and operational pressure. Long posted wait times can negatively affect guest satisfaction, reduce flexibility in park planning, and create bottlenecks around specific attractions.

This project focuses on the following business question:

**How can wait-time data help identify guest experience pressure points and evaluate possible operational improvements at Disney Animal Kingdom?**

## Data Source

The project uses attraction-level wait-time data from the TouringPlans Disney Animal Kingdom Wait Times dataset.

The raw data is organized by attraction-level CSV files. These files were combined into one analysis-ready dataset and cleaned for analysis.

Invalid posted wait-time values, such as `-999`, were flagged and excluded from standard wait-time calculations because they represent unavailable or offline attraction records rather than true guest wait times.

## Methodology

The project included three main analysis components:

1. **Python data cleaning and analysis**  
   The raw attraction-level CSV files were combined, cleaned, and analyzed using Python. New fields were created for attraction names, cleaned wait times, time periods, wait-time categories, and high-wait indicators.

2. **SQL wait-time analysis**  
   The cleaned dataset was loaded into SQLite and queried using SQL. SQL was used to calculate overall KPIs, attraction-level summaries, high-wait record counts, and time-based wait-time patterns.

3. **Scenario simulation**  
   A demand redistribution simulation was created to estimate how adding a new attraction could reduce high-wait exposure. The simulation tested 5%, 10%, 15%, and 20% redistribution scenarios among the highest-pressure attractions.

## Key Metrics

A **high-wait record** was defined as a valid posted wait-time record of **45 minutes or more**.

Key overall metrics included:

- **Valid posted wait-time records:** 1,758,656
- **Average posted wait time:** 30.52 minutes
- **High-wait records:** 388,915
- **Overall high-wait rate:** 22.11%
- **Maximum posted wait time:** 390 minutes

## Key Findings

### 1. Wait-time pressure was concentrated around Pandora attractions

Avatar Flight of Passage had the highest average posted wait time at approximately 136 minutes. It also had a high-wait rate of 99.20%, meaning nearly every valid posted wait-time record was 45 minutes or longer.

Na'vi River Journey had the second-highest average posted wait time at approximately 75 minutes and a high-wait rate of 85.11%.

Together, these attractions represented the clearest guest experience pressure points in the dataset.

### 2. DINOSAUR created a large volume of high-wait records

Although DINOSAUR had a lower average posted wait time than Na'vi River Journey, it ranked second in total high-wait records. This shows why both rate-based and volume-based metrics are useful.

High-wait rate shows how frequently an attraction reaches long-wait conditions, while high-wait record count shows the total volume of long-wait observations.

### 3. Wait-time pressure peaked around midday

Average posted waits were lowest in the early operating hours and increased sharply after 9 AM. The highest average posted wait time occurred around 12 PM.

This suggests that late morning through early afternoon was the most important period for guest experience monitoring and operational support.

### 4. Day of week was not a major driver

Average posted wait times were fairly consistent across the week. Saturday and Monday showed slightly higher average posted waits, while Wednesday had the lowest average wait.

However, the differences between days were relatively small compared with attraction-level and hour-of-day differences.

### 5. Seasonal patterns were visible

December had the highest average posted wait time and highest high-wait rate, while September had the lowest values.

This pattern suggests that holiday and vacation travel periods likely created higher guest experience pressure, while September represented a lower-pressure period in the dataset.

## Scenario Simulation Summary

The simulation estimated how adding a new attraction could reduce high-wait exposure by redistributing demand away from the highest-pressure attractions.

The target attractions included:

- Avatar Flight of Passage
- Na'vi River Journey
- DINOSAUR
- Expedition Everest
- Kali River Rapids

The simulation tested four demand redistribution scenarios:

| Scenario | Estimated Reduction in High-Wait Records | New High-Wait Rate |
|---|---:|---:|
| 5% redistribution | 16,444 | 21.18% |
| 10% redistribution | 32,887 | 20.24% |
| 15% redistribution | 49,331 | 19.30% |
| 20% redistribution | 65,774 | 18.37% |

The 10% scenario provides a useful moderate planning benchmark. Under this scenario, the model estimated approximately 32,887 fewer high-wait records and reduced the overall high-wait rate from 22.11% to 20.24%.

This does not predict exact future guest behavior. Instead, it provides a practical planning model for estimating how demand redistribution could reduce long-wait exposure.

## Business Recommendations

### 1. Prioritize operational planning around high-pressure attractions

Avatar Flight of Passage and Na'vi River Journey should be treated as primary guest experience risk areas because they consistently showed the highest wait-time pressure.

### 2. Use early-day strategies to distribute demand

Because wait times were lowest earlier in the day, guest communication tools could encourage visitors to experience high-demand attractions earlier before wait-time pressure peaks.

### 3. Monitor midday operations closely

Since wait-time pressure peaked around noon, late morning through early afternoon should be a priority period for staffing, queue management, and guest flow monitoring.

### 4. Use both rate and volume metrics

High-wait rate and high-wait record count should be evaluated together. This provides a more complete view of whether an attraction is consistently high-pressure, high-volume, or both.

### 5. Pair new attractions with guest flow strategies

A new attraction could reduce long-wait exposure, but it would not fully eliminate pressure at the highest-demand rides. New attraction investment should be paired with app messaging, signage, itinerary recommendations, and crowd-flow planning.

## Project Conclusion

This project shows how wait-time data can be used to identify guest experience pressure points, analyze operational patterns, and evaluate potential improvement strategies.

The analysis found that Animal Kingdom wait-time pressure was concentrated around a small number of attractions and peaked during specific time periods. The scenario simulation added a strategic planning layer by estimating how a new attraction could reduce long-wait exposure under different demand redistribution assumptions.

Together, the Python analysis, SQL analysis, and simulation model demonstrate how data analytics can support operational decision-making in a guest experience setting.
