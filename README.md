# SQL Project 1 - Fitness App

# Team Name:
21484 Group 3

# **Group Members**
1. Elle Wolf  
2. Dev Patel  
3. Jim Jones  
4. Justin Lee  
5. Chris DiBiasi  

# **Problem Description**

  The task at hand is to model and build a relational database for the general operations of a fitness and health app that collects and analyzes daily health and fitness data from its users. The central entity in the model is the Person entity, who is the user of the app. The goal is for each individual who registers on the app to track their exercise, nutrition, sleep, and overall health.
The app provides various features, including workout plans, diet tracking, activity monitoring, and personalized coaching, all of which are linked to user engagement and fitness progress. We aim to accurately model the relationships between users, their fitness activities, nutritional habits, health metrics,  and subscription plans. Additionally, we will generate sample data to populate into our entities and their attributes. Finally, we will perform functional queries on this dataset to extract valuable insights regarding user behavior, workout effectiveness, engagement trends, and overall app performance.  

# **Data Model**  
<img width="1073" alt="image" src="https://github.com/user-attachments/assets/fb345639-bdb8-4ea5-8d0b-797a908e2d07" />  


### **Data Model Explanation**  
Our model is based on the structure of a hypothetical fitness app. The **Person** entity is representative of the person using the app, and we collect different data points related to their health metrics. The idea behind the app is to help users reach their fitness goals. For example, a user may want to run a faster mile. Our app, “SQL Fit”, is able to track the users progress through their input of data. Things like minutes exercised, heart rate, and calories burned are all collected. These metrics are vital to the app to make predictions on how to help the user reach their goal.  

Our group has included a few one-to-many relationships between **Person** and other attributes. Many of them are in relation to other entities without a further relationship attached, like a dead-end relationship. For these cases, our group felt that there are no other entities that are necessary to further expand upon. The **Person** entity itself is composed of relevant attributes of the user, such as their name, date of birth, gender, and age. **Person** can log their weight as many times as they would like, forming a one-to-many relationship to **Weight**. This includes information on their weight, body fat percentage, muscle mass, and the date logged. Similarly, **Person** can log their sleep whenever they would like, forming another one-to-many relationship with **SleepData**, logging the date, their sleep quality, and hours slept. **BloodPressure** logs systolic pressure, diastolic pressure, as well as date and time measured. **MentalHealth** logs mood, stress, energy levels, and date logged. **BodyTemperature** logs body temperature, temperature status, chills (yes/no), and time / date measured. **Nutrition** logs grams of protein, carbohydrates, fats, and sugar consumed. It also logs calories consumed, water intake, and date logged.  

A large portion of what we would like this app to be used for is fitness. Many of the entities are connected in more complex ways than just a one-to-many relationship with **Person**, like in the paragraph above. To start, a one-to-many relationship is formed with **Person** and **DailyActivity**. This serves as basic data on **Person’s** steps taken, calories burned, and the date. This entity then feeds into **Workout**, because someone’s **DailyActivity** can comprise of many different **Workouts**. Workout includes the date and time the workout is completed. One **Workout** session can consist of many different **Exercises**. **Exercise** consists of minutes exercised, calories burned, and type of exercise. Connected to each of these entities through a one-to-many relationship is **HeartRate**. Both an **Exercise**, such as a pushup, and a **Workout**, such as the session itself, should also have **HeartRate** attached, including min / max BPM (beats per minute) and the status of BPM. **Exercise** and **CardioGoals** form a many-to-many relationship, with **ProgressTracker** as their associative entity. Exercises can have many **CardioGoals**, and vice versa. **CardioGoals** consists of min/max mile time minutes, as well as a target mile time. 



# **Data Dictionary**  
<img width="772" alt="image" src="https://github.com/user-attachments/assets/ba21ccd2-f4b8-4fc4-a214-8484c0e772e0" />
<img width="892" alt="image" src="https://github.com/user-attachments/assets/fe493bf7-ac99-4a70-9f57-dcfbb9d34fe9" />
<img width="891" alt="image" src="https://github.com/user-attachments/assets/c0c425b1-4568-41e3-b614-1736d447ec32" />
<img width="890" alt="image" src="https://github.com/user-attachments/assets/67d519a9-4973-4e10-9e0c-201bb7e75ed9" />
<img width="889" alt="image" src="https://github.com/user-attachments/assets/028013ec-741d-44f0-8bdd-ef36dfc420e9" />
<img width="894" alt="image" src="https://github.com/user-attachments/assets/37417b14-db9f-4a6b-b6f0-fe7457f6d9ec" />
<img width="631" alt="image" src="https://github.com/user-attachments/assets/687ba954-83d6-4832-93d1-cfd8d089ea5a" />
<img width="788" alt="image" src="https://github.com/user-attachments/assets/9a48880d-7312-4d13-9b37-cbf5d0e8a699" />
<img width="793" alt="image" src="https://github.com/user-attachments/assets/f8583083-802a-4978-a248-4f95adb962c5" />
<img width="793" alt="image" src="https://github.com/user-attachments/assets/c2f87e18-45a0-4282-91d0-20622827e3d5" />
<img width="796" alt="image" src="https://github.com/user-attachments/assets/2dd76d6a-cafb-4771-afdb-09072c1746a4" />
<img width="791" alt="image" src="https://github.com/user-attachments/assets/25181d09-232e-44fe-9d64-60ab8abc6ba2" />
<img width="794" alt="image" src="https://github.com/user-attachments/assets/75a8073f-dc97-47eb-a8f1-c50e03cf6ede" />















 


# **Ten Queries** 
## Simple Queries
1. **Retrieve all users who have registered in the system.**
   - **Purpose:** Managers need to know how many users have signed up to track growth and engagement.
<img width="403" alt="image" src="https://github.com/user-attachments/assets/16fdc4c9-c25c-4e61-85f1-3d42bd6279c5" />

  
2. **Get the percent of sleep a user was in REM sleep for and the date logged.**
   - **Purpose:** Managers could use this to assess sleep habits and overall quality of sleep for users.
<img width="569" alt="image" src="https://github.com/user-attachments/assets/28de916b-2c2a-4d83-b409-82443a12bf5f" />


  
3. **Retrieve the calories consumed and water intake from a user.**
   - **Purpose:** This query helps the app collect the most basic nutrition data from users to make dietary recommendations.
<img width="395" alt="image" src="https://github.com/user-attachments/assets/810ae4d4-cf9f-448d-b515-728deaa0e5db" />

4. **Get the total hours of sleep recorded for a user in the last month.**
   - **Purpose:** Managers would use this to analyze user sleep patterns and how they correlate with fitness goals.
  <img width="473" alt="image" src="https://github.com/user-attachments/assets/19d7ea19-322a-4aae-9d7f-9c44f955fc44" />





### Complex Queries 
5. **Retrieve the average heart rate during workouts, along with the average calories burned.**
   - **Purpose:** This helps managers understand the intensity of workouts and how effective they are for users’ fitness goals.
<img width="460" alt="image" src="https://github.com/user-attachments/assets/d5feff7f-9f11-4df9-bc37-817b62c75b95" />

6. **Get users who have a weight loss goal and have burned more than 300 calories in the past week.**
   - **Purpose:** Managers would care about tracking the effectiveness of fitness plans and motivating users toward their goals.
<img width="276" alt="Screenshot 2025-03-20 at 7 08 58 PM" src="https://github.com/user-attachments/assets/581b315a-3b78-4784-b410-121b1676f0ef" />
<img width="159" alt="Screenshot 2025-03-20 at 7 09 16 PM" src="https://github.com/user-attachments/assets/198d5f16-92ec-4822-9f22-b21701af33c5" />


7. **Get the average body temperature of all users on a specific date and compare it to the normal range.**
   - **Purpose:** This query could help monitor users' health and alert managers to any abnormal readings that might indicate health risks.
<img width="839" alt="image" src="https://github.com/user-attachments/assets/988c01d5-4d01-42a0-b098-3e567d2767e4" />


8. **Find the number of users who have logged sleep data and report the average sleep hours per day.**
   - **Purpose:** Managers need to assess user engagement with sleep tracking and the effectiveness of sleep-related recommendations.
<img width="462" alt="image" src="https://github.com/user-attachments/assets/69320cae-cb39-4be2-b378-8af1559e4e5b" />


9. **Retrieve users who have met their fitness goals based on both exercise and diet metrics.**
   - **Purpose:** A manager would need to know which users are achieving their fitness targets to identify success stories or patterns.
<img width="482" alt="image" src="https://github.com/user-attachments/assets/51c61be5-7c97-4987-8272-dad95808dfd1" />

<img width="487" alt="image" src="https://github.com/user-attachments/assets/a11bc2fd-a249-4cd2-83a2-e63611b32800" />



10. **Get the number of calories burned by each user, with their average heart rate, and identify the top 5 most active users.**
    - **Purpose:** Managers can use this data to understand which users are the most engaged and to adjust their strategies accordingly.
<img width="493" alt="image" src="https://github.com/user-attachments/assets/18d375da-941e-4ec1-8902-65c7a3723550" />

<img width="493" alt="image" src="https://github.com/user-attachments/assets/2ef1fb2f-05cf-42db-817a-e6705820ad7a" />












# **Queries**

# **Database Information**  
Name of the database- al_Group_21484_G3











