# Walmart-Project
Predicting the weekly sales of each store for 12 weeks

**1. Problem Statement: Walmart Sales Forecasting and Analysis**

Walmart operates a vast network of retail stores across various locations, and its sales performance is influenced by multiple factors, including seasonality, economic indicators, and promotional events. Analyzing and predicting sales trends is crucial for optimizing inventory management, staffing, and marketing strategies.

**2. The objective** of this project is to analyze historical sales data from Walmart stores to:

**Identify Key Sales Drivers** – Understand the impact of factors like holidays, promotions, consumer price index (CPI), unemployment rate, fuel prices, and temperature on weekly sales.

**Detect Seasonality and Trends** – Explore patterns in sales data to determine high and low sales periods.

**Performance based on Temperature** - Does temperature affect the weekly sales in any manner

**Evaluate Store Performance** – Identify the best and worst-performing stores based on historical data and analyze the reasons behind performance variations.

**Predict Future Sales**  – Develop predictive models using machine learning techniques to forecast sales for the upcoming weeks and assist in decision-making.

**3. Data Description**

**I. Dataset Overview:**
* Total Rows: 6,435
* Total Columns: 8

**II. Column Details:**
* **Store** (int64): Store ID (1 to 45)
* **Date** (object): Weekly timestamp (Format: DD-MM-YYYY)
* **Weekly_Sales** (float64): Total sales for the store in that week
* **Holiday_Flag** (int64): Indicates if the week had a holiday (1 = Holiday, 0 = Non-Holiday)
* **Temperature** (float64): Average temperature for that week
* **Fuel_Price** (float64): Fuel price for that week
* **CPI** (float64): Consumer Price Index
* **Unemployment** (float64): Unemployment rate for that period

**4. Data Pre-processing Steps and Inspiration**
1. Load the Data
2. Cheking the information of the data such as datatype of the column, number of columns and rows
3. Handling missing values
4. Handling duplicated values
5. Checking the unique values
6. Plotting the outliers with the help of boxplot
7. Converting the datatype of Date column from object to Datetime

**5. Choosing the Algorithm for the Project**

**Facebook prpohet**
Facebook Prophet is an open-source time series forecasting algorithm developed by Facebook’s Core Data Science team. It is designed for business forecasts, such as sales, demand, or revenue predictions, where seasonality, holidays, and trends play a crucial role.

I have chosen the Facebook prophet for this project for following reason
* Handles Missing Data & Outliers Well
* Automatic Trend & Seasonality Detection
* Considers Holidays & Special Events
* Works Well with Daily, Weekly, and Monthly Data
* Supports Multiplicative & Additive Seasonality

**6 Assumptions**
1. Data Quality Assumptions
* No Missing Data – We assume that all key variables (sales, dates, prices, unemployment rates) are available and accurate.
* Correct Data Types – The dataset should have the correct formats (e.g., dates in datetime format).
* No Duplicates – Each record corresponds to a unique store-week combination.

2. Sales Trend & Seasonality Assumptions
* Sales follow a seasonal trend – Sales might peak during holidays and drop during off-seasons.
* Holidays impact sales – The Holiday_Flag indicates sales surges during events like Thanksgiving, Christmas, etc.
* External factors (temperature, fuel price, CPI, unemployment) influence sales – We assume these variables affect sales.

3. Forecasting Model Assumptions
* Historical patterns repeat – Models like Prophet and ARIMA assume that past trends will continue in the future.
* No abrupt market changes – We assume that no sudden economic crashes or unexpected external factors drastically change sales patterns.
* Independence of stores – We assume sales in one store don’t directly affect sales in another store.

**7. Model Evaluation for Facebook Prophet**
Once we build a forecasting model using Prophet, we need to evaluate its performance using
1. error metrics and
2. validation techniques.

**8.Inferences from the Project**
1. Sales Trends and Patterns
* Long-Term Sales Growth – The overall sales trend shows an upward trajectory, indicating business growth over time.
* Seasonality Exists – Sales peak at specific times of the year, especially during holidays and festive seasons.
* Weekly Sales Fluctuations – Certain weeks have consistent dips and spikes, likely due to shopping habits.

2. Impact of External Factors on Sales
* Holidays Significantly Affect Sales – Higher sales are observed during events like Thanksgiving, Christmas, and Super Bowl weekends.
* Fuel Price Fluctuations Have a Moderate Effect – Changes in fuel prices impact consumer spending, but the effect varies across stores.
* Unemployment Rate Shows a Negative Correlation – Higher unemployment rates lead to slightly lower sales.
* Temperature Has a Seasonal Effect – Certain temperature ranges correlate with higher sales (e.g., cold months show increased shopping).

3. Model Performance Evaluation
* Prophet Provides a Strong Forecast – The model effectively captures trends and seasonality.
* Error Rates (MAPE, RMSE) Are Acceptable – If MAPE < 10%, the forecast is highly accurate.
* Future Predictions Align with Business Trends – Sales predictions for the next 12 weeks follow expected seasonal trends.

**9. Future Possibilities**
* Unexpected Market Changes Impact Accuracy – External events like economic downturns or supply chain issues are not accounted for.
* Store-Level Predictions Could Be Improved – A separate Prophet model per store may yield better accuracy.

Business Recommendations
* Optimize Inventory Based on Seasonal Trends – Increase stock levels before major holidays.
* Leverage Holiday Sales Spikes – Walmart should run targeted marketing campaigns before peak shopping seasons.
* Monitor Economic Indicators – Adjust pricing or promotions based on unemployment rates and fuel prices.
* Enhance Store-Level Forecasting – Use individual store data for more granular sales predictions.

**10. Conclusion**

* prophet successfully forecasts Walmart's weekly sales with reasonable accuracy.
* Sales follow clear seasonal trends influenced by holidays, fuel prices, and economic conditions.
* Future improvements include hyperparameter tuning, store-specific models, and external factor analysis.



