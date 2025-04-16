# Call Center Trends
This is the first task of Pwc Virtual Internship on forage platform. This Power BI Report is designed for the telecom industry to understand the trends and patterns, through visuals and relevant KPI'S

![Alt text of the image](https://github.com/gaurav510610/PwC-Switzerland-Power-BI-in-Data-Analytics-Virtual-Internship/blob/main/Task%201-%20Call%20Center%20Trends/call-center.jpg)

# Problem Statement
- **Problem:** The manager at PhoneNow (a big telecom company) is seeking transparency and insight into the Call Center dataset to gain an accurate overview of long-term customer and agent behavior trends.

- **Objective:** The purpose of this analysis is to create a dashboard in Power BI for Call Center Manager that reflects all relevant Key Performance Indicators (KPIs) and metrics to:
     - Self-exploratory call trends
     - Overview of the agent’s performance and behaviors
     - Overview the customer satisfaction
     - Contain many metrics and plots related to a single area of business for discussing with higher managers and generating further 
        analysis.
    - Allows for minimal interaction
* **Possible KPIs** include (but are not limited to):
     - Overall Call
     - Issue Resolved
     - Customer Satisfaction%
     - Overall calls answered/abandoned
     - Calls by time
     - Average speed of answer
     - Agents performance quadrant -> average handle time(talk duration) vs calls answered
# Data Sourcing

The Dataset used for this analysis was provided by [Pwc Switzerland](https://www.pwc.ch/en/careers-with-pwc/students/virtual-case-experience.html) and available here: [Call Center Dataset](https://github.com/gaurav510610/PwC-Switzerland-Power-BI-in-Data-Analytics-Virtual-Internship/blob/main/Task%201-%20Call%20Center%20Trends/01%20Call-Center-Dataset.xlsx)

# Data Preparation 

The dataset was loaded into Microsoft Power BI Desktop for transformation in Power Query and modeling.
# Data Cleaning 
Data Cleaning for the dataset was done in Power Query as follows:

* Unnecessary columns were removed
* Each of the columns in the table was validated to have the correct data type
* Unnecessary rows were removed
# Data Transformation
*     The Avgtalkduration Column contains date and Time Value I didn’t need the date value, so I extracted the time from the column using 
      the Transform tab, selecting the ‘Time Only’ option. This allowed me to successfully extract the time from it.
*     I replaced null values with 0 in the satisfaction rating attribute. Since there were no specific instructions 
      on how to handle null values, and considering that it is a numeric field crucial for further business analysis, replacing them with 
      0 was chosen for ease of calculating DAX measures.
*     After that next step is to add a custom column named ‘Call Duration,’ where I converted the values of AvgTalkDuration from hours and 
      minutes into seconds. This transformation facilitates the calculation of the total call duration in seconds.
          call duration in seconds =Time.Hour([AvgTalkDuration])*3600+Time.Minute([AvgTalkDuration])*60+Time.Seconds([AvgTalkDuration])
*     After calculating the call duration column, I noticed the presence of null values in the column. Consequently, I replaced these null 
      values with 0.
*     Next step is to insert new column “Start of hour” to round down a time column to the beginning of the hour .
   
#  Data Modelling 
Since there is one table so there is no need of Data Modelling as we will be pulling our data from the one fact table only.
# Data Visualization
![Alt text of the image]()
