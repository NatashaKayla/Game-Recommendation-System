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

The dataset contains records of video games and their performance across platforms and regions. Below are the descriptions of each feature:

| Feature               | Description                                                              |
| --------------------- | ------------------------------------------------------------------------ |                                     |
| **Name**              | The name of the game                                                     |
| **Platform**          | The platform for which the game was made                                 |
| **Year\_of\_Release** | The year in which the game was released                                  |
| **Genre**             | The genre of the game                                                    |
| **Publisher**         | The game’s publisher                                                     |
| **NA\_Sales**         | Number of copies sold in North America (millions)                        |
| **EU\_Sales**         | Number of copies sold in Europe (millions)                               |
| **JP\_Sales**         | Number of copies sold in Japan (millions)                                |
| **Other\_Sales**      | Number of copies sold in other countries (millions)                      |
| **Global\_Sales**     | Total number of copies sold globally (millions)                          |
| **Critic\_Score**     | Average score given by game critics (0–100)                              |
| **Critic\_Count**     | Number of game critics that reviewed the game                            |
| **User\_Score**       | Average score given by users (0–10)                                      |
| **User\_Count**       | Number of users playing the game                                         |
| **Developer**         | The game’s developer                                                     |
| **Rating**            | The ESRB categorization (e.g., E = Everyone, T = Teen, M = Mature, etc.) |

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

Terima kasih! Kalau begitu, mari kita tambahkan **bagian baru di README** yang menjelaskan proses **modeling yang kamu lakukan** secara ringkas dan profesional, sesuai dengan pendekatan yang kamu pakai: **content-based filtering dengan TF-IDF dan cosine similarity**.

Berikut ini adalah bagian baru yang bisa langsung ditambahkan di README:

---

## 🧠 Recommendation System Modeling

To move beyond EDA, a simple **content-based recommendation system** was implemented to suggest similar games based on their textual features.

### ✅ Approach Used

1. **Content-Based Filtering**
   Games are recommended based on similarity in their metadata — such as genre, platform, publisher, and other descriptive features.

2. **TF-IDF Vectorization**
   The textual data (especially the `Genre`, `Publisher`, and possibly `Name`) was transformed using **TF-IDF (Term Frequency-Inverse Document Frequency)** to numerically represent game content in a meaningful way.

3. **Cosine Similarity Calculation**
   Pairwise cosine similarity was computed between all TF-IDF vectors to measure how "similar" each game is to the others.

4. **Recommendation Function**
   A custom function was built to return the **top 5 similar games** given a specific game title. This function:

   * Takes a game name as input
   * Retrieves the corresponding TF-IDF vector
   * Calculates similarity with all other games
   * Returns the top matches sorted by similarity score

---

## 📌 Conclusion

* The dataset reveals clear patterns in game genres, publishers, and player preferences
* Action and Sports dominate the market, while genres like Puzzle and Strategy remain niche
* ESRB ratings align well with genre types—family-friendly games trend toward "E", while mature content appears in Shooter/Action
* Certain franchises like **LEGO** and **FIFA** consistently attract large audiences
* These insights offer valuable direction for future analysis or building recommendation systems
