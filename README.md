# 🚕 Taxi Trip Data Analysis

This project analyzes taxi trip data to identify whether there is a significant difference in passenger and fare amount based on **payment method** (Card vs Cash). The analysis includes data cleaning, feature transformation, visualizations, and hypothesis testing using statistical methods.

---

## 📊 Objective

To determine if **Fare Amount distribution differs significantly** based on the **payment method** (Card or Cash), and whether this difference is statistically significant.

---

## 🔧 Steps Performed

---

### 1️⃣ Data Cleaning & Preprocessing

- Removed null and duplicate entries from the dataset.
- Selected key columns: `fare_amount`, `trip_distance`, `payment_type`, and `passenger_count`.
- Created and transformed new features:
  - `trip_duration` (in minutes)
  - Extracted `minutes` from datetime columns

---

### 2️⃣ Outlier Detection & Removal

- Identified outliers in `fare_amount`, `trip_distance` and `trip_duration` using a boxplot  
  ![Boxplot](https://raw.githubusercontent.com/Prince-Saxena/Taxi-Trip-Data-Analysis/main/images/boxplot.png)
- Removed outliers using the **IQR (Interquartile Range)** method to ensure accurate visualizations and testing

---

### 3️⃣ Exploratory Visualizations

#### 📊 Fare Amount Distribution by Payment Type  
Stacked histogram showing how fare values vary between Card and Cash users  
![Fare Histogram](https://raw.githubusercontent.com/Prince-Saxena/Taxi-Trip-Data-Analysis/main/images/histplotFare.png)

#### 📏 Trip Distance Distribution by Payment Type  
Stacked histogram displaying distance trends based on payment method  
![Distance Histogram](https://raw.githubusercontent.com/Prince-Saxena/Taxi-Trip-Data-Analysis/main/images/histplotDist.png)

#### 🥧 Payment Method Preference (Pie Chart)  
Shows overall passenger preference between Card and Cash  
![Pie Chart](https://raw.githubusercontent.com/Prince-Saxena/Taxi-Trip-Data-Analysis/main/images/pie.png)

#### 📶 Passenger Count by Payment Type (Stacked Bar Chart)  
Illustrates payment preference by passenger count group  
![Stacked Bar Chart](https://raw.githubusercontent.com/Prince-Saxena/Taxi-Trip-Data-Analysis/main/images/barh.png)

---

### 4️⃣ Data Distribution Check

- Used a **QQ Plot** to test if `fare_amount` follows a normal distribution  
- The plot showed a smooth but **non-standardized** pattern, indicating data is not normally distributed  
![QQ Plot](https://raw.githubusercontent.com/Prince-Saxena/Taxi-Trip-Data-Analysis/main/images/qqplot.png)

---
---

### 5️⃣ Hypothesis Testing

#### 🧪 Test Used
- **Independent Two-Sample T-Test**  
  (applied after checking data distribution with QQ plot)

#### 📌 Hypotheses

- **Null Hypothesis (H₀):**  
  There is no significant difference in passenger distribution based on payment method.

- **Alternative Hypothesis (H₁):**  
  There is a significant difference in passenger distribution based on payment method.

#### 📊 Test Results

- **p-value:** `0.00`  
- **t-statistic:** `147.15`

✅ **Conclusion:**  
The p-value is significantly less than 0.05, so we **reject the null hypothesis**.  
This confirms a **statistically significant difference** in passenger behavior based on the **payment method** (Card vs Cash).

---

## 🛠️ Tools & Libraries Used

- 🐍 Python (Jupyter Notebook)
- 📦 `pandas`, `numpy` – for data handling
- 📉 `matplotlib`, `seaborn` – for visualizations
- 🧪 `scipy.stats` – for t-test
- 📈 `statsmodels.api` – for QQ plot and distribution check

---
