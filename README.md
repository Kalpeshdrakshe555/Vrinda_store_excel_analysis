Project Documentation: Vrinda Store Annual Report 2022
Project Name: Vrinda Store Data Analysis

Tool Used: Microsoft Excel / Power BI

Objective: To analyze the annual sales data of Vrinda Store for the year 2022, identify key customer demographics, and understand sales trends to drive business growth.
1. Data Gathering & Preprocessing
Step 1.1: Load Raw Data

Source: Vrinda Store Raw data.xlsx

Initial Check: The dataset contains order-level details including Order ID, Cust ID, Gender, Age, Date, Status, Channel, SKU, Category, Size, Qty, Amount, and Shipping details.

Step 1.2: Data Cleaning

Handling Null Values: Checked the dataset for missing values. (Action: Removed rows with null values to ensure data integrity).

Standardizing Categorical Data:

Gender Column: Observed inconsistent entries (e.g., 'M', 'W', 'Men', 'Women').

Action: Used "Find & Replace" to standardize all values to 'Men' and 'Women'.

Note: Care was taken to ensure the replacement was specific to the 'Gender' column to avoid corrupting other text fields (e.g., preventing 'Amazon' from becoming 'AMenazon').

Data Type Validation: Ensured 'Qty' and 'Amount' columns are numeric for calculation.

2. Feature Engineering
To enable deeper analysis, new columns were created using the following formulas:

Step 2.1: Age Group Segmentation

Objective: To categorize customers into age brackets.

New Column: Age Group

Formula Used:

Excel

=IF([@Age]>=50, "Senior", IF([@Age]>=30, "Adult", IF([@Age]>=18, "Teenagers", "Children")))
Logic:

50+ years: Senior

30-49 years: Adult

18-29 years: Teenager

<18 years: Children

Step 2.2: Time Series Extraction

Objective: To analyze monthly sales trends.

New Column: Month

Formula Used:

Excel

=TEXT([@Date], "mmm")
Result: Converts dates (e.g., 2022-12-04) to month names (e.g., Dec).

3. Data Analysis & Visualization (Building the Dashboard)
Pivot Tables were created to summarize the data, followed by chart generation.

3.1 Key Performance Indicators (KPIs)

Total Sales: ₹21,176,377 (Sum of Amount)

Total Orders: 31,047 (Count of Order ID)

Total Quantity Sold: 31,237 (Sum of Qty)

3.2 Charts & Insights

Orders vs. Sales (Monthly Trend)

Chart Type: Combo Chart (Bar for Orders, Line for Sales).

Insight: Highest sales observed in March, followed by February and January.

Source Data: count_of orders and their sum m.csv

Sales by Gender

Chart Type: Pie/Donut Chart.

Insight: Women account for ~64% of total sales, making them the primary customer base.

Source Data: Sales Men vs Women.csv

Order Status Distribution

Chart Type: Bar Chart / Pie Chart.

Insight: ~92% of orders are Delivered. Return/Cancellation rates are minimal.

Source Data: delivery status.csv

Top 5 Performing States

Chart Type: Horizontal Bar Chart.

Insight: Maharashtra, Karnataka, and Uttar Pradesh are the top 3 contributing states.

Source Data: Sheet1.csv

Sales by Age Group & Gender

Chart Type: Grouped Bar Chart.

Insight: The Adult age group (30-49) contributes the most to sales, significantly higher than Seniors or Teenagers.

Source Data: sales by age group.csv

Order Contribution by Channel

Chart Type: Pie Chart.

Insight: Amazon, Myntra, and Flipkart are the dominant sales channels, capturing over 80% of orders.

Source Data: count of orders by chennels.csv

4. Interactivity
To make the dashboard interactive, Slicers were added for dynamic filtering:

Month Slicer: To view performance for specific months.

Channel Slicer: To filter data by sales platform (Amazon, Ajio, etc.).

Category Slicer: To analyze specific product categories (Kurta, Set, Western Dress).

5. Conclusion
Vrinda Store shows strong performance in early 2022 (Q1). The primary target audience is Adult Women residing in Maharashtra and Karnataka.
Marketing efforts should focus on maximizing visibility on Amazon and Myntra, while maintaining inventory for the "Adult" demographic.
