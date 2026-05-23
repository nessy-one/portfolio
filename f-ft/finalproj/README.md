# Instagram-usage-analysis Dashboard
This repository contains analytical insights from 134,656 synthetic records of Instagram usage per user. It documents the data analytics techniques applied to preprocess, analyze, and interpret the data, and presents actionable insights using appropriate tools and methodologies.
# 1. Project Overview
This project applies data analytics to a synthetic Instagram usage dataset. The goal is to identify trends among users with different demographics, backgrounds, lifestyles, and habits, and understand how these factors relate to their Instagram usage. The project transforms raw data into actionable insights through data preprocessing, Star Schema modeling, and interactive visualization
* dataset profile: it is a 100% synthetic dataset that contains 134656 records of different users. it contains 57 columns with and has key themes such as demographic & background, lifestyle & habit, and instagram usage and engagement.
<img width="1878" height="691" alt="image" src="https://github.com/user-attachments/assets/36c815e5-74bd-468f-afc8-4e0f48826834" />
<img width="1896" height="688" alt="image" src="https://github.com/user-attachments/assets/8b8800ab-b4da-47df-84aa-e3df8e877113" />
<img width="1900" height="727" alt="image" src="https://github.com/user-attachments/assets/619f3683-b18c-4ba0-87fb-76a00f3c972e" />
<img width="1812" height="727" alt="image" src="https://github.com/user-attachments/assets/493898a4-f02b-48e7-8d6d-07aefdc65050" />

# It contains the following:
  + Demographics and Background – age, gender, country, urban/rural, income_level, employment_status, education_level, relationship_status, and has_children.
  + Lifestyle & Health - exercise_hours_per_week, sleep_hours_per_night, diet_quality, smoking, alcohol_frequency, perceived_stress_score, self_reported_happiness, body_mass_index, blood_pressure_systolic, blood_pressure_diastolic, daily_steps_count
  + Daily/Weekly Habits - weekly_work_hours, hobbies_count, social_events_per_month, books_read_per_year, volunteer_hours_per_month, travel_frequency_per_year
  + Instagram Usage & Engagement - daily_active_minutes_instagram, sessions_per_day, posts_created_per_week, reels_watched_per_day, stories_viewed_per_day, likes_given_per_day, comments_written_per_day, dms_sent_per_week, dms_received_per_week, ads_viewed_per_day, ads_clicked_per_day, time_on_feed_per_day, time_on_explore_per_day, time_on_messages_per_day, time_on_reels_per_day, followers_count, following_count, notification_response_rate, average_session_length_minutes, content_type_preference, preferred_content_theme, privacy_setting_level, two_factor_auth_enabled, biometric_login_used, linked_accounts_count, subscription_status, user_engagement_score, account_creation_year, last_login_date, uses_premium_features
Core Objective: to know the correlation between different demographic, lifestyle and habits on time spent on instagram.
# Data Preprocessing
# CLEAN FRAMEWORK
# C - Conceptualize the data by:
* finding what each row represents
	* Each row represents a unique user with their demographic information, lifestyle, habits and their instagram usage engagement. 
* identifying key metrics by column
	- daily_active_minutes_instagram	
	- sessions_per_day
	- average_session_length_minutes	
	- user_engagement_score
	- identifying key dimensions by column
	- age	
	- gender
	- country
	- urban_rural
	- income_level
	- employment_status
	- education_level
	- relationship_status
	- has_children
	- diet_quality	
	- smoking	
	- alcohol_frequency
	- exercise_hours_per_week	
	- sleep_hours_per_night
	- daily_steps_count
	- account_creation_year
	- content_type_preference	
	- preferred_content_theme	
	- privacy_setting_level
# L - Locate Solvable Problems where we might find:
- create an issues log
<img width="666" height="120" alt="image" src="https://github.com/user-attachments/assets/8dcb462b-4329-498c-8406-ad573d29bf23" />

* error encoding with the word Bachelor’s and Masteral’s due to the UTF-8 encoding problem. it happens due to the character ’ is a special/curly apostrophe, not the normal apostrophe '.
<img width="1647" height="631" alt="image" src="https://github.com/user-attachments/assets/3721779f-e46c-49d9-8979-bacd164d087d" />

* Resolution: using the find and select, input the selected word Masterâ€™s & Bachelorâ€™s and replace it with “Bachelor” and “Masteral.”
<img width="1647" height="660" alt="image" src="https://github.com/user-attachments/assets/67bbe5cd-c35f-4119-b4c1-b0a8497235c6" />
<img width="1648" height="792" alt="image" src="https://github.com/user-attachments/assets/534649e7-eb90-445e-a79c-3a65423a4206" />

* duplicates: checked for duplicate rows by selecting transform data in the home ribbon tab. selected all columns by using ctrl + a keys under keep rows, select keep duplicates in order to see if there are any duplicated rows. Our table showed no duplicates, as shown below.
# E - Evaluate Unsolvable Issues:
Note: In this case, our dataset consists of synthetic data generated by the author. Upon reviewing the table, we found no issues that require correction. Therefore, the following steps will not be applied:
* Handling missing values
* Identifying outliers
* Verifying business logic
# A - Augment the Data:
Since the dataset is synthetic and generated by the author, it already contains representative values for all fields. since the data is synthetic 
# N - Note and Document
<img width="1681" height="352" alt="image" src="https://github.com/user-attachments/assets/633fd8b8-0af0-4716-87db-e3c2fd236564" />
# 3. Data Modeling (Star Schema)
<img width="1126" height="675" alt="image" src="https://github.com/user-attachments/assets/ff0998d6-9ba5-49ef-a5cf-9ee41432a970" />
# Fact table
<img width="1602" height="822" alt="image" src="https://github.com/user-attachments/assets/2ed31906-6e54-4ed2-84f2-bb98f6e619a7" />

# Dim user
<img width="1631" height="791" alt="image" src="https://github.com/user-attachments/assets/8aa60a69-9123-4452-b316-943da041aa71" />

# Dim country
<img width="1687" height="795" alt="image" src="https://github.com/user-attachments/assets/3aa5255a-d438-44e6-8502-b83a968c6a37" />

# Dim healthy lifestyle
<img width="1625" height="813" alt="image" src="https://github.com/user-attachments/assets/fabb70c0-3a27-4f00-80db-d0fd64a9f4db" />

# Dim content preference
<img width="1632" height="627" alt="image" src="https://github.com/user-attachments/assets/155ee603-78ce-4b72-9cec-39be4f3a6f37" />

# Dim date created
<img width="1631" height="782" alt="image" src="https://github.com/user-attachments/assets/8142b120-ecef-4a6e-8d21-a0b03f5f6f32" />

**Descriptive Analysis**
This dataset contains 134656 synthetic records of instagram usage per user. It is composed of key themes with the following demographics, backgrounds, lifestyle, habits, and user engagement. These columns will give us an insightful view regarding the usage of instagram per user. Descriptive analysis is used here to summarize, organize, interpret, and present data. 
The following are some of the findings this dataset has shown:
**Daily instagram usage across Age groups**
<img width="818" height="621" alt="image" src="https://github.com/user-attachments/assets/b46f3c97-b73d-4dbb-9e1a-4bdfdc3fc53f" />

This table shows the total Instagram usage per day  across different age groups. The 25–34 and 35–44 age groups have the highest daily usage, while the below-18 group has the lowest. This suggests that millennials and early Gen X users (ages 25–44) are the most active on Instagram. 

**Instagram usage, Happiness, and stress by Age_group**
<img width="677" height="426" alt="image" src="https://github.com/user-attachments/assets/0697b629-ae1e-4dee-9bbd-cccd5cbe3730" />

There is a negative trend between Instagram usage and stress/happiness: younger users spend more time on Instagram but report lower happiness, while older users spend less time but experience higher stress. Instagram usage declines with age, but perceived stress increases with age. This chart highlights how Instagram engagement and mental well-being metrics vary across age groups, helping to identify patterns for targeted interventions or further analysis.

**Session Length Trends by Account Age: Exploring User Behavior Over Time**
<img width="538" height="331" alt="image" src="https://github.com/user-attachments/assets/4d8b513c-1f82-41b7-b1e2-c6078baef9ea" />

The graph suggests that average daily session activity stays relatively stable across different account creation years, with only small fluctuations over time. Users from all account ages tend to have similar engagement levels, although accounts created around 2015 and 2021 show slightly higher session activity compared to other years.

# Visualization & Dashoard (Dash Framework)

# WIREFRAME
**OVERVIEW DASHBOARD**
<img width="1672" height="941" alt="348de8c5-c8d5-40e6-b936-e0d5bf75ee07" src="https://github.com/user-attachments/assets/66d0ce9a-1836-4bd0-a9c1-c5721eb4ef2f" />

**LIFESTYLE DASHBOARD**
<img width="1672" height="941" alt="26fd9c70-17ff-4be1-b40e-f79f37648fe3" src="https://github.com/user-attachments/assets/83f663a3-665f-4bb4-a084-8cd525f787e3" />

**ENGAGEMENT DASHBOARD**
<img width="1672" height="941" alt="4b5ea4d4-4635-4c77-a70a-e908173466f8" src="https://github.com/user-attachments/assets/7cadf363-53d0-4d0c-af82-e89caa88c8b6" />

# The Pyramid Framework (Metrics & KPIs)
<img width="1102" height="97" alt="image" src="https://github.com/user-attachments/assets/443cbf4b-35a7-423b-9250-b725a8f3b2b4" />

* For the Overview we generated the following using the card visual which are the:
	* Average_session_length_minutes
	* Average_user_engagement_score
	* Average_daily_minutes_on_instagram

<img width="1127" height="111" alt="image" src="https://github.com/user-attachments/assets/4dd86597-fba4-4265-bf82-bcea6d9ad593" />
* In the Lifestyle Dashboard we used the following for the KPI:
	* Average of sleep_hours_per_night
	* Average Exercise Hours
	* Average of perceived_stress_score
**Note: We use these KPIs to show the average lifestyle and well-being of users, including how much they sleep, how active they are, and their perceived stress levels. This allows us to compare trends across age groups, gender, and other demographic dimensions to understand patterns in user health and habits. **

<img width="1136" height="142" alt="image" src="https://github.com/user-attachments/assets/11078b3a-9c27-4bb2-9aa9-85901a781bac" />
* lastly, in the user_engagement we used the following: 
	* total instagram time per day
	* Engagement Actions per Day

**Meausres/Columns use:**
* For total hours in instagram
`Total of hours in instagram =
(COALESCE([time_on_feed_per_day], 0) +
COALESCE([time_on_explore_per_day], 0) +
COALESCE([time_on_messages_per_day], 0) +
COALESCE([time_on_reels_per_day], 0)) / 60`
* Age group
`Age group = 
SWITCH(
    TRUE(),
    [age] < 18, "Below 18",
    [age] <= 24, "18-24",
    [age] <= 34, "25-34",
    [age] <= 44, "35-44",
    [age] <= 54, "45-54",
    "55+"
)`
* BMI CATEGORY
`BMI Category = 
SWITCH(
    TRUE(),
    [body_mass_index] < 18.5, "Underweight",
    [body_mass_index] >= 18.5 && [body_mass_index] < 24.9, "Normal weight",
    [body_mass_index] >= 25 && [body_mass_index] < 29.9, "Overweight",
    [body_mass_index] >= 30, "Obese",
    "Unknown"
)`
# CHART
**OVERVIEW: DEMOGRAPHICS**
<img width="953" height="538" alt="image" src="https://github.com/user-attachments/assets/a85e9ced-0a29-4d6f-88ac-f8fcf2608eaa" />

1. Daily Active Minutes by Gender: Shows the distribution of daily active minutes among Female, Male, Non-binary, and Prefer not to say users.
2. Daily Instagram Usage Across Age Groups: Displays total Instagram usage per day across different age groups.
3. Employment Status Distribution: Compares the number of users and their income levels by employment status.
4. Total Hours in Instagram (by Children): Compares total Instagram hours between users with and without children.
5. Total Hours in Instagram (by Relationship Status): Shows total Instagram hours based on relationship status.
6. Instagram Usage and Engagement by Education Level: Displays total hours and user engagement across different education levels.
7. User Engagement Score by Age: Shows the average user engagement score for different age groups.

**LIFESTYLE DASHBOARD**
<img width="1141" height="555" alt="image" src="https://github.com/user-attachments/assets/fa8ae2c8-46ca-4dcd-a758-9e1315b489dd" />
1. Total Hours in Instagram by BMI Category: Shows total Instagram usage based on users’ BMI categories.
2. Sleep, Exercise, and Instagram Engagement by Age Group: Displays average sleep hours, exercise hours, and user engagement scores across different age groups.
3. Instagram Usage by Alcohol Frequency: Shows Instagram usage distribution based on how often users consume alcohol.
4. Total Instagram Hours by Diet Quality: Compares total Instagram hours according to users’ self-reported diet quality.
5. Instagram Usage, Happiness, and Stress by Age Group: Displays Instagram usage hours, self-reported happiness, and perceived stress scores across age group

**ENGAGEMENT DASHBOARD**
<img width="928" height="517" alt="image" src="https://github.com/user-attachments/assets/2c66491d-5811-4f90-af30-f793182310e1" />

1. Posts Created vs Engagement: Shows the relationship between number of posts created per week and average user engagement score.
2. n Age-Based Comparison of Engagement Activities: Displays engagement activities (likes, comments, posts) and overall engagement score by age group.
3. Time Spent on Instagram Sections: Age Group Breakdown: Compares time spent on exploring, scrolling in feed, chatting, and reels across different age groups.
4. Session Length Trends by Account Age: Shows average number of Instagram sessions per day based on account creation year.

# 5. Insights and Recommendations
**Overview dashboard**
The dashboard reveals that social media engagement is heavily shaped by demographic and lifestyle factors, particularly age, gender, employment status, and social status. Younger users, especially those aged 18–34, dominate Instagram activity and contribute the highest engagement levels. This shows that social media has become an important part of entertainment, communication, and self-expression for younger people. In a real-world context, businesses, marketers, and digital platforms must adopt data-driven strategies to better understand audience behavior and optimize user experiences. Social media companies should prioritize personalized content delivery, mental health initiatives, and creating balanced engagement to keep users satisfied while avoiding too much screen time. These insights can also help businesses improve advertising, online campaigns, and customer interaction in today’s digital world.


**User engagement in terms of different activities, account, and trends**
The dashboard reveals that user engagement on Instagram is strongly influenced by different activities, content preferences, and account behavior. Features such as reels, explore pages, and frequent posting encourage users to spend more time on the platform. Younger users, especially those aged 18–24, show the highest levels of interaction, content creation, and engagement compared to older age groups. This shows that younger users are more attracted to fast, entertaining, and visually appealing content, which reflects current social media trends and changing online behavior. In a real-world context, businesses and content creators can use these insights to create more effective digital strategies and improve audience engagement. Brands should focus on producing creative and interactive content that matches user interests and viewing habits. Social media platforms can also improve user experience by recommending relevant content, supporting meaningful interactions, and promoting responsible social media use. These insights can help businesses strengthen brand awareness, improve online communication, and build stronger relationships with users in today’s fast-growing digital world.

**Lifestyle dashboard**
The dashboard reveals that Instagram usage is closely connected to lifestyle habits, physical health, and emotional well-being. Factors such as sleep, exercise, stress, diet quality, and alcohol consumption all appear to influence how users interact with social media. Younger users continue to spend the most time online, while lifestyle patterns and personal habits affect engagement levels across different age groups. This shows that heavy social media usage may be linked to stress and unhealthy routines when not properly balanced with physical activity, sleep, and healthy habits. In a real-world context, businesses, health organizations, and social media platforms can use these insights to promote healthier digital habits and more positive online environments. These findings can also help improve wellness campaigns, educational content, and responsible social media strategies in today’s digital world.







fill up the resolution column

