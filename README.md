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
### **Data Model Explanation**  
Our model is based on the structure of a hypothetical fitness app. The **Person** entity is representative of the person using the app, and we collect different data points related to their health metrics. The idea behind the app is to help users reach their fitness goals. For example, a user may want to run a faster mile. Our app, “SQL Fit”, is able to track the users progress through their input of data. Things like minutes exercised, heart rate, and calories burned are all collected. These metrics are vital to the app to make predictions on how to help the user reach their goal.  

Our group has included a few one-to-many relationships between **Person** and other attributes. Many of them are in relation to other entities without a further relationship attached, like a dead-end relationship. For these cases, our group felt that there are no other entities that are necessary to further expand upon. The **Person** entity itself is composed of relevant attributes of the user, such as their name, date of birth, gender, and age. **Person** can log their weight as many times as they would like, forming a one-to-many relationship to **Weight**. This includes information on their weight, body fat percentage, muscle mass, and the date logged. Similarly, **Person** can log their sleep whenever they would like, forming another one-to-many relationship with **SleepData**, logging the date, their sleep quality, and hours slept. **BloodPressure** logs systolic pressure, diastolic pressure, as well as date and time measured. **MentalHealth** logs mood, stress, and energy levels. **BodyTemperature** logs body temperature, temperature status, chills (yes/no), and time / date measured. **Nutrition** logs grams of protein, carbohydrates, fats, and sugar consumed. It also logs calories consumed, water intake, and date logged.  

A large portion of what we would like this app to be used for is fitness. Many of the entities are connected in more complex ways than just a one-to-many relationship with **Person**, like in the paragraph above. To start, a one-to-many relationship is formed with **Person** and **DailyActivity**. This serves as basic data on **Person’s** steps taken and calories burned. This entity then feeds into **Workout**, because someone’s **DailyActivity** can comprise of many different **Workouts**. Workout includes the date and time the workout is completed. One **Exercise** can consist of many different **Workouts**. **Exercise** consists of minutes exercised, calories burned, and type of exercise. Connected to each of these entities through a one-to-many relationship is **HeartRate**. Both an **Exercise**, such as a pushup, and a **Workout**, such as the session itself, should also have **HeartRate** attached, including min / max BPM (beats per minute) and the status of BPM. **Exercise** and **CardioGoals** form a many-to-many relationship, with **ProgressTracker** as their associative entity. Exercises can have many **CardioGoals**, and vice versa. **CardioGoals** consists of min/max mile time minutes, as well as a target mile time. 



# **Data Dictionary**   
| Column Name | Data Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. Id of item to fetch |

# **Ten Queries**  




