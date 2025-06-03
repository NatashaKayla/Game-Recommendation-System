# 🎮 Game Recommendation System - EDA & Feature Analysis

This project analyzes a video game dataset to uncover patterns in game genres, platforms, ratings, and popularity. These insights form the foundation for understanding the gaming market and user engagement.

---

## 🎯 Main Objectives

* Clean and preprocess the dataset for analysis
* Explore genre, rating, platform, and sales trends
* Visualize feature distributions and relationships
* Extract actionable insights to understand user and market behavior

---

## 🧾 Dataset Description

The dataset contains information on video games and their performance across different markets. Key features include:

| Feature               | Description                                  |
| --------------------- | -------------------------------------------- |
| **Name**              | Game title                                   |
| **Platform**          | Gaming platform (e.g., PS2, X360, PC)        |
| **Year\_of\_Release** | Year the game was released                   |
| **Genre**             | Primary genre (e.g., Action, Sports, Puzzle) |
| **Publisher**         | Game publisher                               |
| **NA\_Sales**         | Sales in North America (in millions)         |
| **EU\_Sales**         | Sales in Europe                              |
| **JP\_Sales**         | Sales in Japan                               |
| **Other\_Sales**      | Sales in other regions                       |
| **Global\_Sales**     | Total worldwide sales                        |
| **Critic\_Score**     | Score from professional critics              |
| **Critic\_Count**     | Number of critic reviews                     |
| **User\_Score**       | Average user score                           |
| **User\_Count**       | Number of user ratings                       |
| **Developer**         | Developer name                               |
| **Rating**            | ESRB rating (e.g., E, T, M)                  |

---

## 🧹 Data Cleaning Steps

* **Dropped identifiers** such as index and redundant columns
* **Handled duplicates** and removed exact game duplicates
* **Handled missing values** in columns like `User_Score`, `Critic_Score`, and `Year_of_Release`
* **Filtered anomalies**, such as:

  * `User_Count` < 0
  * `Year_of_Release` < 1950
  * Negative numeric values replaced with the positive median

---

## 📊 Exploratory Data Analysis (EDA)

The analysis focused on visualizing data distributions and uncovering patterns:

### 🔍 Feature Distributions

* Count plots for **Genre**, **Rating**, and **Platform**
* Bar plot of **Top 5 Publishers**
* Distribution of **Rating per Genre**
* Frequency of each **Game Genre**

### 📈 Highlighted Visuals

* **Top 10 Games** by global popularity
* **Heatmap** showing correlation between numerical features
* **Distribution checks** for User Scores and Critic Scores

---

## 📌 Key Insights

* **Action** is the most frequent genre, followed by **Sports** and **Miscellaneous**
* **Electronic Arts** leads in **Sports** games; **Ubisoft** and **Activision** dominate **Action**
* Family-friendly genres like **Racing and Simulation** are rated **E (Everyone)**
* Mature genres like **Shooter and Action** are often rated **T** or **M**
* **Need for Speed: Most Wanted** is among the most popular titles
* **LEGO** and **FIFA** franchises show consistent popularity across the dataset

---

## 📌 Conclusion

* The dataset reveals clear patterns in game genres, publishers, and player preferences
* Action and Sports dominate the market, while genres like Puzzle and Strategy remain niche
* ESRB ratings align well with genre types—family-friendly games trend toward "E", while mature content appears in Shooter/Action
* Certain franchises like **LEGO** and **FIFA** consistently attract large audiences
* These insights offer valuable direction for future analysis or building recommendation systems
