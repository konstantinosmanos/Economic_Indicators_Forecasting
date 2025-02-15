# 📊 Economic Indicators Analysis & Forecasting 🇬🇷  

🚀 **Analyzing and forecasting Greece's GDP Growth, Inflation Rate, and Unemployment Rate using Python and VAR models.**  

---

## 🔍 **Project Overview**
This project explores **historical economic data** from Greece and applies **statistical analysis & time series forecasting** to understand and predict future economic trends.  

Key tasks performed:  
✅ **Data Collection & Cleaning** from the World Bank.  
✅ **Exploratory Data Analysis (EDA)** to visualize economic trends.  
✅ **Correlation & Regression Analysis** to identify key relationships.  
✅ **Time Series Forecasting (VAR Model)** to predict trends for the next 5 years.  
✅ **Data Visualization** of historical trends and future forecasts.  

📌 **[Check the full analysis in the Jupyter Notebook](./forecasting_analysis.ipynb)**  

---

## 📂 **Project Structure**

---

## 📊 **Data Collection & Preprocessing**
- **Source**: World Bank  
- **Timeframe**: 1991 - 2023 (33 years of annual data)  
- **Economic Indicators Used**:
  - **GDP Growth (annual %)**
  - **Inflation Rate (%)**
  - **Unemployment Rate (% of total labor force)**  

**Data Cleaning Steps:**  
✅ Checked for missing values & ensured correct data types.  
✅ Renamed columns for clarity.  
✅ Visualized historical trends in economic indicators.  

---

## 📈 **Correlation Analysis**
We calculated **Pearson correlation coefficients** and visualized them using a heatmap to understand relationships between indicators.

### **Key Findings**:
- **GDP Growth vs. Unemployment Rate** → **-0.39 (Negative Correlation)**  
  - Confirms **Okun’s Law**: As GDP grows, unemployment tends to decrease.  
- **Inflation vs. Unemployment Rate** → **-0.60 (Negative Correlation)**  
  - Supports **Phillips Curve**: Higher inflation is associated with lower unemployment.  
- **GDP Growth vs. Inflation** → **0.16 (Weak Positive Correlation)**  
  - Inflation slightly increases as GDP grows, but the relationship is weak.  

📊 **[See the correlation heatmap here](./charts/Correlation_Matrix_growth_inflation_unemployment.png)**  

---

## 🔍 **Regression Analysis: How Inflation & Unemployment Affect GDP Growth**
We used **Ordinary Least Squares (OLS) regression** to test if **Inflation Rate** and **Unemployment Rate** significantly impact **GDP Growth**.

### **Results:**
| Variable                 | Coefficient | p-value  | Significance? |
|--------------------------|------------|---------|--------------|
| **Inflation Rate**       | -0.0976    | 0.599   | ❌ No significant effect |
| **Unemployment Rate**    | -0.3382    | 0.037   | ✅ Significant negative effect |

- **Unemployment Rate negatively impacts GDP Growth**, supporting Okun’s Law.
- **Inflation Rate does not significantly impact GDP Growth** in Greece.

📊 **[See the regression output in the Jupyter Notebook](./forecasting_analysis.ipynb)**  

---

## 🔮 **Time Series Forecasting (VAR Model)**
To predict **future trends (2024 - 2028)**, we used a **Vector Autoregression (VAR) model**.  
Before forecasting, we checked for **stationarity** using the **Augmented Dickey-Fuller (ADF) Test**:

| Variable               | Test Statistic | P-Value  | Conclusion |
|------------------------|---------------|---------|------------|
| **GDP Growth**        | -3.31          | 0.0146  | **Stationary** ✅ |
| **Inflation Rate**    | -3.54          | 0.0069  | **Stationary** ✅ |
| **Unemployment Rate** | -1.88          | 0.3422  | ❌ Non-Stationary |

📌 **Since Unemployment Rate was non-stationary, we applied differencing to make it stationary.**

---

## 📈 **Forecast Results (2024-2028)**
| Year | GDP Growth (%) | Inflation Rate (%) | Unemployment Rate (%) |
|------|--------------|------------------|----------------------|
| 2024 | 4.01        | 4.29             | 11.05                |
| 2025 | 2.42        | 4.04             | 11.05                |
| 2026 | 2.32        | 3.26             | 11.31                |
| 2027 | 1.97        | 3.37             | 11.34                |
| 2028 | 1.73        | 3.02             | 11.40                |

📊 **Visualizations of the Forecast**:
### **📊 GDP Growth Forecast**
![GDP Growth Forecast](./charts/Forecast_growth_Greece_5years.png)

### **📊 Inflation Rate Forecast**
![Inflation Rate Forecast](./charts/Forecast_inflation_Greece_5years.png)

### **📊 Unemployment Rate Forecast**
![Unemployment Rate Forecast](./charts/Forecast_unemployment_Greece_5years.png)

---

## 📌 **Limitations & Future Improvements**
While this model successfully analyzes and forecasts **Greece’s GDP Growth, Inflation, and Unemployment**, **macroeconomic theory suggests additional factors** that could improve accuracy:  

- **GDP Equation (Y = C + I + G + NE)**  
  - **Consumption (C)** → Affected by taxation & household spending.  
  - **Investment (I)** → Influenced by interest rates.  
  - **Government Spending (G)** → Often assumed constant but varies in fiscal policies.  
  - **Net Exports (NE)** → Trade balance impacts GDP growth.  

🔹 **Enhancing the Model:**  
Including these additional **macroeconomic indicators** (e.g., taxation, interest rates, government spending, trade balance) would likely **increase R²** and provide a **more comprehensive explanation of GDP Growth variance**.  

📌 However, the **goal of this project** was not to build a perfect predictive model but to **demonstrate skills in econometrics, data analysis, and forecasting using Python**. The results confirm that **Phillips Curve** and **Okun’s Law** hold in Greece’s economic context, showcasing the practical applications of economic theory in data analysis.  

---

## 🛠 **Technologies Used**
- **Python**: Pandas, Statsmodels, Matplotlib, Seaborn
- **Time Series Analysis**: VAR Model, ADF Test
- **Data Visualization**: Matplotlib & Seaborn

---

## 📬 **Contact & Connect**
📩 [Email Me](mailto:manoskonstantinos960@gmail.com)  
🔗 [LinkedIn](https://www.linkedin.com/in/konstantinosmanos)  
🖥 [GitHub](https://github.com/konstantinosmanos)  

🚀 **Like this project? Give it a ⭐ on GitHub!**
