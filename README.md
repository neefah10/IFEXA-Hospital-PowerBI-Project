# Healthcare Performance & Patient Analytics Dashboard
### IFEXA Power BI Final Project

#### Project Overview
I was hired as a Data Analyst for a healthcare organization operating across different states in Nigeria. Management provided raw data about patient visits, departments, revenue, cost, waiting time and satisfaction. My task was to turn this data into an interactive Power BI dashboard that answers one main question: "How is our organization performing, what are patients experiencing, and where should management focus?"

#### Business Problem
The hospital was managing operations with raw data but no clear view of performance. They could not easily see which departments had long waiting times, which states were bringing more revenue, why targets were not met, or how waiting time affected patient satisfaction.

#### Dataset Description
The dataset contains three tables:
- **Patient Visits:** Patient ID, Visit Date, State, Branch, Department, Diagnosis, Age, Gender, Revenue, Cost, Waiting Time, Satisfaction Score, Outcome, Patient Type
- **State Targets:** Monthly revenue target per state
- **Date Table:** For time analysis

#### Tools Used
- Power BI Desktop
- Power Query for data cleaning
- DAX for measures
- Excel for source data

#### Data Cleaning Process
Using Power Query, I:
- Cleaned and standardized text fields like State, Branch and Department
- Fixed date formats and created a proper Date Table
- Created Age Groups from age: Child, Young Adult, Adult, Senior
- Checked for duplicates and removed errors
- Connected the tables for analysis

#### Data Model
I used a Star Schema design:
- Date Table -> Patient Visits (on Date)
- State Targets -> Patient Visits (on State)

#### DAX Measures
I created 18 measures from scratch to show I understand DAX. They include:
- Core KPIs: Total Patients, Total Visits, Total Revenue, Total Cost, Total Profit, Profit Margin %
- Patient Metrics: Average Revenue per Patient, Average Waiting Time, Average Satisfaction, Average Visits per Patient
- Financial Tracking: Revenue Target, Revenue Variance, Achievement %, Previous Month Revenue, MoM Growth, Previous Year Revenue, YoY Growth

#### Dashboard Structure

**1. Executive Overview:** High-level KPIs, Monthly Visits, Revenue by State, Patients by Department, Revenue vs Target, Outcome Distribution. Slicers: Date, State, Branch, Department, Gender.
![Executive Overview](Sreenshots/Executive%20Overview.jpg)

**2. Patient Analysis:** Patients by Age Group, Gender, Diagnosis, State, New vs Returning, Patient Outcomes and average visits. This page answers who our patients are and where they come from.
![Patient Analysis](Screenshots/Patient%20Analysis.jpg)

**3. Hospital Operation:** Visits by Department, Waiting Time by Department, Satisfaction by Department, Branch Performance and monthly volume. Shows operational efficiency.
![Hospital Operation](Screenshots/Hospital%20Operations.jpg)

**4. Financial Performance:** Revenue by State, Department and Service, Profit by Department, Monthly Revenue trend and Target achievement. Shows financial health.
![Financial Performance](Screenshots/Financial%20Performance.jpg)

**5. Patient Experience:** Satisfaction by Department and Branch, Satisfaction vs Waiting Time, Outcome and Satisfaction distribution.
![Patient Experience](Screenshots/Patient%20Experience.jpg)

**6. Operation Detail:** Drill-through page for deeper view of operations. Allows users to right-click from main pages to see detailed breakdown.
![Operation Detail](Screenshots/Operation%20Detail.jpg)

**7. Financial Detail:** Drill-through page for deeper view of finance. Shows transaction-level details behind summary.
![Financial Detail](Screenshots/Financial%20Detail.jpg)

Features used: Slicers, Drill-through, Conditional Formatting, Tooltips, Bookmarks, Page Navigation and Dynamic Titles.

#### Key Insights
**Patient Analysis:**
- Adult age group has the largest number of patients
- Malaria and Typhoid are the most common diagnoses
- Rivers State has the highest patient volume while some branches like Lekki have lower volume
- Most patients are returning patients, which shows good retention but new patient growth needs attention
- Most patients recovered, but some require follow-up or referral

**Hospital Operations:**
- Pediatrics handles the highest patient load
- Laboratory department has the longest waiting time
- Obio-Akpor branch handles the most visits and also records longer waiting times
- There is a seasonal trend, with peak in July and low in December

**Financial Performance:**
- Rivers State generates the highest revenue
- No state met its revenue target, which shows a gap that needs investigation
- Pediatrics is the most profitable department
- Revenue trend follows patient volume

**Patient Experience:**
- Pharmacy has the highest satisfaction, Maternity has the lowest
- There is a clear relationship between waiting time and satisfaction. When waiting time increases, satisfaction drops
- Overall satisfaction is stable but can be improved

#### Recommendations
1. Reduce waiting time in Laboratory and busy branches like Obio-Akpor by adding staff during peak periods.
2. Investigate low-volume branches like Lekki and Nnewi to understand if it is awareness, service mix or location issue.
3. Plan staffing and resources based on seasonal pattern. Prepare for July peak and manage cost in December.
4. Review referral cases to know if it is due to lack of specialists or equipment.
5. Create improvement plan for Maternity department to increase satisfaction.

#### Conclusion
This project shows a complete BI process from data cleaning with Power Query, to building a Star Schema model, creating DAX measures, and designing clear visuals. The goal was not just to make a beautiful dashboard, but to make a useful one that helps management make better decisions.

#### Files in this Repository
- Dataset: Cleaned Excel file
- Power BI File: .pbix file
- Screenshots: 7 dashboard pages

Author: Abdulrasheed Hanifat | IFEXA Final Project
