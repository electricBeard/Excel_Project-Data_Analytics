# Excel Salary Analysis
## Introduction
As a job seeker, I've always been surprised by the lack of analysis we do to optimize our skills for the data science market. I set out to understand what skills top employers request and, therefore, how job seekers can find opportunities to land more pay.

### Questions to Analyze  
To understand the data science job market, I asked the following:  
1. Do more skills get you better pay?
2. What’s the salary for data jobs in different regions?
3. What are the top skills of data professionals?
4. What’s the pay for the top 10 skills?

### Excel Skills Used  
The following Excel skills were utilized for analysis:
- 📊 Pivot Tables
- 📈 Pivot Charts
- 🧮 DAX (Data Analysis Expressions)
- 🔍 Power Query
- 💪 Power Pivot  

### Data Jobs Dataset  
The dataset used for this project contains reeal-world data science job information from 2023. The dataset was compiled by [Luke Barousse](https://youtu.be/pCJ15nGFgVg?si=OHtraTw1cDgKTO3j) and provides a foundation for analyzing data using Excel.  

It includeds detailed information on:  
- 👨‍💼 Job titles
- 💰 Salaries
- 📍 Locations
- 🛠️ Skills  

## 1️⃣ Do more skills get you better pay?
### 🔍 Skill: Power Query (ETL)
#### 📥 Extract
* I first used Power Query to extract the original data (data_salary_all.xlsx) and create two queries:  
  * 🗃️ First one with all the data jobs information.
  * 🔧 The second listing the skills for each job ID.  

#### 🔄 Transform
* Then, I transformed each query by changing column types, removing unnecessary columns, cleaning text to eliminate specific words, and trimming excess whitespace.  
  * 📊 data_jobs_all  
  ![Applied Steps to data jobs](P2_Images/2_Project_Analysis_Screenshot1.png)  
  * 📊 data_jobs_skills  
  ![Applied Steps in job skills](P2_Images/2_Project_Analysis_Screenshot2.png)  

#### 🔗 Load
* Finally, I loaded both transformed queries into the workbook, setting the foundation for my subsequent analysis. 
  * 📊 data_jobs_all  
    ![power query editor large](P2_Images/2_Project_Analysis_Screenshot3.png)  
  * 🛠️ data_job_skills
    ![power query editor 2 columns](P2_Images/2_Project_Analysis_Screenshot4.png)  

### 📊 Analysis  
#### 💡 Insights  
* 📈 There is a positive correlation between the number of skills requested in job postings and the median salary, particularly in roles like Senior Data Engineer and Data Scientist.  
* 💼 Roles that require fewer skills, like Business Analyst, tend to offer lower salaries, suggesting that more specialized skill sets command higher market value.  
![Applied Steps in Transform](P2_Images/2_Project_Analysis_Chart1.png)  

#### 🤔 So What
* This trend emphasizes the value of acquiring multiple relevant skills, particularly for individuals aiming for higher-paying roles.

## 2️⃣ What’s the salary for data jobs in different regions?
### 🧮 Skills: PivotTables & DAX
#### 📈Pivot Table
* 🔢 I created a PivotTable using the Data Model I created with Power Pivot.
* 📊 I moved the `job_title_short` to the rows area and `salary_year_avg` into the values area.
* 🧮 Then I added new measure to calculate the median salary for United States jobs.  
```
=CALCULATE(
    MEDIAN(data_jobs_all[salary_year_avg]),
    data_jobs_all[job_country] = "United States")
```  
#### 🧮 DAX
* To calculate the median year salary I used DAX.  
```
Median Salary := MEDIAN(data_jobs_all[salary_year_avg])
```  

### 📊 Analysis
#### 💡 Insights
* 💼 Job roles like Senior Data Engineer and Data Scientist command higher median salaries both in the US and internationally, showcasing the global demand for high-level data expertise.  
* 💰 The salary disparity between US and Non-US roles is particularly notable in high-tech jobs, which might be influenced by the concentration of tech industries in the US.  
![skills vs salary chart](P2_Images/2_Project_Analysis_Chart1.png)  

#### 🤔 So What
* This trend emphasizes the value of acquiring multiple relevant skills, particularly for individuals aiming for higher-paying roles.










