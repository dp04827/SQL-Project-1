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

# **Database Information**  
Name of the database- al_Group_21484_G3












