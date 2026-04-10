**📊 Zepto Business Data Analysis (SQL + Power BI)**
📌 Project Overview

This project focuses on analyzing an e-commerce grocery dataset (Zepto-like) using PostgreSQL and Power BI to derive actionable business insights related to pricing, discounts, and inventory management.

The goal is to simulate real-world business problem-solving using data analytics techniques.

**🎯 Objectives**
- Analyze product pricing and discount strategies
- Identify inventory inefficiencies (stock-outs)
- Evaluate category-level performance
- Provide data-driven business recommendations

**🗂️ Dataset Description**
The dataset contains product-level information:

| Column Name              | Description                          |
|-------------------------|--------------------------------------|
| sku_id                  | Unique product ID                    |
| category                | Product category                     |
| name                    | Product name                         |
| mrp                     | Maximum Retail Price                 |
| discountPercent         | Discount (%)                         |
| discountedSellingPrice  | Final selling price                  |
| availableQuantity       | Available stock                      |
| weightInGms             | Product weight in grams              |
| outOfStock              | Stock availability status            |
| quantity                | Units per product                    |


**⚙️ Tools & Technologies**
SQL (PostgreSQL / pgAdmin)
Power BI (Dashboard & Visualization)
GitHub (Version Control)


**🧹 Data Cleaning & Preparation**
Removed invalid records where MRP = 0
Converted prices from paise to rupees
Checked for NULL values and inconsistencies
Identified duplicate product entries (multiple SKUs)


**🔍 SQL Analysis Performed**
1. Product Exploration
Total number of products
Unique categories
Stock availability distribution
2. Pricing & Discount Analysis
Top 10 products with highest discounts
High MRP but low discount products
3. Inventory Analysis
In-stock vs out-of-stock products
High-value products currently unavailable
4. Revenue Analysis
- Estimated revenue by category:
```Revenue = Selling Price × Available Quantity```
6. Value Analysis
Price per gram calculation to identify best-value products
7. Product Segmentation
Categorized products into:
- Low (<1kg)
- Medium (1–5kg)
- Bulk (>5kg)


**📊 Power BI Dashboard**
An interactive dashboard was created to visualize key insights and support decision-making.

🎯 Dashboard Features
- 📍Overview
Total Products
Total Categories
Total Estimated Revenue
Stock Availability (In-stock vs Out-of-stock)
- 💰 Pricing & Discounts
Top discounted products
Average discount by category
Premium products with low discounts
- 📦 Inventory Insights
Out-of-stock high-value products
Category-wise stock levels
Inventory distribution
- ⚖️ Value Analysis
Price per gram comparison
Identification of value-for-money products


**📌 Key KPIs**
- 💰 Total Revenue
- 📉 Stock-out Rate
- 🏷️ Average Discount
- 📦 Inventory Levels
- 🖼️ Dashboard Preview
![Overview](https://github.com/neharahate07/Zepto-Business-Data-Analysis-SQL-Power-Bi-/blob/main/IMG_20260410_120235.jpg.jpeg)

## 📈 SQL Analysis Sample

```sql
-- Average discount by category
SELECT category, AVG(discount) AS avg_discount
FROM products
GROUP BY category;

-- Identify out-of-stock products
SELECT product_name, category
FROM products
WHERE stock = 0;
```

## 📂 Project Files

| File Type | Description | Link |
|----------|------------|------|
| 📊 Dataset | Raw product data | [View](https://github.com/neharahate07/Zepto-Business-Data-Analysis-SQL-Power-Bi-/blob/main/zepto_data.xlsx) |
| 🗄️ SQL Script | Data cleaning & analysis queries | [View](https://github.com/neharahate07/Zepto-Business-Data-Analysis-SQL-Power-Bi-/blob/main/Zepto%20SQL%20Project.sql) |
| 📈 Power BI Dashboard | Interactive dashboard file | [Download](https://github.com/neharahate07/Zepto-Business-Data-Analysis-SQL-Power-Bi-/blob/main/Zepto%20Dashboard.pbix) |


**💼 Business Insights**
- ⚠️ Revenue Leakage Identified
High MRP products that are out of stock indicate missed sales opportunities
- 💡 Pricing Strategy Gap
Premium products with low discounts may reduce competitiveness
- 📊 High-Performing Categories
Certain categories contribute significantly to total revenue
- 🏷️ Discount Optimization
Some categories offer high discounts, impacting profit margins
- ⚖️ Customer Value Insight
Price-per-gram analysis highlights products offering better value


**🚀 Business Recommendations**
- Improve inventory management to reduce stock-outs
- Optimize discount strategies for premium products
- Focus marketing efforts on high-performing categories
- Use value-based pricing to attract cost-conscious customers


## 📂 Project Structure

```
zepto-sql-business-analysis/
│
├── zepto_project.sql
├── dataset.csv
├── dashboard.pbix
├── images/
│   ├── overview.png
│
└── README.md
```
## ▶️ How to Run the Project
## SQL:
- Open PostgreSQL / pgAdmin
- Create database
- Run SQL script
## Power BI:
- Open .pbix file
- Refresh dataset
- Explore dashboard


## 📈 Key Learnings
- Applied SQL for real-world business problem solving
- Built interactive dashboards in Power BI
- Translated raw data into actionable insights
- Strengthened analytical and decision-making skills


## 🔮 Future Scope
- Add time-series sales analysis
- Build predictive models using Python
- Deploy dashboard online (Power BI Service)


## 👩‍💻 Author
**Neha Rahate**  
MBA (Business Analytics) | Aspiring Data Analyst  



















