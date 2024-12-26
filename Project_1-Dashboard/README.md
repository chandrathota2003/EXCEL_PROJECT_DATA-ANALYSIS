# Excel Salary Dashboard

![1_Salary_Dashboard.png](/C:\Users\Chandu\OneDrive\Pictures\Screenshot
## Introduction

This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated. 

The data is from my Excel course, which provides a foundation in analyzing data using this powerful tool. The data contains detailed information on job titles, salaries, locations, and essential skills that are presented here.

### Dashboard File
My final dashboard is in [1_Salary_Dashboard.xlsx](1_Salary_Dashboard.xlsx).

### Excel Skills Used

The following Excel skills were utilized for analysis:

- Charts
- Formulas and Functions
- Data Validation

### Data Jobs Dataset

The dataset used for this project contains real-world data science job information from 2023. The dataset is available via my Excel course, which provides a foundation for analyzing data using Excel. It includes detailed information on:

- Job titles
- Salaries
- Locations
- Skills

## Dashboard Build

### Charts

#### Data Science Job Salaries - Bar Chart

**Excel Features:** 
- Utilize the bar chart feature with formatted salary values.
- Optimize the layout for clarity.

**Design Choice:** 
- Use horizontal bar charts for visual comparison of median salaries.

**Data Organization:** 
- Sort job titles by descending salary for improved readability.

**Insights Gained:** 
- Identify salary trends, noting that senior roles and engineers are higher-paying than analyst roles.

#### Country Median Salaries - Map Chart

**Excel Features:** 
- Utilize Excel's map chart feature to plot median salaries globally.

**Design Choice:** 
- Use color-coded maps to visually differentiate salary levels across regions.

**Data Representation:** 
- Plot median salary for each country with available data.

**Visual Enhancement:** 
- Improve readability and immediate understanding of geographic salary trends.

**Insights Gained:** 
- Quickly grasp global salary disparities and highlight high/low salary regions.

### Formulas and Functions

#### Median Salary by Job Titles

```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

**Multi-Criteria Filtering:** 
- Check job title, country, schedule type, and exclude blank salaries.

**Array Formula:** 
- Utilize `MEDIAN()` function with nested `IF()` statement to analyze an array.

**Tailored Insights:** 
- Provide specific salary information for job titles, regions, and schedule types.

**Formula Purpose:** 
- Populate the table below, returning the median salary based on job title, country, and type specified.

#### Count of Job Schedule Type

```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

**Unique List Generation:** 
- Use the `FILTER()` function to exclude entries containing "and" or commas and omit zero values.

**Formula Purpose:** 
- Populate the table below, providing a list of unique job schedule types.

### Data Validation

#### Filtered List

**Enhanced Data Validation:** 
- Implement the filtered list as a data validation rule under the `Job Title`, `Country`, and `Type` options in the Data tab.

- Restrict user input to predefined, validated schedule types.
- Prevent incorrect or inconsistent entries.
- Enhance overall usability of the dashboard.

## Conclusion

This dashboard showcases insights into salary trends across various data-related job titles. Utilizing data from my Excel course, the dashboard allows users to make informed decisions about their career paths and understand how location and job type influence salaries. This project aims to provide practical guidance for job seekers and professionals in the data science field.
