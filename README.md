# Hospital-Analysis
## Table Of Contents
- [Project overview](#project-overview)
- [Data Sources](#data-sources)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Results of Findings](#results-of-findings)
- [Recommendations](#recommendations)
- [Limitations](limitations)

### Project Overview
This Data Analysis Project aims to provide insights into patient demographics and trends, medical equipment usage and maintenance and staff performance in the Health Care industry. By analyzing various aspects of hospital data, this project seeks to identify areas for improvement in hospital operations such as in efficiency and patient care and satisfaction, make data-driven recommendations and gain a deeper understanding of the industry's performance. This project is of personal interest to me as i've always had a keen interest in the health care industry and was curious as to how the management of large hospitals are able to decide what equipments to stock more or less of as well as how they keep a track of the volume of patients coming in, so the appropriate number of staff members can treat all patients without long wait times and without staff members feeling burnt out.

[Dashboard](hospital.png)

![image](https://github.com/ChrisAnn609/Hospital-Analysis/assets/173093556/8c457fbe-77f2-4b1d-bb84-4ce6dd6d6094)

  

### Data Sources
The Primary Data set used for this analysis is the "Hospital Data Analysis.xlsx" file containing detailed information about
- Patient Records
- Staff Schedule
- Medical Equipment Logs
- Equipment Failure logs
    
#### The tools used were:
- Kaggle- Data Collection
- Excel- Data Entry 
- Power BI- Data Cleaning, transformation and Visualization

### Data Cleaning and Preparation
In the initial data preparation phase, the following tasks were performed:
- Data loading and inspection
- Handling missing and duplicate values
- Data cleaning and formatting

### Exploratory Data Analysis
Exploratory Data Analysis involved exploring the Cinema Data Analysis data to answer key questions such as:
- What are the trends in patient admissions and discharges over time?
- Are there any correlations between equipment maintenance schedules and equipment failures?
- What is the patient population like(gender, age range, geographic distribution)?
- Are there any staffing and or scheduling issues?
    
The visualizations used to answer this question included: Slicers, cards, Line charts, Bar charts, Scatter Plots, Waterfall chart, Gauge chart and Pie Charts. For the Hospital Analysis project, 100 patients visited the hospital within January to March 2023. Of the 100 patients, 58 were females and 42 were males. The patients were from the parishes of Manchester, Portland, St. Thomas, St. Ann and St. James. Patients visited the hospital for a number of issues. The main illnesses seen within the patients were: , which were further categorized into urgent, semi-urgent and non-urgent cases. For non-urgent cases, patients only spent a few hours at the hospital. For semi-urgent cases, customers spent between 1-6 days in the hospital while for urgent cases, customers spent 1 week in the hospital.
The analysis of the charts reveals that the highest number of admissions and discharges occurred in the second quarter of 2023, with 42 admissions and 40 discharges, respectively. The first quarter shows the lowest activity for both admissions and discharges, with only 13 each. There is a significant drop in both admissions and discharges in the fourth quarter, with 16 admissions and 18 discharges. The general trend indicates a peak in hospital activity during the second quarter, followed by a decline in the subsequent quarters. The third quarter maintains a moderate level of activity.
A total of 70 equipments were used over the twelve week period. These were: 16 Blood Pressure Monitors, 13 Pulse Oximeters, 12 Insulin Pumps, 12 Treadmills with Cushioning, 10 Ultrasound Machines and 7 Bariatric Wheelchairs. The hospital equipments recorded a peak usage of 19 days in May and a low of 2 days in March, thus had an equipment utilization rate of 99%. There was a steady increase in downtime from January to July, peaking at 5 days in July. November recorded 3 days of downtime, leading to a total of 22 downtime days across the year. The Hospital Analysis also provided a comprehensive view of the distribution of staff members within various departments and time slots. There were 30 members of staff in total distributed across the Radiology, Cardiology, Emergency, Obstetrics, Human Resources, Laboratory, and Security departments. The shifts assigned to the members of staff were:10:00 am-6:00 pm, 10:00 pm - 8:00 am,12:00 am-8:00 am, 12:00 pm -8:00 pm, 4:00 pm -12:00 am, 6:00 pm - 2:00 am, 7:00 am-3:00 pm, 8:00 am-4:00 pm, 9:00 am -5:00 pm and 9:30 am -5:30 pm.  Every week, a Doctor was assigned to a different department. 
 ### Data Analysis
The following metrics were calculated using DAX formulas:
  
  1- Staff attendance rate for the month of March.
  
  2- Average length of stay for Patients.
  
  3- Equipment Utilization Rate.

  4- Total downtime in days by Equipment type.
  
Staff attendance rate for the month of March calculation.

The formula used to calculate the Staff attendance rate for the month of March is as follows:

```
Staff Attendance Rate = DIVIDE([Total Staff Present (March)],[Total Staff Members],0)
)
```


Average length of stay for Patients calculation

The formula used to calculate the Average length of stay for Patients is as follows:

```
Average Length of Stay = 
AVERAGE('Patient Records (2)'[Length of Stay])
```

Equipment Utilization Rate

The formula used to calculate the Equipment Utilization rate is as follows:
```
Equipment Utilization Rate = 
DIVIDE(
    [Total Usage Hours],
    [Total Available Hours],
    0
)
```
Total downtime in days by Equipment type
The formula used to calculate the Total downtime in days by Equipment type is as follows:
```
TotalDowntime = SUM('Equipment Failure Log'[Downtime in days])
```

### Results Of Findings

- The staff attendance rate for the month of March was 20%, which means that staff members were present and ontime for 20% of their scheduled work. Staff members were either late or absent for 80% of the scheduled work hours for the month of March. This low attendance rate could lead to understaffing, increased workload on present staff and delays in terms of patients receiving proper health care in a timely manner.
- The average length of stay for patients at the hospital was 4 days. This means that on average, patients are admitted and remain in the hospital for four(4) days before being discharged.
- The months of May, June and July recorded the highest number of admissions and discharges, while the month of March recorded the lowest number of admissions and discharges.
- The majority of the patients were from the parishes of Manchester and St. Ann.
- The Equipment Utilization rate was 99%, meaning that the equipments are being used for a significant portion of time.
- Neither Blood pressure monitors, Ultrasound machines nor treadmills with cushioning had no downtime.
- Pulse Oximeters were down for 10 days out of the 12 week period; while the Insulin Pump and Bariatric Wheelchairs were down for 6 days out of the 12 week period.
- For non-urgent cases, patients only spent a few hours at the hospital. For semi-urgent cases, customers spent between 1-6 days in the hospital while for urgent cases, customers spent 1 week in the hospital.
- There were nearly equal amounts of urgent, semi-urgent and non-urgent cases.
- May was the busiest month for equipment usage.


### Recommendations
Based on the analysis, the following actions are recommended:
- The Hospital should enforce attendance policies or provide incentives for good attendance.
- Hospital Management must ensure the working conditions are more conducive for working so staff members will attend work regularly and be on time. This will ensure patients receive proper health care in a timely manner.
- Invest in more Pulse Oximeters especially.
-  Ensure proper maintenance schedule is in place in order to prevent machine breakdown, due to not being able to service the machines as often as they should. Management should focus on managing and reducing equipment downtime in order to increase operational efficiency.
-  Allocate more resources and increase staffing during the second quarter to manage the higher volume of patients.This will ensure better preparedness for periods of high and low patient activity throughout the year and improve overall hospital operations.

### Limitations
  Some records had to be excluded, as the accuracy of the analysis conclusion would have been affected.
