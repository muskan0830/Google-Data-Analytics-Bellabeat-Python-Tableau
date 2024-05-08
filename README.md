<a href="https://public.tableau.com/app/profile/muskan.kashyap/viz/BellabeatDashboardGoogleDataAnalyticsCapstone/PhysicalActivity"> [Access My Dashboard from Here!] </a>

# PYTHON
# Bellabeat Fitness Tracker Data Analysis

## Introduction
This repository presents a comprehensive analysis of the Bellabeat fitness tracker data. The analysis encompasses cleaning, manipulation, exploration, and interpretation of various datasets related to daily activity, heart rate, hourly data, minute data, and sleep patterns. The primary objective is to derive meaningful insights to understand user behavior and inform decision-making for product enhancement and marketing strategies.

## Data Cleaning and Transformation
The initial phase involved loading multiple CSV files containing data for two time periods: March-April and April-May. Each dataset underwent cleaning and transformation to ensure consistency and prepare them for analysis. This process included importing necessary libraries, handling data types, addressing missing values, and merging datasets for comprehensive analysis.

## Statistical Summary
Statistical summaries were generated for key datasets, providing insights into the central tendency and dispersion of variables. These summaries aided in understanding the overall distribution of data and identifying potential outliers.

## Data Exploration and Visualization
Exploratory data analysis (EDA) was conducted to uncover patterns, trends, and relationships within the data. Visualization techniques such as line graphs and heatmaps were employed to illustrate these findings. Notable analyses include daily activity trends, heart rate patterns, hourly data exploration, and minute-level analysis of calorie expenditure and sleep patterns.

## Insights and Interpretation
The analysis provided insights into daily activity levels, heart rate patterns, and sleep quality. Correlation analysis explored relationships between variables, while cross-analysis provided comprehensive insights into user behavior. These findings can inform product development, marketing strategies, and user engagement initiatives for Bellabeat.

## Conclusion
The analysis of Bellabeat fitness tracker data offers valuable insights into user behavior and activity patterns. These insights can drive data-driven decision-making and innovation to enhance the overall user experience. Further analysis and exploration may uncover additional insights, contributing to continuous improvement and innovation in fitness tracking technology.


# TABLEAU

**Health Analytics Dashboard with Tableau**

## Introduction:
This project aims to create a comprehensive health analytics dashboard using Tableau, integrating data from Bellabeat, a health and wellness company. The dashboard will provide insights into physical activity, heart health, and sleep analysis based on the collected data.

## Data Preparation:
1. **Import and Clean Data:** Six cleaned files obtained after Python analysis will be imported into Tableau. These files include data on physical activity, heart rate, and sleep duration.
2. **Column Name Standardization:** Column names will be standardized across files. For instance, in the 'heartrate_seconds' file, the column 'value' will be renamed to 'heart_rate', and in the 'minute_sleep' file, 'Value' will be renamed to 'SleepStages'.

3. **Creating Groups for Time of Day**

In the Tableau environment, we'll create groups for different times of the day based on the 'hour of the day' column from the 'heartrate_seconds' and 'minute_sleep' files.

a. Make sure you are connected to the respective data sources containing the 'heartrate_seconds' and 'minute_sleep' datasets.

b. **Select the 'Hour of the Day' Column:** Navigate to the 'Data' pane and locate the 'hour of the day' column in both datasets.

c. **Create Group for 'heartrate_seconds' File:**
   - Right-click on the 'hour of the day' column in the 'heartrate_seconds' dataset.
   - From the context menu, select 'Create' and then 'Group'.

d. **Define Groupings:**
   - In the Group dialog box, define the groupings as follows:
     - 6-12: Morning
     - 13-16: Afternoon
     - 17-20: Evening
     - Rest: Night (This will include all remaining hours)

e. **Apply Grouping:** Click 'OK' to apply the groupings. Tableau will create a new calculated field representing the time of day groups based on the 'hour of the day' column.

f. **Repeat Steps 3-5 for 'minute_sleep' File:** Follow the same procedure to create time of day groups for the 'minute_sleep' dataset.

4. **Creating Groups for Sleep Stages**

For the 'minute_sleep' file, we'll create groups for different sleep stages based on the 'SleepStages' column.

a. **Select the 'SleepStages' Column:** Navigate to the 'Data' pane and locate the 'SleepStages' column in the 'minute_sleep' dataset.

b. **Create Group:**
   - Right-click on the 'SleepStages' column.
   - From the context menu, select 'Create' and then 'Group'.

c. **Define Groupings:**
   - In the Group dialog box, define the groupings as follows:
     - 1: Awake
     - 2: Light Sleep
     - 3: Deep Sleep

5. **Creating Calculated Fields for Sleep Duration**

a. **Create Calculated Field - Total Time In Bed:**
   - Go to the 'Analysis' menu and select 'Create Calculated Field'.
   - Name the calculated field 'Total Time In Bed'.
   - Enter the formula to sum the columns representing different sleep stages:
     ```
     [Awake] + [Light Sleep] + [Deep Sleep]
     ```

6. **Create Calculated Field - Total Sleep:**
   - Follow the same procedure as above to create a calculated field named 'Total_Sleep'.
   - Enter the formula to sum the columns 'Light Sleep' and 'Deep Sleep':
     ```
     [Light Sleep] + [Deep Sleep]
     ```

7. **Create Calculated Field - Sleep Efficiency:**
   - Create another calculated field named 'Sleep Efficiency'.
   - Enter the formula to calculate sleep efficiency:
     ```
     ({Total Sleep} / {Total Time In Bed}) * 100
     ```

8. **Repeat Steps 5-7 for 'sleep_duration_weekdays' File**

Follow the same process outlined in Steps 5-7 for the 'sleep_duration_weekdays' dataset to create calculated fields for sleep duration analysis.

## Data Visualization:

**Physical Activity Dashboard:**
1. **Key Performance Indicator (KPI) 1:** Average daily steps will be visualized using a card and a line chart.
2. **KPI 2:** Average daily total distance will be visualized using a card and a line chart.
3. **KPI 3:** Average sedentary minutes will be visualized using a card.
4. **KPI 4:** Average "very active minutes" will be visualized using a card.
5. **Dual Axis Chart:** A dual-axis chart (column and line) will be created to visualize the average calories burned and sedentary minutes over weekdays, as well as the average total distance and very active minutes over weekdays.

**Heart Health Dashboard:**
1. **KPI 1:** Hourly average heart rate will be visualized using a card and a line chart.
2. **KPI 2:** Hourly average total steps will be visualized using a card and a line chart.
3. **KPI 3:** Hourly average total calories burned will be visualized using a card.
4. **KPI 4:** Hourly average of total intensity will be visualized using a card.
5. **Dual Axis Chart:** A dual-axis chart (column and line) will be created to visualize the average heart rate and calories burned, as well as the average heart rate and total intensity.

**Sleep Analysis Dashboard:**
1. **KPI 1:** Average sleep efficiency by hour will be visualized using a card and a line chart.
2. **KPI 2:** Average sleep efficiency by weekdays will be visualized using a card and a line chart.
3. **Multiple Line Chart:** A multiple line chart will be created to analyze the pattern of hourly variation in sleep stages.
4. **Pie Chart:** A pie chart will be created to analyze the distribution of sleep stages.

**Additional Features:**
- All visuals will be kept floating for flexible layout.
- Navigation buttons will be inserted for seamless navigation between the three dashboards.

**Analysis Results:**

**Physical Activity:**
- Average daily total steps: 7281, with Sunday having the lowest average (6607) and Saturday having the highest (7752).
- Average calories burned and sedentary minutes show consistent patterns across each day.
- Monday and Saturday recorded the highest total distance and average "very active" minutes.

**Heart Health:**
- Hourly average heart rate: 78.10
- Hourly average total steps: 302.5
- Afternoon has the highest average heart rate (75.2), while night has the lowest (64.7).
- Average total intensity is highest in the evening (16) and lowest at night (2.1).

**Sleep Analysis:**
- Average sleep efficiency by hour: 11.89 people have efficient sleep on average.
- Average sleep efficiency by weekdays: 8 people have efficient sleep on average.
- Distribution of sleep stages: 84% awake, 13% in light sleep, and 3% in deep sleep.
- Hourly variation in sleep stages: Most people are awake in the middle of the night, in light sleep in the early morning, and in deep sleep after 10 PM.

**Conclusion:**
This Tableau dashboard provides valuable insights into physical activity, heart health, and sleep analysis, enabling users to track their health metrics effectively and make informed decisions for improved well-being.
