# 🛒 Zepto E-Commerce SQL Data Analysis Project

## 📌 Project Overview

This is a SQL portfolio project where I performed data analysis on an e-commerce inventory dataset scraped from **Zepto**, one of India’s fastest-growing quick-commerce startups.

The objective of this project was to simulate a real-world data analyst workflow:
- Work with raw inventory data  
- Clean and transform messy data  
- Perform exploratory data analysis (EDA)  
- Generate business insights using SQL  

This project reflects practical data analysis tasks commonly performed in retail and e-commerce companies.

---

## 📁 Dataset Details

- Source: Kaggle (Zepto product listing data)
- Each row represents a unique SKU (Stock Keeping Unit)
- Duplicate product names exist due to:
  - Different weights
  - Different packaging
  - Different discounts
  - Multiple category placements  

This mirrors real-world e-commerce catalog structures.

---

## 🧾 Columns Description

| Column Name | Description |
|-------------|-------------|
| sku_id | Unique product ID (Primary Key) |
| name | Product name |
| category | Product category |
| mrp | Maximum Retail Price (converted from paise to ₹) |
| discountPercent | Discount percentage |
| discountedSellingPrice | Final selling price |
| availableQuantity | Units available in stock |
| weightInGms | Weight in grams |
| outOfStock | Stock availability (True/False) |
| quantity | Units per package |

---

## 🔧 Project Workflow

### 1️⃣ Database Creation
Created a PostgreSQL table with appropriate data types and constraints.

### 2️⃣ Data Import
- Imported CSV file using pgAdmin  
- Faced UTF-8 encoding error  
- Resolved by saving file in CSV UTF-8 format  
- Successfully loaded dataset  

### 3️⃣ Exploratory Data Analysis (EDA)
- Counted total records  
- Checked for null values  
- Identified distinct categories  
- Compared in-stock vs out-of-stock products  
- Detected duplicate product entries (multiple SKUs)

### 4️⃣ Data Cleaning
- Removed rows with zero MRP or selling price  
- Converted price from paise to rupees  
- Standardized data for consistency  

### 5️⃣ Business Insights Using SQL
- Top 10 highest discount products  
- High-MRP products currently out of stock  
- Estimated revenue by category  
- Expensive products with minimal discount  
- Top 5 categories with highest average discount  
- Price per gram analysis for value comparison  
- Product grouping by weight (Low, Medium, Bulk)  
- Total inventory weight per category  

---

## 🛠️ How to Run This Project

### Step 1: Clone the Repository
```bash
git clone https://github.com/amlanmohanty/zepto-SQL-data-analysis-project.git
cd zepto-SQL-data-analysis-project
