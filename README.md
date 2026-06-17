# 🚀📊 Analyzing E-Learning Platform Purchases using MySQL


![MySQL](https://img.shields.io/badge/MySQL-Database-blue?style=for-the-badge&logo=mysql)
![SQL](https://img.shields.io/badge/SQL-Data%20Analysis-orange?style=for-the-badge)
![Data Analytics](https://img.shields.io/badge/Data-Analytics-green?style=for-the-badge)
![GitHub](https://img.shields.io/badge/GitHub-Portfolio-black?style=for-the-badge&logo=github)
![Project Status](https://img.shields.io/badge/Project-Completed-brightgreen?style=for-the-badge)
![Module](https://img.shields.io/badge/Data%20Analytics-Module%203-purple?style=for-the-badge)

---

# 🎯 Project Overview

This project analyzes **E-Learning Platform Purchase Data** using **MySQL** to understand:

📈 Sales Trends  
👨‍🎓 Learner Behavior  
📚 Popular Course Categories  
💰 Revenue Performance  
📊 Business Insights

---

# 🗄️ <u><b>DATABASE SETUP & DATA ENTRY</b></u>

## 🏗️ <u><b>Create Database</b></u>

- Create the `Elearning_Platform` database.
- Set up the environment for SQL analysis.

<img width="2819" height="1438" alt="image" src="https://github.com/user-attachments/assets/4228f9a3-4b13-4e56-8f05-5fa2bf5de807" />

---

## 🏗️ <u><b>Create Tables</b></u>

### 👨‍🎓 learners
| Column Name | Description |
|-------------|-------------|
| learner_id | Primary Key |
| full_name | Learner Name |
| country | Country of Residence |

### 📚 courses
| Column Name | Description |
|-------------|-------------|
| course_id | Primary Key |
| course_name | Course Title |
| category | Course Category |
| unit_price | Price Per Course |

### 🛒 purchases
| Column Name | Description |
|-------------|-------------|
| purchase_id | Primary Key |
| learner_id | Foreign Key |
| course_id | Foreign Key |
| quantity | Number of Courses Purchased |
| purchase_date | Purchase Date |

<img width="2823" height="1444" alt="image" src="https://github.com/user-attachments/assets/1bd91ad3-cef1-4e95-8223-5a2ad92a28bb" />

---

## 📝 <u><b>Insert Sample Data</b></u>

✅ 5 Learners  
✅ 5 Courses  
✅ 8 Purchase Records

---

# 🔗 <u><b>DATA EXPLORATION USING JOINS</b></u>

## 🔹 <u><b>INNER JOIN</b></u>

📌 Combine learner, course, and purchase information.

---

## 🔹 <u><b>LEFT JOIN</b></u>

📌 Display all learners including those without purchases.

---

## 🔹 <u><b>RIGHT JOIN</b></u>

📌 Display all courses and purchase information.

---

# 📈 <u><b>CORE ANALYTICAL QUERIES</b></u>

## 🥇 <u><b>Q1. Display Each Learner's Total Spending with Their Country</b></u>

🎯 Objective:
Calculate the total amount spent by each learner and display their country.

<img width="2821" height="1444" alt="image" src="https://github.com/user-attachments/assets/b85be975-b80d-454a-8178-80824cee91e4" />

---

## 🥈 <u><b>Q2. Find the Top 3 Most Purchased Courses by Quantity</b></u>

🎯 Objective:
Identify the most popular courses based on purchase quantity.

<img width="2828" height="1445" alt="image" src="https://github.com/user-attachments/assets/810e77b2-1105-4b43-a69d-2230a865a8fc" />

---

## 🥉 <u><b>Q3. Show Each Category's Total Revenue and Number of Unique Learners</b></u>

🎯 Objective:
Analyze category performance using:

- 💰 Total Revenue
- 👥 Unique Learners

<img width="2835" height="1456" alt="image" src="https://github.com/user-attachments/assets/bcf5b77e-f0a6-4535-8b5a-e9b5f6709b8c" />

---

## 👨‍💻 <u><b>Q4. List Learners Who Purchased from More Than One Category</b></u>

🎯 Objective:
Identify learners who purchased courses from multiple categories.

---

## 🚫 <u><b>Q5. Identify Courses Never Purchased</b></u>

🎯 Objective:
Find courses with zero purchase records.

---

# 🔍 <u><b>SUBQUERIES & CORRELATED SUBQUERIES</b></u>

## 💰 <u><b>Q6. Find Learners Whose Total Spending is Above the Average Learner Spending</b></u>

🎯 Objective:
Compare learner spending with the overall average spending.

---

## 💎 <u><b>Q7. Display Courses Whose Price is Higher Than Any Course in the 'Beginner' Category</b></u>

🎯 Objective:
Identify premium courses based on pricing.

---

## 🌍 <u><b>Q8. Find Learners Who Spent More Than the Average Spending in Their Country</b></u>

🎯 Objective:
Analyze spending behavior within each country.

---

# ⚡ <u><b>CTE, CASE, VIEW & NULL HANDLING</b></u>

## 🏆 <u><b>Q9. Use a CTE to Calculate Total Spending Per Learner and Display Learners with Spending Above 10,000</b></u>

🎯 Objective:
Identify high-value learners using Common Table Expressions (CTE).

---

## 🎯 <u><b>Q10. CASE Expression – Classify Learners Based on Spending</b></u>

| Spending Range | Customer Category |
|----------------|-------------------|
| 💰 Above 15,000 | 🥇 High Value |
| 💵 8,000–15,000 | 🥈 Medium Value |
| 💸 Below 8,000 | 🥉 Low Value |

<img width="2827" height="1450" alt="image" src="https://github.com/user-attachments/assets/7ee188f1-d7d6-46db-8293-a5ab80a2a9df" />

---

## 🧹 <u><b>Q11. NULL Handling – Display All Courses and Replace NULL Purchase Counts with 0 Using IFNULL() or COALESCE()</b></u>

🎯 Objective:
Handle missing values and replace NULL values with zero.

---

## 👁️ <u><b>Q12. Create View – category_performance_view</b></u>

### 📊 View Displays:

- 📚 Category
- 💰 Total Revenue
- 🛒 Number of Purchases
- 📈 Average Revenue Per Purchase

<img width="2828" height="1442" alt="image" src="https://github.com/user-attachments/assets/991b5742-4cb7-4ac2-8192-51920d6c46f0" />

---

# 📊 <u><b>KEY INSIGHTS</b></u>

✅ Top-performing categories generate maximum revenue.

✅ Multi-category learners contribute higher spending.

✅ Certain courses require additional marketing strategies.

✅ High-value learners significantly impact business growth.

---

# 💡 <u><b>RECOMMENDATIONS</b></u>

🚀 Focus marketing on top-performing categories.

🎯 Introduce personalized recommendations.

📦 Create bundle offers for cross-category learners.

📢 Promote low-performing courses.

🏆 Retain high-value learners through loyalty programs.

---

# 🛠️ <u><b>SKILLS DEMONSTRATED</b></u>

💻 MySQL  
🗄️ Database Design  
🔗 SQL Joins  
📊 Aggregate Functions  
🔍 Subqueries  
⚡ CTE (Common Table Expressions)  
🎯 CASE Statements  
👁️ Views  
🧹 NULL Handling  
📈 Data Analysis  
📊 Business Intelligence

---

# ⭐ Project Outcome

This project demonstrates how **MySQL and SQL analytics techniques** can be used to transform raw purchase data into meaningful business insights and support data-driven decision-making.

---

# 🏷️ Hashtags

mysql, sql, data-analytics, data-analysis, database-design, sql-project, mysql-project, business-intelligence, data-modeling, analytics,
subqueries, cte, joins, views, relational-database, portfolio-project
