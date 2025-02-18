# Healthcare_0107

### Report Link : https://drive.google.com/file/d/19yUtZHYXJ6KFMZEroE1i3zWFiOeZ-BNp/view?usp=drive_link

## Problem Statement

The objective is to import and analyze financial performance data from local files using Power BI. 
The analysis aims to evaluate key financial metrics and trends within the healthcare sector. 
Additionally, the study will provide insights into the performance and efficiency of healthcare providers, 
helping stakeholders make data-driven decisions.


### Project Requirement

To Build report and dashboard of bellow


### 1) KPIs and Trends:

Identify and present the key 
performance indicators (KPIs) and significant trends in the dataset.

### 2) Detailed Analysis:

Ensure the analysis is thorough and 
detailed, covering all relevant aspects of the healthcare center's finance and the performance of healthcare providers.

### 3) Dashboard Creation:

#### Create a comprehensive dashboard includes:
 - Financial Overview: Summarize the financial health of the healthcare center.
 - Provider Insights: Analyze the performance and efficiency of healthcare providers.
 - Trend Analysis: Highlight any important trends over time.
 - Additional Insights: Any other relevant insights that can be derived from the data.


### Expectations:
- Visualization: Use appropriate visualizations to effectively communicate the findings.
- Interactivity: Ensure the dashboard is interactive and user-friendly.
- Clarity: Present the data in a clear and concise manner, making it easy for stakeholders to understand the insights.



### Steps followed 

- Step 1 : Load data into Power BI Desktop,by connecting to locally downloaded csv files on machine
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : There was no need to clean or do any tranformation on dataset so from here i moved to further steps and loaded data in power bi 
- Step 5 : For a detailed analysis created a seperate date table to analyze data yearly quarterly ,monthly and weekly basis by using the DAX formuala as bellow.
           
           = Date Table = 
           ADDCOLUMNS(CALENDARAUTO(),
           "Year",YEAR([Date]),
           "Month",FORMAT([Date],"mmm"),
           "Monthnum",MONTH([Date]),
           "Weekday",FORMAT([Date],"ddd"),
           "Weeknum", WEEKDAY([Date]),
           "Qtr","Q-"& FORMAT([Date],"Q"),
           "WeekType",IF(WEEKDAY([Date]) = 1 ||
            WEEKDAY([Date]) = 7,
            "Weekend""Weekday"))


Snap of newly calculated date table ,

![Image](https://github.com/user-attachments/assets/5ab8a16a-25ce-4b57-8b14-edba05050ac7)
        
- Step 6 : Created Data Model by using Star schema from here started creating report Requirement here my fact table is visits and dimensions are remaining tables.

- Step 7 : As per the report Requirement i created list of DAX measures and bundlled  them in a table 

Here's snap of measures 

![Image](https://github.com/user-attachments/assets/c852f56a-d543-4519-a9f3-85938e412922)

- Step 8 : For all the KPIs trend analysis for Billling Amount,Medication Cost,Treatment Cost,Insurance Cover,Room Charges and Out Of Pocket indicatores i used Card New Visual and grouped them in one Ribbon.

- Step 9 : To show Billing Amount by each city  i used Bar Chart Visual

- Step 10 : To show Total Billing Amount by Procedure i used column Chart and added Data Lables for each column and percentage of totals by Procedure.
 
 - Step 11 : To show Billing amount by Diagnosis and Service Type i used clusterd bar chart and added Data Lables to Claculate percentage totals .

 - Step 12 : For Overall report Interactivity i added slicer visual for Department column.
 
And here's final snap of Analysis Page.

![Image](https://github.com/user-attachments/assets/7b90e30c-fa40-49f0-8e01-65e34d27db70)
 
 
- Step 13 : For Home Page i used canva to design a logo and name for the hospital and on home page to show key heilights of report.

# Snapshot of Home Page

![Image](https://github.com/user-attachments/assets/c1fe217b-57b8-411e-82d7-51c687d81527)

# Insights

A two pages report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### As per the Requirement of hospital we created the Power BI report for their Data analytics.
