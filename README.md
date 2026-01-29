# 📊 BlinkIT Sales Analysis – SQL Case Study

## 📝 Project Overview
This project analyzes **BlinkIT grocery sales data** using **SQL** to uncover key business insights related to product performance, outlet characteristics, customer ratings, and operational efficiency.

The goal is to generate **actionable insights** that can help improve:
- Sales performance
- Shelf space utilization
- Outlet-level strategy
- Product visibility optimization

---

## 🛠️ Tech Stack
- **Database:** SQL (MySQL / PostgreSQL compatible)
- **Analysis Type:** Exploratory Data Analysis (EDA)
- **Dataset:** BlinkIT Grocery Sales Data

---

## 📂 Dataset Description
The dataset contains information on:
- Item details (type, weight, fat content, visibility)
- Outlet details (type, size, location, establishment year)
- Sales and customer ratings

---

## 🧹 Data Cleaning & Preprocessing
Key data cleaning steps included:
- Standardizing `Item_Fat_Content` values
- Creating derived columns for deeper analysis:
  - `Weight_Category`
  - `Age_Category`
  - `Rating_Category`

Example:
```sql
UPDATE blinkit  
SET item_fat_content = CASE  
  WHEN item_fat_content IN ('LF','low fat') THEN 'Low Fat' 
  WHEN item_fat_content = 'reg' THEN 'Regular' 
  ELSE item_fat_content 
END;
