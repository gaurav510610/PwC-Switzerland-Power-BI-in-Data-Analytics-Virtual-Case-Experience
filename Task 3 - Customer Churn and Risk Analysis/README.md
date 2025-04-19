## Customer Churn Retention
Power BI dashboard prepared as part of the virtual internship program of PwC Switzerland The telecom dataset has a total of 7043 datapoints out of which 1869 datapoints are of churned customers. The motive of this project was to analyse the trends among churned customers, parameters affecting churn, customers at the risk of churn, tickets dashboarding to analyse churn.
# Data Sources
The data for this project was provided by PWC Virtual Internship Program provided by Forage. The data includes customer demographics, usage patterns, survey responses, and customer feedback. The data was cleaned and transformed using Power Query in Power BI Desktop to create the dashboard.

<a href ="https://github.com/gaurav510610/PwC-Switzerland-Power-BI-in-Data-Analytics-Virtual-Internship/blob/main/Task%203%20-%20Customer%20Churn%20and%20Risk%20Analysis/02%20Churn-Dataset.xlsx">Dataset</a>
# Technologies Used
**Data storage:** CSV/Excel files
- **Excel:** For initial data cleaning and manipulation.
-  Microsoft Power BI 
# Key Performance Indicators (KPIs):
- Total Customers: 7043
- Total Charges: $16.06 million
- Average Monthly Charges: $64.76
- Churn Percentage: 26.54%
# Data Visualization

Data visualization for the datasets was done in Microsoft Power BI Desktop:

• Demographic Info : Shows the male-female distribution,churn by senior citizen,dependents impact,partner impact effect of internet service provider recommendations and a short insight on the report

• Account Info : shows contrct type payment method tenuraity impact on customer count total charges, average monthly charges etc

• Services : shows customer count by streamingTV,customer count by streamingmovies,churn by phoneservice,online security device protection,Tech support etc
# Data Analysis (DAX):
Measures used in all visualization are:
- Average MonthlyCharges = AVERAGE('01 Churn-Dataset'[MonthlyCharges])
- Average TotalCharges = AVERAGE('01 Churn-Dataset'[TotalCharges])
- Churn rate % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[Churn]),'01 Churn-Dataset'[Churn]="Yes"),CALCULATE( COUNT('01 Churn-Dataset'[Churn]),ALLSELECTED('01 Churn-Dataset'[Churn])))
- % of Dependents = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[Dependents]),'01 Churn-Dataset'[Dependents]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[Dependents]),'01 Churn-Dataset'[Churn]="Yes"),0)
- Device protection in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[DeviceProtection]), '01 Churn-Dataset'[DeviceProtection] ="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[DeviceProtection]),'01 Churn-Dataset'[Churn]="Yes"),0)
- Online Backup in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[OnlineBackup]),'01 Churn-Dataset'[OnlineBackup]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[OnlineBackup]),'01 Churn-Dataset'[Churn]="Yes"),0)
- Online Security in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[OnlineSecurity]),'01 Churn-Dataset'[OnlineSecurity]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[OnlineSecurity]),'01 Churn-Dataset'[Churn]="Yes"),0)
- % of Partner = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[Partner]),'01 Churn-Dataset'[Partner]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[Partner]),'01 Churn-Dataset'[Churn]="Yes"),0)
- Phone Service in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[PhoneService]),'01 Churn-Dataset'[PhoneService]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[PhoneService]),'01 Churn-Dataset'[Churn]="Yes"),0)
- % of senior Citizen = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[SeniorCitizen]),'01 Churn-Dataset'[SeniorCitizen]=1,'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[SeniorCitizen]),'01 Churn-Dataset'[Churn]="Yes"),
 0)
- Streaming Movies in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[StreamingMovies]),'01 Churn-Dataset'[StreamingMovies]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[StreamingMovies]),'01 Churn-Dataset'[Churn]="Yes"),0)
- Streaming TV in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[StreamingTV]),'01 Churn-Dataset'[StreamingTV]="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[StreamingTV]),'01 Churn-Dataset'[Churn]="Yes"),0)
- Tech Support in % =DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[TechSupport]), '01 Churn-Dataset'[TechSupport] ="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[TechSupport]),'01 Churn-Dataset'[Churn]="Yes"),0)
#  Dashboard
You can check out my dashboard <a 
 href ='https://github.com/gaurav510610/PwC-Switzerland-Power-BI-in-Data-Analytics-Virtual-Internship/blob/main/Task%203%20-%20Customer%20Churn%20and%20Risk%20Analysis/Churn%20analysis.pbix'>here</a> .
 
# Dashboard Image
**Figure 1.** shows visualizations from Customer churn Exploratory)
![Alt text of the image](https://github.com/gaurav510610/PwC-Switzerland-Power-BI-in-Data-Analytics-Virtual-Internship/blob/main/Task%203%20-%20Customer%20Churn%20and%20Risk%20Analysis/Customer%20Churn%20exploratory%20dashboard-1.png)
**Figure 2.** shows visualizations from Customer Risk Analysis
![Alt text of the image](https://github.com/gaurav510610/PwC-Switzerland-Power-BI-in-Data-Analytics-Virtual-Internship/blob/main/Task%203%20-%20Customer%20Churn%20and%20Risk%20Analysis/Customer%20Risk%20analysis-1.png)
# Insights:
- Paperless Billing Preference: Majority of customers prefer paperless billing.
- Payment Method Trends: Electronic check or mailed check are the preferred payment methods.
- Gender Parity: Nearly equal representation of male and female customers.
- Contract Preferences: Month-to-month contracts exhibit the highest churn rate, while 2-year contracts demonstrate the highest retention rate.
- Service Demand: Fiber optics emerge as the most popular internet service.
- Demographic Breakdown: The dataset includes 3402 partners, 2110 dependents, and 1142 senior citizens, providing valuable insights into customer demographics and preferences.
- Tech tickets consisted of highest proportion among churned customers and customers using fiber optic or electronic payment method raised higher tech tickets as compared to others. Hence support services for these categories must be responsive with SLAs as low as possible
- Among churned customers 69% customers used the fiber optic internet service and 57% had the electronic payment mode.
- 2955 tech tickets were opened and 3632 admin tickets were opened.
- 7043 customers are at the risk of churn. and The churn rate is 27% and yearly charges is $16.06M charges. and Monthly Charges is $456.12K monthly charges.
# Recommendation:
- Proactive Churn Management: Implement targeted offers and personalized communication to reduce churn rates.
- Enhanced Customer Engagement: Develop initiatives to enhance customer satisfaction and loyalty.
- Optimized Contract Offerings: Offer flexible contract options with incentives for longer-term commitments.
- Streamlined Billing Processes: Improve billing processes and promote automatic payment methods.
- Continuous Monitoring and Analysis: Establish a framework for continuous monitoring of customer data to identify emerging trends.
- The Company could try convincing customers to subscribe to One-Year and Two-Year contract. The contract are not favorable to customers as they tend to pay more monthly
- Increase sales of 1 and 2-year contracts by 5% each and Yearly increase of automatic payments by 5%.



