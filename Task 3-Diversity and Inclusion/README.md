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
<a href ="https://github.com/gaurav510610/PwC-Switzerland-Power-BI-in-Data-Analytics-Virtual-Internship/blob/main/Task%203-Diversity%20and%20Inclusion/03%20Diversity-Inclusion-Dataset.xlsx">DataSet</a>
 

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

Dashboard:  <a 
href ="https://github.com/gaurav510610/PwC-Switzerland-Power-BI-in-Data-Analytics-Virtual-Internship/blob/main/Task%203-Diversity%20and%20Inclusion/Diversity%20%26%20Inclusion.pbix">View Dashboard</a>


Shows visualizations from Diversity and Inclusion:
#                                  Diversity& Inclusion  HR Dashboard 1
![Alt text of the image](https://github.com/gaurav510610/PwC-Switzerland-Power-BI-in-Data-Analytics-Virtual-Internship/blob/main/Task%203-Diversity%20and%20Inclusion/dashboard1-1.png)
#                                 Diversity& Inclusion  HR Dashboard 2      
![Alt text of the image](https://github.com/gaurav510610/PwC-Switzerland-Power-BI-in-Data-Analytics-Virtual-Internship/blob/main/Task%203-Diversity%20and%20Inclusion/dashboard2-1.png)
#                                 Diversity& Inclusion  HR Dashboard 3
![Alt text of the image](https://github.com/gaurav510610/PwC-Switzerland-Power-BI-in-Data-Analytics-Virtual-Internship/blob/main/Task%203-Diversity%20and%20Inclusion/dashboard3-1.png)
#  Insights:
As shown the data Visualization, It can be deduced that:

- 41 % Female hires of the year and 59 % Male hires of the years.
- 53.8% of promoted were Female in the Junior Officer category, the highest for the year.
- 47% of promoted were Male in the Junior Officer category, the lowest for the year.
- Director is the highest Average time of job level promoted in this year.
- Average Rating Female 2.42%
- Average Rating Male 2.41%
- Employees promoted year of 2021 is 54.34% Male and 45.66% Female.
- The most common age group is 20-29 having 223 employees fall in this category.
# Recommendations

- There is a need to look into the rate of employment of staffs from different nationality, people of different nationality should be encouraged to take up roles in the company.
- From the analysis above the rate of Diversity and Inclusion is low considering how that there's gender imbalance in how staffs are hired and promoted.
- Strengthen leadership development programs to groom and support individuals from all backgrounds for higher roles. This contributes to a pipeline of diverse talent ready to take on leadership positions.
- Maintain transparent communication about promotion criteria, processes, and opportunities within the organization. This clarity can empower employees to proactively engage in their career development.
- Conducting employee satisfaction surveys, with a specific focus on gender-related experiences, can unveil qualitative insights. Understanding how men and women perceive the workplace culture and opportunities for advancement is crucial for addressing any potential disparities.
- Review existing HR policies to ensure they are inclusive and accommodate the diverse needs of all employees. This includes considerations such as flexible working arrangements, parental leave policies, and initiatives promoting work-life balance.
- Conduct periodic diversity audits to track progress over time. Regular assessments ensure that diversity and inclusion initiatives remain a priority and provide valuable insights for ongoing refinement.

