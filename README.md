# 🚕 Taxi Trip Data Analysis

This project analyzes taxi trip data to identify whether there is a significant difference in passenger behavior based on **payment method** (Card vs Cash). The analysis includes data cleaning, feature transformation, visualizations, and hypothesis testing using statistical methods.

---

## 📊 Objective

To determine if **passenger distribution differs significantly** based on the **payment method** (Card or Cash), and whether this difference is statistically significant.

---

## 🔧 Steps Performed

### 1. Data Cleaning & Preprocessing
- Removed null and duplicate entries
- Selected relevant columns for analysis
- Transformed and created new columns for better insights (e.g., `trip_duration`, `fare_amount`, `passenger_count`)

### 2. Feature Engineering
- Created new features like:
  - `trip_duration` (in minutes)
  - Day/Hour of trip
- Filtered outliers using boxplots and IQR method

### 3. Visualizations
- **Boxplots & Histplots**: Compared `fare_amount` across payment methods
- **Pie Chart**: Showed overall passenger preference for Card vs Cash
- **Stacked Bar Chart**: Showed percentage of passengers by count per payment method
- **QQ Plot**: Checked for normality to decide on statistical test

_You can view the visuals in the `/images` folder._

---

## 🧪 Hypothesis Testing

### ● Test Used:
**Independent Two-Sample T-Test** (after checking data with QQ plot)

### ● Hypothesis:
- **Null Hypothesis (H₀):** No difference in passenger distribution based on payment method
- **Alternative Hypothesis (H₁):** There is a difference

### ● Result:
- **p-value:** `0.00`
- **t-statistic:** `147.15`

📌 **Conclusion**: We **reject the null hypothesis**, meaning there is a **statistically significant difference** in passenger behavior based on the payment method.

---

## 🖼️ Visuals

Charts and visual analysis images are included in the [`/images`](https://github.com/Prince-Saxena/Taxi-Trip-Data-Analysis/images) folder:
- Boxplot by payment method
- Histogram of fare
- Pie chart of passenger preference
- Stacked horizontal bar chart
- QQ plot for normality check

---

## 🛠️ Tools & Libraries Used
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- SciPy (for statistical test)
- Statsmodels (for QQ plot)
- Jupyter Notebook

---

## 📁 Project Structure

