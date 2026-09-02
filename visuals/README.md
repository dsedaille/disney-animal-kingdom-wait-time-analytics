# Visuals

This folder contains exported visualizations from the Disney Animal Kingdom Wait Time & Guest Experience Analytics project.

The charts were created in Python using the cleaned TouringPlans Animal Kingdom wait-time dataset. These visuals support the main notebook analysis and highlight attraction-level wait-time pressure, high-wait risk, and time-based guest experience patterns.

## Included Visuals

- `average_posted_wait_time_by_attraction.png`  
  Shows the average posted wait time for each Animal Kingdom attraction. This visual highlights Avatar Flight of Passage and Na'vi River Journey as the highest wait-time pressure points.

- `high_wait_rate_by_attraction.png`  
  Shows the percentage of valid posted wait-time records where each attraction had a wait of 45 minutes or more.

- `high_wait_records_by_attraction.png`  
  Shows the total number of high-wait records for each attraction. This helps identify attractions that contributed the largest volume of long-wait observations.

- `average_posted_wait_time_by_hour.png`  
  Shows how average posted wait times changed throughout the day during typical operating hours.

- `average_posted_wait_time_by_day_of_week.png`  
  Shows average posted wait times by day of week to evaluate whether weekday or weekend patterns affected guest wait experience.

- `average_posted_wait_time_by_month.png`  
  Shows average posted wait times by month to identify seasonal wait-time patterns.

## Notes

A high-wait record is defined as a valid posted wait-time record of 45 minutes or more.

The visuals focus primarily on posted wait times because posted wait-time data was available for most records, while actual wait-time data was only available for a smaller subset and was not paired with posted wait times in the same rows.
