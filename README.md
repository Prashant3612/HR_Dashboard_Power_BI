 # HR Analytics with Power BI: Employee Attrition Analysis

## Overview
Understanding the underlying factors contributing to attrition is crucial for HR departments to develop effective retention strategies. This project aims to leverage Power BI to analyze employee attrition trends within a company and identify actionable insights to mitigate attrition rates.

## Problem Statement

The company faces a persistent issue of employee attrition, which is impacting its ability to maintain a stable workforce and sustain productivity levels. The HR department needs to gain deeper insights into the reasons behind employee departures and identify potential areas for improvement in retention efforts.

## Data Sources

The primary data source for this project is the company's HR database, which contains information on employee demographics, ages, compensation, and educational qualifications. Additionally, external data sources such as employee satisfaction surveys or market trends may be incorporated for comprehensive analysis.

### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that there were some duplicate entries of employees. 
- Step 5 : Duplicate entires were removed by Power Query Editior.
- Step 6 : Added an additional column was added called "AttritionCount" with reference to "Attrition" column, where we have taken "Yes" as 1 and "No" as 0.
- Step 7 : A Dough nut chart was added representing "Attrition by Education".
- Step 8 : Visual filters (Slicers) were added for Departments :"Human Resource", "Research and Development", "Sales" for better understanding.
- Step 9 : Four card visuals were added to the canvas, representing KPIs: Attrition Rate, Total Employees, Avg Salary, Avg Employee Age, Average Year at Company
- Step 10 : Two clustered bar charts were also added to represent the "Attrition by Job role", "Attrition by Salary Slab".
- Step 11 : Stacked Column chart was added to represent "Attrition by Age"
- Step 12 : Area Chart was also added to show Attrition by years at company. 
  
- Step 14 : Following Measure was created with the help of DAX expressions, 

        a)Attrition rate was calculated from column "AttritionCount" and "EmployeeCount
              Attrition Rate = DIVIDE(SUM(HR_Analytics[Attrition_count]),sum(HR_Analytics[EmployeeCount]))
        b)Total Employes = COUNT(HR_Analytics[EmpID])
        c)Avg Employee Age = AVERAGE(HR_Analytics[Age])
        d)Avg Salary = AVERAGE(HR_Analytics[MonthlyIncome])
        e)Avg Years At Company = AVERAGE(HR_Analytics[TotalWorkingYears])
        

 # Report Snapshot (Power BI DESKTOP)

 
![Dashboard_upload](https://raw.githubusercontent.com/Prashant3612/HR_Dashboard_Power_BI/main/HR_Dashboard.jpg)

# Insights

A single page report was created on Power BI Desktop.

Following inferences can be drawn from the dashboard;

### [1] KPIs
        Oerall Employees = 1470
        Attrition Rate: 16.1%
        Avg. Year at Company: 7.01
        Avg. Employee Age: 37
        Avg. Salary: $7K/annum

           
           
### [2] Salary Slab

   Employees in lower salary brackets exhibit higher attrition rates, while attrition decreases as salary levels increase. This highlights the significant    impact of compensation satisfaction on employee retention within the organization.  
  
  ### [3] Attrition by Education
    Life Sciences: 41.22%
    Medical: 31.56%
    Marketing: 10.82%
    Technical Degree: 8.96%

  a) This suggest that unique challenges in Life Sciences and Medical fields may contribute to higher attrition, such as workload or limited career   advancement.

  b) Technical Degree holders show lower attrition, suggesting clearer career paths; replicating this success may benefit other fields.
  
  c) Assessing alignment between job requirements and employee skills can identify mismatches affecting attrition.
  
      
 ### [4] Some other insights
 
 ### Attrition by Job role
 a) Sales-related roles, notably Sales Executives and Representatives, face higher attrition, suggesting issues in sales departments requiring attention.
 
  b) Prioritize retention efforts for Sales, Research, and Lab roles to stabilize the workforce and maintain productivity.
  
  c) Research Scientist and Research Director roles have relatively high attrition. Offering clear career paths, opportunities for professional growth, and     recognition for contributions could enhance retention in research-oriented positions.
  
  d) The relatively low attrition in Manager and Manufacturing Director roles suggests effective leadership or career satisfaction among employees in these  positions. Understanding and replicating the factors contributing to their lower attrition rates could benefit other areas of the organization

 ### Attrition by Years at company

  a) As experience in the company increases, attrition rates decrease
  
  b) Long-serving employees exhibit lower attrition rates, indicating successful retention efforts and higher job satisfaction over time.
  
  c) Lower attrition among experienced employees shows effective succession planning and leadership development


### Job Satisfaction Rating

   a) Levels 2 and 3 ratings dominate, indicating a significant portion of employees are moderately satisfied, with potential for improvement.
   
   b) High responses at level 1 suggest a notable proportion of dissatisfied employees, warranting focus to mitigate retention risks and enhance morale.

### Attrition by Gender
  There were more males who left the company as compared to females.
