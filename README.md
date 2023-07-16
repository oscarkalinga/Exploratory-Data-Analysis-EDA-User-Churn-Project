# Exploratory Data Analysis (EDA), User Churn Project

# Project Overview
The Waze data team is currently developing a data analytics project aimed at increasing overall growth by 
preventing monthly user churn on the Waze app. Thorough exploratory data analysis (EDA) enables Waze 
to make better decisions about how to proactively target users likely to churn, thereby improving retention 
and overall customer satisfaction. This report offers details and key insights which 
impact the future development of the overall project. The key insight drawn from the analysis is the more times users used the app, the less likely they were to churn. While 40% of the users who didn't use the app at all last month churned, nobody who used the app for 30 days churned.

# Business understanding
Waze’s free navigation app makes it easier for drivers around the world to get to where they want to go. Waze’s community of map editors, beta testers, 
translators, partners, and users helps make each drive better and safer. Waze partners with cities, transportation authorities, broadcasters, businesses, 
and first responders to help as many people as possible travel more efficiently and safely. You’ll collaborate with your Waze teammates to analyze and interpret 
data, generate valuable insights, and help leadership make informed business decisions.

Your team is about to start a new project to help prevent user churn on the Waze app. Churn quantifies the number of users who have uninstalled the Waze app or
stopped using the app. This project focuses on monthly user churn. This project is part of a larger effort at Waze to increase growth. 
Typically, high retention rates indicate satisfied users who repeatedly use the Waze app over time. Developing a churn prediction model will help prevent churn, 
improve user retention, and grow Waze’s business. An accurate model can also help identify specific factors that contribute to churn and answer questions 
such as: 
Who are the users most likely to churn?
Why do users churn? 
When do users churn? 
For example, if Waze can identify a segment of users who are at high risk of churning, Waze can proactively engage these users with special offers to try and retain them. Otherwise, Waze may lose these users without knowing why. 
Your insights will help Waze leadership optimize the company’s retention strategy, enhance user experience, and make data-driven decisions about product development.

## Team members at Waze
Data team roles
<ul>
  <li> Harriet Hadzic - Director of Data Analysis </li>
  <li>May Santner - Data Analysis Manager </li>
  <li>Chidi Ga - Senior Data Analyst </li>
  <li>Sylvester Esperanza - Senior Project Manager</li>
</ul>
Data team members have technical experience with data analysis and data science. However, you should always be sure to keep summaries and messages
to these team members concisely and to the point. 
<br></br>
Cross-functional team members
<ul>
  <li>Emrick Larson - Finance and Administration Department Head </li>
  <li>Ursula Sayo - Operations Manager</li>
</ul>
Your Waze team includes several managers overseeing operations. It is crucial to adapt your communication to their roles since their responsibilities 
are less technical.

> Note: The story, all names, characters, and incidents portrayed in this project are fictitious. No identification with actual persons (living or deceased) is 
intended or should be inferred. And, the data shared in this project has been created for pedagogical purposes.

# Data Understanding
The user churn data came from Google partner [Waze](https://drive.google.com/file/d/1wM0b6kXat7WOgDZIdszZetSuxdYTrRN9/view?usp=sharing). 
The data consisted of approximately 15k unique users and 13 features. The features included information on 
ID,	sessions,	drives,	total sessions,	total navigations, driven km drives	duration minutes drives,	activity days,	driving_days
The Pie chart below shows the breakdown of how many users churned (17.7%) versus retained users (82.3%) that exist in the dataset. 

![image](https://github.com/OscarMATK/Exploratory-Data-Analysis-EDA-User-Churn-Project/assets/73540285/aba321cd-2774-4174-aa9f-e9cc0e3cbc28)

# Key insights
<ul>
  <li>The more times users used the app, the less likely they were to churn. While 40% of the users who didn't use the app at all last month churned, nobody who used the app 30 days churned.
</li>
  <li>Distance driven per driving day had a 
positive correlation with user churn. The 
farther a user drove on each driving day, 
the more likely they were to churn.</li>
  <li>Number of driving days had a negative 
correlation with churn. Users who drove 
more days of the last month were less 
likely to churn.
</li>
  <li>Users of all tenures from brand new to 
~10 years were relatively evenly 
represented in the data</li>
  <li>Nearly all the variables were either very 
right-skewed or uniformly distributed.</li>
    <ul>
      <li>or the right-skewed distributions, 
this means that most users had 
values in the lower end of the range 
for that variable</li>
      <li>For the uniform distributions, this 
means that users were generally 
equally likely to have values 
anywhere within the range for that 
variable.
      </li>
    </ul>
</li>
  <li>Several variables had highly improbable 
or perhaps even impossible outlying 
values, such as: driven_km_drives, 
activity_days and driving_days
  </li>
</ul>
<br></br>

![image](https://github.com/OscarMATK/Exploratory-Data-Analysis-EDA-User-Churn-Project/assets/73540285/8706f73b-ceb4-4c26-b248-a6a39100a903)

The churn rate is highest for people who didn't use Waze much during the last month. The more times they used the app, the less likely they were to churn. While 40% of the users who didn't use the app at all last month churned, nobody who used the app 30 days churned.

![image](https://github.com/OscarMATK/Exploratory-Data-Analysis-EDA-User-Churn-Project/assets/73540285/19b63cf0-f4ad-4aab-b22d-7bc14a3b77c6)

The proportion of churned users to retained users is consistent between device types.

# Conclusion
The following questions drive the conclusion
<br>
**Questions:**

1. What types of distributions did you notice in the variables? What did this tell you about the data?

> *Nearly all the variables were either very right-skewed or uniformly distributed. For the right-skewed distributions, this means that most users had values in the lower end of the range for that variable. For the uniform distributions, this means that users were generally equally likely to have values anywhere within the range for that variable.*

2. Was there anything that led you to believe the data was erroneous or problematic in any way?

> *Most of the data was not problematic, and there was no indication that any single variable was completely wrong. However, several variables had highly improbable or perhaps even impossible outlying values, such as `driven_km_drives`. Some of the monthly variables also might be problematic, such as `activity_days` and `driving_days`, because one has a max value of 31 while the other has a max value of 30, indicating that data collection might not have occurred in the same month for both of these variables.*

3. Did your investigation give rise to further questions that you would like to explore or ask the Waze team about?

> *Yes. I'd want to ask the Waze data team to confirm that the monthly variables were collected during the same month, given the fact that some have max values of 30 days while others have 31 days. I'd also want to learn why so many long-time users suddenly started using the app so much in just the last month. Was there anything that changed in the last month that might prompt this kind of behavior?*

4. What percentage of users churned and what percentage were retained?

> *Less than 18% of users churned, and \~82% were retained.*

5. What factors correlated with user churn? How?

> *Distance driven per driving day had a positive correlation with user churn. The farther a user drove on each driving day, the more likely they were to churn. On the other hand, number of driving days had a negative correlation with churn. Users who drove more days of the last month were less likely to churn.*

6. Did newer uses have greater representation in this dataset than users with longer tenure? How do you know?

> *No. Users of all tenures from brand new to \~10 years were relatively evenly represented in the data. This is borne out by the histogram for `n_days_after_onboarding`, which reveals a uniform distribution for this variable.*
Investigate the erroneous or problematic discrepancies 
between a number of sessions, driving_days, and 
activity_days.

# Recommendations
<ul>
  <li>Investigate the erroneous or problematic discrepancies between number of sessions, driving_days, and activity_days</li>
  <li>Continue to explore user profiles with the greater Waze team; this may glean insights on the reason for the long-distance drivers’ churn rate</li>
  <li>Plan to run deeper statistical analyses on the variables in the data to determine their impact on user churn.</li>
</ul>
