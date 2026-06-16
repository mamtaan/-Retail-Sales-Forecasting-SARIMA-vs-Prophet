# 📈 Retail Sales Forecasting using SARIMA & Prophet
Forecasting Future Retail Demand using Time Series Analysis

Developed an end-to-end sales forecasting pipeline using SARIMA and Facebook Prophet to identify trends, seasonality, holiday effects, and generate a 90-day sales forecast for business decision-making.

# 📑 Table of Contents
- <a href ="#overview">Overview</a>
- <a href ="#business-problem">Business Problem</a>
- <a href="#dataset">Dataset</a>
- <a href="#project-structure">Project Structure</a>
- <a href ="#tools-technologies">Tools & Technologies</a>
- <a href="#time-series-analysis">Time Series Analysis</a>
- <a href="#stationarity-testing">Stationarity Testing</a>
- <a href="#sarima-modeling">SARIMA Modeling</a>
- <a href="#prophet-modeling">Prophet Modeling</a>
- <a href="#model-comparison">Model Comparison</a>
- <a href="#90-day-forecast">90-Day Forecast</a>
- <a href="#business-impact">Business Impact</a>
- <a href="#author--contact">Author & Contact</a>



<h2><a class="anchor" id="overview"></a>Overview</h2>

Retail businesses rely heavily on accurate sales forecasting for inventory planning, workforce allocation, procurement, and revenue management.

This project analyzes historical retail sales data and builds forecasting models using both classical statistical techniques (SARIMA) and modern forecasting frameworks (Prophet).

The goal is to identify the most effective forecasting approach and generate a reliable 90-day future forecast.


<h2><a class="anchor" id="business-problem"></a>Business Problem</h2>

Poor demand forecasting can lead to:

Stock shortages
Overstocking
Revenue loss
Increased storage costs
Inefficient supply chain operations

This project aims to:

✅ Forecast future sales demand

✅ Capture seasonal purchasing patterns

✅ Evaluate forecasting accuracy

✅ Support inventory and supply chain planning

<h2><a class="anchor" id="dataset"></a>Dataset</h2>

Dataset

| Feature     | Description                |
| ----------- | -------------------------- |
| date        | Sales date                 |
| store_nbr   | Store identifier           |
| family      | Product category           |
| sales       | Daily sales                |
| onpromotion | Promotional products count |

Holiday Dataset
Used to incorporate:
*    National Holidays
*    Local Holidays
*    Regional Events

into Prophet forecasting.

<h2><a class="anchor" id="project-structure"></a>Project Structure</h2>

```
Retail-Sales-Forecasting/
│
├── Data/
│   ├── train.csv
│   └── holidays_events.csv
│
├── Notebook/
│   └── Sales_Forecasting.ipynb
│
├── Images/
│   ├── Sales_Trend.png
│   ├── Decomposition.png
│   ├── ACF_PACF.png
│   ├── Model_Comparison.png
│   └── Forecast_90_Days.png
│
└── README.md

```
<h2><a class="tools-technologies" id="overview"></a>Tools & Technologies</h2>

Tools & Technologies
*    Python
*   Pandas
*    NumPy
*    Matplotlib
*    Plotly
*   Statsmodels
*   Pmdarima
*    Prophet
*    Scikit-learn
*    Jupyter Notebook

<h2><a class="anchor" id="time-series-analysis"></a>Time Series Analysis</h2>

Time Series Decomposition

![Decomposition](Images/Decomposition.png)

### Findings :
*    Trend component showed continuous growth
*    Seasonal component revealed recurring demand cycles
*    Residual component captured random fluctuations


<h2><a class="anchor" id="stationarity-testing"></a>Stationarity Testing</h2>

Stationarity Testing
###### Augmented Dickey-Fuller Test

Before Differencing:
-   ADF Statistic = -2.616
-  p-value = 0.0897
## Non-stationary

After Differencing:
- ADF Statistic = -11.4976
- p-value = 0.0000

## Stationary

![Stationary Data](images/Stationary_data.png)

<h2><a class="anchor" id="sarima-modeling"></a>SARIMA Modeling</h2>

SARIMA Modeling

## Auto-ARIMA Best Model
SARIMA(5,1,3)(2,0,1)[7]


| Metric | Value   |
| ------ | ------- |
| MAE    | 138,823 |
| RMSE   | 188,182 |
| MAPE   | 35.43%  |

<h2><a class="anchor" id="prophet-modeling"></a>Prophet Modeling</h2>

Prophet Modeling
### Features Implemented
*    Holiday Effects
*    Weekly Seasonality
*    Yearly Seasonality
*    Custom Monthly Seasonality
*    Automatic Changepoint Detection

![Prophet](images/Prophet_forecast.png)


| Metric | Value   |
| ------ | ------- |
| MAE    | 131,224 |
| RMSE   | 179,400 |
| MAPE   | 41.49%  |

<h2><a class="anchor" id="model-comparison"></a>Model Comparison</h2>

Model Comparison

| Model   |         MAE |        RMSE |       MAPE |
| ------- | ----------: | ----------: | ---------: |
| SARIMA  |     138,823 |     188,182 | **35.43%** |
| Prophet | **131,224** | **179,400** |     41.49% |

### Insights :
*    Prophet achieved lower MAE and RMSE.
*    SARIMA achieved lower MAPE.
*    Prophet was selected for future forecasting because of its ability to model holidays and trend changes.

<h2><a class="anchor" id="90-day-forecast"></a>90-Day Forecast</h2>

90-Day Forecast

![90 -Days Forecast](images/90days_fore.png)

### Forecast Highlights
*    Expected daily sales range:
    *** ~800K to 1.2M units ***
*    Weekly demand cycles continue
*    Confidence intervals quantify forecast uncertainty

<h2><a class="anchor" id="business-impact"></a>Business Impact</h2>

Business Impact

SARIMA MAE  = 138,823
Prophet MAE = 131,224

#### Improvement:
*    7,599 units/day

#### Over 90 days:
*    684,000 units


<h2><a class="anchor" id="author--contact"></a>Author & Contact</h2>

Author & Contact

Abdul Mamtaan

Data Analyst | Python | SQL | Power BI | Machine Learning

Mail : abdulmamtaan8@gmail.com
GitHub: https://github.com/mamtaan
LinkedIn: https://www.linkedin.com/in/abdul-mamtaan/