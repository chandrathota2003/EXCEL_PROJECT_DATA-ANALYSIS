# Project 2 Analysis

## Introduction

As a former job seeker, I’ve always been curious about the data science job market, especially the skills top employers request and how to achieve higher pay. This project aims to analyze the most optimal jobs and skills in the data science market.

### Questions to Analyze

1. Do more skills get you better pay?
2. What’s the salary for data jobs in different regions?
3. What are the top skills of data professionals?
4. What’s the pay for the top 10 skills?

### Excel Skills Used

- Pivot Tables
- Pivot Charts
- DAX (Data Analysis Expressions)
- Power Query
- Power Pivot

### Data Jobs Dataset

The dataset used contains real-world data science job information from 2023, including job titles, salaries, locations, and skills.

## Analysis Steps

### 1. Do more skills get you better pay?

#### Skill: Power Query (ETL)

**Extract**
- Extract the original data (`data_salary_all.xlsx`) and create two queries:
  - One with all the data jobs information.
  - Another listing the skills for each job ID.

**Transform**
- Transform each query by changing column types, removing unnecessary columns, and cleaning text.

**Load**
- Load both transformed queries into the workbook.

**Analysis**
- Use PivotTables to analyze the correlation between the number of skills and the median salary.

### 2. What’s the salary for data jobs in different regions?

#### Skills: PivotTables & DAX

**Pivot Table**
- Create a PivotTable using the Data Model.
- Move `job_title_short` to the rows area and `salary_year_avg` into the values area.

**DAX**
- Use DAX to calculate the median salary:
  ```
  Median Salary := MEDIAN(data_jobs_all[salary_year_avg])
  ```

**Analysis**
- Compare median salaries for data jobs in different regions.

### 3. What are the top skills of data professionals?

#### Skill: Power Pivot

**Data Model**
- Create a data model by integrating the `data_jobs_all` and `data_jobs_skills` tables.

**Relationship**
- Establish a relationship between the two tables using the `job_id` column.

**Analysis**
- Use PivotTables to identify top skills in data-related jobs.

### 4. What’s the pay of the top 10 skills?

#### Skill: Advanced Charts (Pivot Chart)

**PivotChart**
- Create a combo PivotChart to plot median salary and skill likelihood from the PivotTable.
  - Primary Axis: Median Salary
  - Secondary Axis: Skill Likelihood

**Analysis**
- Identify higher median salaries associated with top skills.

## Conclusion

This project provides insights into the data science job market, emphasizing the value of acquiring multiple relevant skills, regional salary variations, top skills of data professionals, and the relationship between specific skills and higher salaries. The analysis was conducted using various Excel features, including Power Query, PivotTables, DAX, and charts.

I hope this project serves as a practical guide for data professionals, offering valuable insights into the skills needed for higher-paying roles.
