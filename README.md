# Superstore-Sales-Analysis-SQL-
Built a SQL mini project using the Superstore dataset to analyze regional sales, top-performing products, and monthly revenue trends. Delivered actionable insights through advanced queries (GROUP BY, ORDER BY, LIMIT) and demonstrated strong data analysis skills.
## Dataset
- Source: [Superstore Dataset on Kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final/data)
- Contains fields like: Order Date, Region, Product Name, Category, Sales, Profit, Quantity, Discount.
## SQL Queries & Insights

### Regional Sales Performance
```sql
SELECT Region, SUM(Sales) AS TotalSales
FROM sample_project.`sample - superstore`
GROUP BY Region
ORDER BY TotalSales DESC
``` 
 Top 5 Products by Sales
 ```sql
SELECT `Product Name`, SUM(Sales) AS TotalSales
FROM sample_project.`sample - superstore`
GROUP BY `Product Name`
ORDER BY TotalSales DESC
LIMIT 5;
``` 
Monthly Sales Trend
```sql
SELECT DATE_FORMAT(`Order Date`, '%Y-%m') AS Month, SUM(Sales) AS TotalSales
FROM sample_project.`sample - superstore`
GROUP BY Month
ORDER BY Month;
```
### 5. **Key Learnings**
```markdown
## Key Learnings
- Used GROUP BY, ORDER BY, LIMIT for aggregation and ranking.
- Applied date functions for time-series analysis.
- Translated raw transactional data into actionable business insights.
```
### Regional Sales Performance
![Regional Sales](images/regional_sales.jpeg)

### Top 5 Products by Sales
![Top Products](images/top_products.jpeg)

### Monthly Sales Trend
![Monthly Trend](images/monthly_trends.jpeg)

## Next Steps
- Extend analysis with Python (Pandas + Matplotlib) for visualizations.
- Build a Power BI dashboard using the same dataset.
- Integrate SQL + Python for end-to-end workflows.

