# 📊 Superstore Sales & Profitability Analysis — Case Study

This project presents a detailed exploratory data analysis (EDA) of a **Superstore Sales Dataset**, uncovering valuable business insights related to **sales**, **profit**, **shipping behavior**, and **customer performance**.

## 🔍 Objective

To explore and analyze Superstore data to:
- Understand sales & profitability patterns
- Detect operational inefficiencies
- Identify key customer & regional trends
- Provide actionable insights to optimize decision-making

---

## 📁 Dataset Overview

- **Columns**: Order ID, Order Date, Ship Date, Category, Sub-Category, State, Region, Customer ID, Sales Price, Quantity, Discount, Profit, Ship Mode, etc.
- **Scope**: U.S.-based retail transactions

---

## 📌 Key Tasks Performed

### 🧹 Data Cleaning & Preprocessing
- Removed duplicate records and documented affected rows/order IDs
- Handled inconsistent date formats (`dd-mm-yyyy` to datetime)
- Validated Order Date year against Order ID
- Imputed missing values in:
  - **Quantity** using **median** (due to skewness)
  - **Ship Mode** using **business rules based on Days to Ship**
- Standardized **State** names by replacing abbreviations (e.g., TX → Texas)

---

### 🧮 Feature Engineering
- **Days to Ship**: Calculated as the difference between Order and Ship Date
- **Shipping Urgency**: Categorical variable based on Days to Ship
- **Original Price & Total Discount**: Derived from Sales Price and Discount
- **Days Since Last Order**: For customer behavior analysis
- Aggregated **Total Sales**, **Quantity**, and **Discount per Customer**
- Created **Customer Sales & Profit Quintiles**

---

### 📈 Data Visualization & Insights
#### 📦 Sales & Profit Analysis
- **Scatter & Regression Plot**: Analyzed correlation between Sales and Profit
- **Boxplot & Violin Plot**: Detected outliers and visualized profit distribution
- **Heatmap**: Cross-tabbed Customer Sales vs. Profit Quintiles
- **Joint Plot**: Distribution of sales and profit to identify high-value customers

#### 🚚 Shipping & Profitability
- **Shipping Urgency Distribution**: Pie chart
- **Shipping Mode vs. Profit**: Grouped bar chart and region-wise pivot table
- **Days to Ship vs. Profit**: Violin plots to identify optimal delivery windows

#### 🛒 Discount Impact
- **Scatter Plot with Regression Line**: Showed how increasing discounts often reduce profit

#### 🌍 Geographical Insights
- **State-wise Profitability**: Pivot table to rank top/bottom states by profit
- **Correlation Matrix (State vs. Profit)**: Weak correlation observed

---

## 📌 Tools & Libraries Used

- **Python**
- `pandas`, `numpy` — data handling
- `matplotlib`, `seaborn` — data visualization
- `sklearn.preprocessing.LabelEncoder` — for encoding categorical data

---

## 📊 Key Insights

- High discounts generally reduce profitability — discount strategy needs optimization.
- Faster shipping (0–1 days) doesn’t guarantee higher profit — cost-benefit analysis needed.
- Top sales don't always mean top profits — certain customer groups yield high sales with low margins.
- Certain states consistently underperform in profitability — localized strategies recommended.
- Shipping Mode choice significantly impacts both **customer experience** and **profit**.

---

## 🏁 Outcome

- Delivered a comprehensive analysis suitable for **business decision-making**.
- Highlighted key areas of improvement in **logistics**, **pricing**, and **customer segmentation**.


