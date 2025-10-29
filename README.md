 Fitbit Fitness Tracker Data Analysis  

 Project Overview  
This project analyzes "Fitbit fitness tracker data" to uncover insights about user activity, sleep, and calorie patterns. Using Python (Pandas, Matplotlib, Seaborn), the goal was to explore how daily activity levels affect sleep duration and calories burned.  

The project involves "data cleaning, merging, exploratory data analysis (EDA)", and "visual storytelling"through interactive charts. It highlights meaningful relationships between activity, rest, and sedentary behavior — providing a holistic view of user wellness patterns.

---

### Dataset Information  
The datasets are sourced from the **Fitbit Fitness Tracker Data (Kaggle)**.  

- **dailyActivity_merged.csv** — Daily summary of user activity (steps, distance, calories, etc.)  
- **sleepDay_merged.csv** — Sleep duration and quality per user  

After cleaning, both datasets were merged on common fields (`Id` and `ActivityDate`) for analysis.

---

### Data Cleaning Steps  
1. Imported data using `pandas`  
2. Converted `ActivityDate` and `SleepDay` columns to datetime format  
3. Checked and handled missing values using `.isnull().sum()`  
4. Removed duplicates using `.drop_duplicates()`  
5. Merged datasets using:
   ```python
   merged = pd.merge(daily, sleep, on=['Id', 'ActivityDate'], how='outer')

### Exploratory Data Analysis (EDA)
1. Steps Over Time

Visualized total steps per day to identify user activity trends.

**Insight: Most users show fluctuations in daily steps, indicating inconsistent activity levels.**

**2. Activity vs Sleep**

Scatter plot comparing total steps and total minutes asleep.

**Insight: Slight positive correlation — more active users tend to sleep slightly longer.**

** 3. Average Steps by Weekday**

Bar chart showing average steps for each day of the week.

**Insight: Activity levels are higher midweek and drop on weekends.**

 **4. Calories Burned Distribution**

Histogram of calories burned per day.

**Insight: Most users burn between 1,700–2,500 calories daily.**

**5. Top 5 Most Active Users**

Bar chart showing the users with the highest total steps.

**Insight: Top 5 users recorded over 40,000 steps, showing consistent engagement.**

**6. Correlation Heatmap**

Heatmap showing relationships between activity, sedentary, and sleep metrics.

**Key Findings:**
Steps ↔ Distance: 0.99 (very strong correlation)

Calories ↔ Activity: 0.59 (moderate positive correlation)

SedentaryMinutes ↔ Calories: -0.33 (negative correlation)

Sleep ↔ Activity: Weak correlation (~0.1)

### Key Insights Summary
**Observation	Insight**
🏃 Steps vs Distance	Strong correlation (r = 0.99). More steps = greater distance.
🔥 Calories Burned	Positively correlated with total steps and distance.
🪑 Sedentary Time	Negatively correlated with steps (-0.29) and calories (-0.33).
😴 Sleep Duration	Weakly correlated with physical activity — indicates other influencing factors.
👣 Top Active Users	Top 5 users maintained over 40K total steps, showing consistent movement.
🧰 Technologies Used

## Python Libraries

**pandas** → Data manipulation and cleaning

**matplotlib** → Visualizations

**seaborn**→ Statistical charts and heatmaps

**numpy** → Numerical operations

## Possible Improvements
-Add weight logs and heart rate data for deeper correlation studies.
-Create a Power BI dashboard summarizing the findings visually.
-Apply clustering or regression to predict calorie burn based on activity.

## Conclusion

This analysis highlights how daily movement, sleep, and sedentary time interact to shape user health trends.
While higher activity correlates with better calorie expenditure, sleep quality appears largely independent — suggesting that achieving balanced wellness requires a combination of activity, rest, and recovery.

 ## Author

Insherah Majid
Data Analyst | Python | Power BI | SQL
📍 Srinagar, kashmir

🔗 Connect with me:

LinkedIn

GitHub

- Visuals Included
- Average Steps by Weekday
- Activity vs Sleep Scatter Plot
- Calories Burned Distribution
- Top 5 Most Active Users
- Correlation Heatmap

⭐ If you find this project insightful, consider giving it a star on GitHub!




