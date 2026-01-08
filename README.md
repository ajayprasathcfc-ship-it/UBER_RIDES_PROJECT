# UBER_RIDES_PROJECT

Uber Ride Analysis using Data Science
Dataset Description


The dataset used in this project contains historical Uber ride information recorded over a period of time. Each row represents a single Uber trip with details related to time, distance, category, and purpose of the ride.



Dataset Features:

START_DATE* – Date and time when the ride started

END_DATE* – Date and time when the ride ended

CATEGORY* – Type of ride (Business or Personal)

START* – Pickup location

STOP* – Drop-off location

MILES* – Distance traveled during the ride

PURPOSE* – Reason for the ride

Derived Features:

DATE – Date extracted from start time

TIME – Hour of the day (0–23)

DAY-NIGHT – Time period classification (Morning, Afternoon, Evening, Night)

MONTH – Month of the ride

WEEKDAYS – Day of the week

MINUTES – Duration of the ride

The dataset consists of 1099 ride records and 13 columns after preprocessing.





 Data Preprocessing

To ensure data quality and consistency, the following preprocessing steps were performed:

Removed duplicate rows to avoid data repetition

Converted date-related columns to proper datetime format

Handled missing values:

Numerical columns were filled using mean/median values

Extracted new features from datetime columns such as:

Hour of day

Weekday

Month

Categorized rides into time periods using pd.cut():

Middle of Night, Morning, Afternoon, Evening, Night

Verified dataset integrity using:

df.info()

df.describe()

df.isnull().sum()

These steps helped create a clean and structured dataset suitable for analysis.





Exploratory Data Analysis (EDA)

Exploratory Data Analysis was conducted to understand ride patterns and distributions using visualizations and summary statistics.

EDA Techniques Used:

Count plots for:

Rides by category (Business vs Personal)

Rides by weekday

Rides by month

Rides by hour (peak hours)

Bar plots for:

Top 10 pickup locations

Line plots for:

Average distance traveled by hour

Heatmaps to analyze:

Ride purpose vs day/night distribution

Descriptive statistics to identify:

Central tendencies

Variations

Outliers in ride distance and duration

All visualizations were created using Matplotlib and Seaborn libraries.





Key Insights

Based on the analysis, the following insights were observed:

Business rides significantly outnumber personal rides

Ride demand is higher during night and evening hours

Friday records the highest number of rides compared to other weekdays

January shows the highest ride frequency among all months

Meetings and unspecified purposes dominate business rides

Certain pickup locations appear frequently, indicating high-demand zones

Long-distance rides exist as outliers and may represent special trips




Tools & Libraries Used

Python

Pandas

NumPy

Matplotlib

Seaborn

Jupyter Notebook




Conclusion

This project demonstrates effective use of data cleaning, feature engineering, and exploratory data analysis techniques to understand Uber ride behavior. The insights extracted from visual analysis provide a clear understanding of ride patterns across time, category, and purpose.
