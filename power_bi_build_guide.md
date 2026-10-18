# Power BI recreation guide

1. Open Power BI Desktop → Get data → Text/CSV → select `sales_data.xlsx`.
2. Confirm data types: Order Date = Date; Quantity = Whole number; Unit Price and Sales = Decimal number.
3. Create measures:
   ```DAX
   Total Sales = SUM(sales_data[Sales])
   Total Orders = DISTINCTCOUNT(sales_data[Order ID])
   Units Sold = SUM(sales_data[Quantity])
   Average Order Value = DIVIDE([Total Sales], [Total Orders])
   ```
4. Add Card visuals for Total Sales, Total Orders, Units Sold, Average Order Value.
5. Add a clustered bar/column chart for Sales by Region and Sales by Category.
6. Add a line chart with Order Date on the X-axis and Total Sales as values; use a month/date hierarchy.
7. Add slicers for Region, Category, and Salesperson.
8. Format titles, currency/number display, and page layout. Test slicers before saving.
9. Take a screenshot for your repository README. Do not claim Power BI features you have not built and tested.
