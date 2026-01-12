# Restaurant Order Data Analysis (MySQL)

## Project Overview
This project analyzes restaurant order data stored in a MySQL database to understand customer behavior and menu performance. Using SQL queries, the analysis explores menu items, order activity, and purchasing patterns to identify top-performing dishes, underperforming items, and high-value customers.

**Scenario:**  
You have been hired as a Data Analyst for *Taste of the World Cafe*, a restaurant with diverse menu offerings. After launching a new menu at the start of the year, management requested insights into how customers are responding.

---

## Objectives
1. Explore the restaurant menu to understand pricing, categories, and item distribution  
2. Analyze order activity to understand order volume, order size, and customer behavior  
3. Combine menu and order data to evaluate menu performance and spending patterns  

---

## Database Setup
A MySQL database named **restaurant_db** was created and populated with the provided data. The data was validated to ensure all tables loaded correctly before analysis.

Tables used:
- menu_items  
- order_details  

---

## Objective 1: Explore the Menu

### Key Questions
- How many items are on the menu?
- What are the least and most expensive items?
- How many Italian dishes are on the menu?
- What are the least and most expensive Italian dishes?
- How many dishes are in each category?
- What is the average dish price within each category?

### Key Findings
- The menu contains **32 total items**
- Italian dishes account for **9 menu items**
- Pricing varies significantly across menu categories
- Category-level analysis revealed differences in pricing and menu depth

### Techniques Used
- COUNT(*)
- ORDER BY
- WHERE
- GROUP BY
- Aggregation functions (AVG, COUNT)

---

## Objective 2: Explore Orders

### Key Questions
- What is the date range of the order data?
- How many unique orders were placed during this period?
- How many total items were ordered?
- Which orders contained the most items?
- How many orders included more than 12 items?

### Key Findings
- Orders range from **January 1, 2023 to March 31, 2023**
- **5,370 unique orders** were placed
- **12,234 total items** were ordered
- Several orders contained unusually large numbers of items, suggesting group or bulk purchases

### Techniques Used
- MIN() and MAX()
- COUNT(DISTINCT)
- Subqueries
- HAVING with aggregated results

---

## Objective 3: Menu Performance & Customer Behavior

### Table Join
The order_details and menu_items tables were combined using a **LEFT JOIN** on:
- order_details.item_id
- menu_items.menu_item_id

This preserved all order records while adding menu item details for analysis.

---

### Least & Most Ordered Items
- **Most ordered item:** Hamburger  
- **Least ordered item:** Chicken Tacos  

This indicates opportunities to promote or revise underperforming menu items while maintaining popular offerings.

---

### Top-Spending Orders
- Identified the **top 5 highest-spending orders**
- High-value orders consistently included **Italian menu items**

---

### Insights from High-Spend Orders
- The highest-spending order was dominated by Italian dishes
- Although Italian items were not the most frequently ordered overall, they contributed heavily to high-revenue orders
- Italian dishes appear to be premium, high-value items and should remain on the menu

---

## Business Insights & Recommendations
- Italian dishes drive high-revenue transactions despite lower overall order frequency
- Popular items such as hamburgers generate consistent demand
- Low-performing items like chicken tacos may require pricing, recipe, or marketing adjustments
- Menu strategy should balance customer popularity with revenue contribution

---

## Skills Demonstrated
- SQL querying (MySQL)
- Relational database analysis
- JOIN operations
- Aggregations and subqueries
- Data-driven business insights
- Analytical problem solving

---

## Author
Steven Williams  
Master’s in Business Analytics  
Focus: SQL, Python, and Data Analytics
