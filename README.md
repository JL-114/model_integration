# 🍦 Ice Cream Sales Predictor

A application that predicts daily ice cream cone sales for major U.S. cities using machine learning and live weather forecast data from the Open-Meteo API.

---

## 📌 Project Overview

This project demonstrates how to train a Multiple Linear Regression model in Python, export the trained model using `pickle`, and integrate it into an interactive Streamlit web interface. 

The application retrieves real-time daily temperature forecasts from the [Open-Meteo API](https://open-meteo.com/) for a chosen location and date, combines it with day-of-week classification (Weekday vs. Weekend), and generates sales predictions.

---

## ⚙️ Features & Predictors

The prediction model uses two main features:
1. **`temperature` (°F)**: Daily high temperature forecast retrieved via Open-Meteo API.
2. **`is_weekend` (Binary)**: Automatically computed based on the selected date:
   - `1` = Weekend (Saturday / Sunday)
   - `0` = Weekday (Monday – Friday)

### Model Equation Format
The underlying linear model takes the following form:
$$\text{Sales} = (\text{Coeff}_{\text{temp}} \times \text{temperature}) + (\text{Coeff}_{\text{weekend}} \times \text{is\_weekend}) + \text{Intercept}$$

---

## 📁 Repository Structure

```text
├── app.py              # Streamlit application file
├── model.pkl           # Saved Scikit-Learn linear regression model
├── requirements.txt    # Python dependencies list
└── README.md           # Project documentation

