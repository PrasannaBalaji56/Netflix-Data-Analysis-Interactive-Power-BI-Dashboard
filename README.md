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
