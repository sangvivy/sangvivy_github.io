# 🎓 GPA Forecast Dashboard

**Predict and visualize student GPA trends using ARIMA, SARIMA, and Holt-Winters models in Python.**

---

## 📝 Project Overview

This **Streamlit** web application allows users to upload a CSV file containing student GPA data and forecast future GPA trends. The dashboard supports multiple time series forecasting models including **ARIMA**, **SARIMA**, and **Holt-Winters (additive)**. Users can select individual students, visualize historical GPA data, inspect model diagnostics, and download forecasted results.

**Key Features:**
- 📤 Upload CSV or load a default `student_gpa.csv`
- 🧹 Preprocess and clean GPA time series
- 📅 Handle semesters as time points (`Spring`, `Summer`, `Fall`)
- 📈 Forecast GPA for the next **1–8 semesters**
- 📊 Evaluate models with **RMSE**, **MAE**, and **MAPE**
- 🖼 Interactive visualizations of historical data, forecasts, and diagnostics
- 💾 Download forecast tables as CSV

---

## ⚡ Installation

1. **Clone the repository:**
```bash
git clone https://github.com/yourusername/gpa-forecast-dashboard.git
cd gpa-forecast-dashboard
````

2. **Create a virtual environment (recommended):**

```bash
python -m venv venv
venv\Scripts\activate   # Windows
source venv/bin/activate  # macOS/Linux
```

3. **Install dependencies:**

```bash
pip install -r requirements.txt
```

> If you don’t have a `requirements.txt`, install manually:

```bash
pip install streamlit pandas numpy matplotlib scikit-learn statsmodels pmdarima
```

---

## 🚀 Usage

Run the app with:

```bash
streamlit run app.py
```

**Steps to use:**

1. Upload a CSV file containing these columns:

   * `studentID` (unique identifier)
   * `Year` (e.g., 2023)
   * `Semester` (`Spring`, `Summer`, `Fall`)
   * `GPA` (numeric, 0–4.0)
2. Select a student from the dropdown.
3. Adjust forecast horizon using the slider (1–8 semesters).
4. View forecasts, metrics, and diagnostics.
5. Download forecast tables as CSV.

---

## 📁 File Structure

```
gpa-forecast-dashboard/
│
├── app.py               # Main Streamlit app
├── student_gpa.csv      # Example dataset (optional)
├── requirements.txt     # Python dependencies
└── README.md            # Project documentation
```

---

## 📊 Forecast Models

* **ARIMA** – Auto-regressive Integrated Moving Average
* **SARIMA** – Seasonal ARIMA with quarterly seasonality
* **Holt-Winters** – Additive trend and seasonality

**Metrics for evaluation:**

* RMSE (Root Mean Squared Error)
* MAE (Mean Absolute Error)
* MAPE (Mean Absolute Percentage Error)

---

## 🛠 Dependencies

* Python 3.8+ (tested on 3.12)
* Streamlit
* pandas, numpy, matplotlib
* scikit-learn
* statsmodels
* pmdarima (optional for auto_arima)

---

## 💡 Tips

* Use diagnostics (ACF, PACF, seasonal decomposition) to understand trends and seasonality.
* Ensure semester names are standardized: `Spring`, `Summer`, `Fall`.
* Forecast results may be unstable for very short series (<6 observations).

---
