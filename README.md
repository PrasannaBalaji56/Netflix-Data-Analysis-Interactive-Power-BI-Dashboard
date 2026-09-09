# 🎬 Netflix Data Analysis & Power BI Dashboard

## 📌 Project Overview

This project analyzes Netflix content and customer viewing behavior using **Power BI**.

The dashboard combines Netflix content data with customer viewing and rating data to understand content performance, customer engagement, ratings, geographical patterns, age-group behavior, and subscription preferences.

The project focuses on transforming raw data into meaningful business insights through data cleaning, analysis, DAX measures, and interactive Power BI visualizations.

---

## 🎯 Project Objectives

The main objectives of this project are:

- Analyze customer demographics and viewing behavior
- Identify the most-watched Netflix content
- Compare Movies vs TV Shows based on watch time
- Analyze genre popularity and performance
- Analyze customer ratings
- Compare ratings across countries and age groups
- Understand subscription plan distribution and engagement
- Analyze watch time across subscription types
- Identify geographical differences in engagement and ratings
- Analyze director performance based on user ratings
- Support content localization and subscription strategy decisions

---

## 📊 Dashboard Pages

### 1. 🎬 Content Wise Analysis

This page focuses on Netflix content performance and viewing behavior.

### Key Analysis:
- Total watch time
- Total users
- Total titles
- Average customer rating
- Watch time by age group
- Top 10 most-watched titles
- Watch time by country and genre
- Movie vs TV Show watch time
- Genre filtering

### Key Finding:
The dashboard shows differences in viewing behavior across age groups, countries, genres, and content types. The **60+ age group records the highest total watch time** among the analyzed age groups.

---

### 2. 👥 Age & Subscription Wise Analysis

This page analyzes customer demographics and subscription behavior.

### Key Analysis:
- Average watch time
- Most popular subscription plan
- Subscription percentage
- Most popular age group
- Total shows watched
- Age group vs subscription type
- Subscription type vs watch time
- Watch time by genre and age group

### Key Findings:
- **Standard** is the most popular subscription plan in the analyzed customer dataset.
- The **60+ age group** has the highest customer representation in the dashboard.
- Subscription plans show differences in customer activity and average watch time.
- Age groups demonstrate different viewing and subscription patterns.

---

### 3. ⭐ Rating & Country Wise Analysis

This page focuses on customer satisfaction and geographical performance.

### Key Analysis:
- Average rating and watch time by country
- Rating distribution by country
- Average rating by director
- Rating by age group
- Country vs watch time
- Country, genre, age-group, and month filters

### Key Findings:
- **South Korea and Japan** record the highest average rating at approximately **3.04**.
- **India and Australia** record comparatively lower average ratings at approximately **2.98**.
- Watch time also varies across countries, showing differences in customer engagement.
- Combining ratings with watch time provides a better view of both **customer satisfaction and engagement**.

---

## 💡 Business Insights

### 🌍 Content Localization

Country-level differences in watch time and ratings indicate that customer preferences are not uniform across markets.

Netflix can improve engagement by:

- Increasing relevant regional content
- Promoting locally preferred genres
- Improving localized recommendations
- Studying content gaps in lower-performing markets
- Using country-level viewing behavior for content planning

---

### 👥 Customer Segmentation

Age-group analysis shows that customer behavior differs between demographic segments.

Netflix can use age-based viewing patterns to:

- Improve personalized recommendations
- Promote relevant genres to different age groups
- Understand high-engagement customer segments
- Design targeted content strategies

---

### 💳 Subscription Strategy

The subscription analysis shows differences in customer distribution and viewing behavior across Basic, Standard, and Premium plans.

Netflix can use these patterns to:

- Understand which plans attract more customers
- Identify highly engaged subscription segments
- Improve plan-specific recommendations
- Support customer retention strategies

---

### ⭐ Ratings & Engagement

Customer ratings provide a measure of satisfaction, while watch time represents engagement.

Using both metrics together provides a stronger understanding of content performance than using either metric alone.

---

## 🛠️ Tools & Technologies

- **Microsoft Excel** – Data cleaning and preprocessing
- **Power BI** – Data modeling, DAX, visualization, and dashboard creation
- **DAX** – Measures and calculations
- **Power Query** – Data transformation
- **GitHub** – Project documentation and version control

---

## 📂 Datasets

The project uses two datasets:

### Netflix Shows Dataset

Contains information about Netflix content including:

- Show ID
- Type
- Title
- Director
- Cast
- Country
- Date Added
- Release Year
- Rating
- Duration
- Genre

### Netflix Customer Dataset

Contains customer viewing and rating information including:

- Customer ID
- Show ID
- Customer Name
- Age
- Gender
- Country
- Subscription Type
- Watch Time
- Customer Rating

The customer rating is measured on a **1–5 scale**.

---

## 🧹 Data Cleaning & Preparation

The data preparation process included:

- Handling missing values
- Checking data consistency
- Standardizing date fields
- Creating age groups
- Preparing categorical fields
- Checking rating values
- Preparing data for Power BI analysis

---

## 📈 Key DAX Measures

Examples of measures used in the dashboard:

```DAX
Total Customers =
DISTINCTCOUNT(customer[customer_id])


TOTAL USERS =
DISTINCTCOUNT(netflix_customer_ratings_20000[customer_id])

TOTAL WATCHING =
SUM(netflix_customer_ratings_20000[watch_time_minutes])

Added =
IF(
    'netflix_dataset_20000 csv'[date_added] >= EDATE(TODAY(), -24),
    "Recently Added",
    "Older"
)


TOTAL TITLE =
COUNT('netflix_dataset_20000 csv'[title])


age group =
IF(
    netflix_customer_ratings_20000[age] <= 18,
    "13-18",
    IF(
        netflix_customer_ratings_20000[age] <= 30,
        "19-30",
        IF(
            netflix_customer_ratings_20000[age] <= 45,
            "31-45",
            IF(
                netflix_customer_ratings_20000[age] <= 60,
                "46 - 60",
                "60+"
            )
        )
    )
)

Column =
IF(
    netflix_customer_ratings_20000[watch_time_minutes] > [avg watch time],
    "Heavy watcher",
    "normal watcher"
)




| DAX Function      | Purpose                                                                    |
| ----------------- | -------------------------------------------------------------------------- |
| `SUM()`           | Calculates total values such as shows watched and watch time               |
| `DISTINCTCOUNT()` | Counts unique customers                                                    |
| `COUNT()`         | Counts the number of titles                                                |
| `IF()`            | Creates conditions and classifications                                     |
| `EDATE()`         | Calculates a date a specific number of months before or after another date |
| `TODAY()`         | Returns the current date                                                   |

```
---

## 📸 Dashboard Screenshots

### 🏠 Dashboard Home Page

<img width="1283" height="719" alt="Screenshot 2026-09-08 004514" src="https://github.com/user-attachments/assets/17e0f23e-b190-4377-8887-f7ae609b2cf5" />
<img width="1279" height="717" alt="Screenshot 2026-09-08 004531" src="https://github.com/user-attachments/assets/0550495f-b190-4d41-9a9d-d17fe3ba75e7" />
<img width="1275" height="722" alt="Screenshot 2026-09-08 004546" src="https://github.com/user-attachments/assets/7fa6cdb4-2177-46b8-a247-8383016b8721" />
<img width="1280" height="720" alt="Screenshot 2026-09-08 004504" src="https://github.com/user-attachments/assets/e938c62e-137a-4332-9ba2-8b076ee63a0c" />
