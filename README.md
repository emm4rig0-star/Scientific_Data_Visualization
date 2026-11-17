# Scientific_Data_Visualization
# 📱 Social media impact on students' lives

Project for the **Scientific Data Visualization** course.
**Authors:** Luca Perez, Chiara Busacca, Emma Rigo

## 🎯 Objective

Parents say that social media makes you sleep less, lowers your grades, increases stress, and worsens mental health. **Are they right?**
This project uses data and clustering techniques to test this.

## 📊 Dataset

* Source: [https://www.kaggle.com/datasets/harishyadav0506/impact-of-social-media-on-life/data](https://www.kaggle.com/datasets/harishyadav0506/impact-of-social-media-on-life/data)
* 4,500 records and 16 variables (social media usage, sleep quality and duration, stress, mental health, academic performance, platform, etc.)
* After cleaning: **4,369 students**

## 🧹 Data Cleaning

* Removal of null values (131 records)
* Data type conversion and mapping of categorical variables (e.g., `Social_comparison_frequency`: Never=0 … Always=4)
* Conversion of grades from the GPA scale (/4) to the Italian scale (/110)

## 🔬 Methodology

1. **Exploratory analysis**: nighttime usage, social comparison, relationship between hours of sleep, stress, and grades.
2. **Feature selection** (4 out of 16): daily smartphone usage, weekend usage, nighttime usage, social comparison frequency.
3. **PCA** to project the data onto 2 principal components and visualize them.
4. **K-means** to identify groups. The number of clusters **k = 2** was chosen using the silhouette score (0.300).
5. **Cluster analysis**: comparison between the two groups regarding sleep, stress, mental health, and grades, as well as between perception and reality.

## 🔑 Key Findings

| Metric | Cluster 0 · Moderate | Cluster 1 · Intensive |
| --- | --- | --- |
| Hours of sleep | 7.1 | 6.4 |
| Sleep quality | 2.8 | 2.2 |
| Perceived stress | 11.0 | 15.3 |
| Mental health index | 84.8 | 76.3 |
| Average grade (/110) | 97.9 | 91.8 |

* **Verdict: parents are (largely) right.** Intensive use is associated with less sleep, lower grades, and lower well-being.
* Correlations with daily hours of use: sleep ρ = -0.66, stress ρ = +0.70, mental health ρ = -0.80, grades ρ = -0.65.
* **Perception gap**: 74% of intensive users still perceive social media as beneficial.
* Clustering does not separate distinct personas, but rather divides a **continuum**, with a critical threshold of around 4.5–5 hours per day.
* **Habits matter more than platforms**: nighttime usage and duration carry more weight than specific apps.
