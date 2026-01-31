# Innomatics-hackaton-
# 🍔 Food Delivery Data Analysis – Hackathon Project

## 📌 Project Overview
This project focuses on combining and analyzing food delivery data from multiple real-world data sources.  
The goal is to create a **single source of truth dataset** and perform analytical queries to answer business-oriented questions such as order trends, user behavior, restaurant performance, and revenue insights.

This repository was created as part of a **Hackathon / Data Analytics Challenge**.

---

## 📂 Datasets Used
The project uses three different data formats to simulate real-world systems:

### 1️⃣ orders.csv (Transactional Data)
- Contains order-level information
- Each row represents a single food order
- Key columns:
  - `order_id`
  - `user_id`
  - `restaurant_id`
  - `order_amount`
  - `order_date`

### 2️⃣ users.json (User Master Data)
- Contains user details
- Key columns:
  - `user_id`
  - `user_name`
  - `city`
  - `membership` (Gold / Regular)

### 3️⃣ restaurants.sql (Restaurant Master Data)
- SQL script containing restaurant information
- Key columns:
  - `restaurant_id`
  - `restaurant_name`
  - `city`
  - `cuisine`

---

## 🔗 Data Integration Process
The datasets were merged using the following logic:

- **Join Type:** Left Join  
- **Join Keys:**
  - `orders.user_id → users.user_id`
  - `orders.restaurant_id → restaurants.restaurant_id`

This ensures **all orders are retained**, even if some user or restaurant details are missing.

---

## 📁 Final Output
### ✅ `final_food_delivery_dataset.csv`

The final merged dataset contains:
- Order details
- User information
- Restaurant information

This dataset acts as the **only source of truth** for all analysis and MCQs in the hackathon.

---

## 📊 Analysis Performed
Using the final dataset, the following analyses were carried out:

- 📈 Order trends over time  
- 👥 User behavior patterns  
- 🏙️ City-wise performance  
- 🍽️ Cuisine-wise restaurant performance  
- ⭐ Membership impact (Gold vs Regular users)  
- 💰 Revenue distribution and seasonality  
- 🧮 Average Order Value (AOV) analysis  

---

## 🧠 Sample Analytical Question
**Which restaurant has the highest average order value but less than 20 total orders?**

✔️ **Answer:** `Ruchi Foods Chinese`

This was determined by:
- Calculating total orders per restaurant
- Filtering restaurants with `< 20` orders
- Comparing average order values (AOV)

---

## 🛠️ Tools & Technologies
- Python
- Pandas
- SQLite
- Jupyter Notebook

---

## 📓 Notebook
- `Tharun_Nandula_Hackathon.ipynb`  
Contains:
- Data loading
- Data cleaning
- Data merging
- Exploratory analysis
- Business question solutions

---

## 🚀 How to Run
1. Clone the repository
2. Open the notebook in Jupyter / Google Colab
3. Ensure all data files are in the same directory
4. Run cells sequentially

---

## 📌 Key Learning Outcomes
- Handling multiple data formats (CSV, JSON, SQL)
- Real-world data joins and schema understanding
- Analytical thinking for business problems
- Avoiding common pitfalls in hackathon MCQs

---

## 📬 Author
**Lokesh (Loki)**  
B.Tech CSE (AI & ML) | Data Science Enthusiast  

---

⭐ If you found this project useful, feel free to star the repository!
