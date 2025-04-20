# DIVERSITY & INCLUSION ANALYSIS
![Alt text of the image](https://github.com/gaurav510610/PwC-Switzerland-Power-BI-in-Data-Analytics-Virtual-Internship/blob/main/Task%203-Diversity%20and%20Inclusion/diversity.jpg)
# Project Brief:
Diversity and Inclusion refers an equal employment opportunity based on nationality, gender religion etc.
Human Resources at our telecom client is highly into diversity and inclusion. They’ve been working hard to improve gender balance at the executive management level, but they’re not seeing any progress. They’re reaching out to us for help.
At PwC Switzerland we are often approached by clients seeking support with diversity and inclusion. Companies need a workforce of diverse talents and backgrounds to succeed in an increasingly complex and heterogeneous world. To us, diversity and inclusion are business imperatives, not just nice-to-haves.
# Problem Statement :
The purpose of this task is to:
- Number of male
- Number of female
- Number of leavers
- % employees promoted (FY21)
- % of women promoted
- % of hires men
- % of hires women
- % turnover
- Average performance rating: men
- Average Performance rating: women
# Data Collection
The data was provided by PWC.
# Data Preparation
I started by using Excel to do a quick review of the data I would be working with. I learned how many rows and columns this particular dataset has, what kind of data is in each column, and whether there are any null values that would help with my research.

# Data Analysis (DAX):
Measures used in all visualization are:
- #of leavers = CALCULATE(COUNTA('Pharma Group AG'[Employee ID]), 'Pharma Group AG'[Leaver FY] IN { "FY20" })
- Number of Male = CALCULATE(DISTINCTCOUNT('Pharma Group AG'[Employee ID]),FILTER('Pharma Group AG','Pharma Group AG'[Gender]="Male"))
- Number of Female = CALCULATE(DISTINCTCOUNT('Pharma Group AG'[Employee ID]),FILTER('Pharma Group AG','Pharma Group AG'[Gender]="Female"))
- % employees promoted (FY21) = DIVIDE(CALCULATE(DISTINCTCOUNT('Pharma Group AG'[Employee ID]),FILTER('Pharma Group AG','Pharma Group AG'[Promotion in FY21?]="Yes")),CALCULATE(DISTINCTCOUNT('Pharma Group AG'[Employee ID]),FILTER('Pharma Group AG','Pharma Group AG'[In base group for Promotion FY21]="Yes")))
- % of Female Hires = DIVIDE('Pharma Group AG'[Number of Female],'Pharma Group AG'[Number of Male]+'Pharma Group AG'[Number of Female])
- % of Male hires= DIVIDE('Pharma Group AG'[Number of Male],'Pharma Group AG'[Number of Male]+'Pharma Group AG'[Number of Female])
- Average Male Performance Rating = CALCULATE(AVERAGE('Pharma Group AG'[FY20 Performance Rating]),'Pharma Group AG','Pharma Group AG'[Gender]="Male")
- Average Female Performance Rating = CALCULATE(AVERAGE('Pharma Group AG'[FY20 Performance Rating]),'Pharma Group AG','Pharma Group AG'[Gender]="Female")
# Data Visualization: 
Data visualization for the data analysis (DAX) was done in Microsoft Power BI Desktop:

Dashboard: View Dashboard

Shows visualizations from Diversity and Inclusion:

