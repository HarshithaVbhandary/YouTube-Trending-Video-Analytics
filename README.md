# 📊 YouTube Trending Video Analytics

This project analyzes YouTube trending videos across **India (IN)** and **United States (US)** to uncover trends in video categories, sentiments, regional preferences, and viewer engagement.

---

## 🎯 Objective
To uncover patterns in YouTube trending videos by analyzing multi-region datasets, with a focus on:
- Most popular video genres
- Sentiment analysis of video titles
- Trending duration patterns
- Regional viewership behavior

---

## 🧰 Tools Used
- **Python**: Data cleaning, sentiment analysis, visualizations (Matplotlib, Seaborn)
- **Pandas & NumPy**: Data manipulation
- **TextBlob**: Sentiment polarity of video titles
- **SQL-style queries**: Category ranking by views
- **Power BI**: Dashboarding and interactive reports

---

## 🧹 Methodology

### 1. Data Cleaning
- Datasets: `USvideos.csv`, `INvideos.csv` (from Kaggle)
- Removed duplicates by `video_id`, `title`, `region`
- Converted `trending_date` and `publish_time` to datetime
- Merged datasets using `pd.concat()`

### 2. Sentiment Analysis
- Applied `TextBlob` on video titles
- Created new column: `title_sentiment` (range: -1 to 1)

### 3. SQL-style Analysis (using Pandas)
```sql
SELECT category_id, AVG(views) AS avg_views
FROM youtube_trending
GROUP BY category_id
ORDER BY avg_views DESC;

4. Trending Duration Calculation
trending_duration = trending_date - publish_time

📊 Visualizations
Python Visuals (Matplotlib/Seaborn)
Histogram: Distribution of trending durations

Bar Chart: Average views by category

Line Chart: Average trending duration over time

Bar Plot: Sentiment by region

Power BI Dashboard Includes:
Card/KPI: Total views, average sentiment, total videos

Gauge: Total views vs benchmark

Filled Map: Views by region

Scatter Plot: Views vs comment count

Donut Chart: Video count by region

Line Charts: Views over time, Trending duration trends

📌 Key Insights
🔹 Most Popular Genres
Music and Entertainment consistently receive highest average views.

🔹 Sentiment Patterns
US titles are slightly more positive on average.

India shows more sentiment diversity (emotional and trending).

🔹 Trending Duration
Most videos trend for just 1–3 days.

US videos tend to remain trending longer than Indian videos.

🔹 Region-Wise Comparison
US has higher average views.

India publishes more trending videos, but with shorter durations.





