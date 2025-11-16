# British Airways Data Science Virtual Experience

This repository contains my work for the British Airways Data Science Virtual Experience program, hosted on the Forage platform. This simulation involved two tasks: forecasting lounge demand based on flight schedules and building a predictive model to understand customer booking behavior.

### 🛠️ Tech Stack

* **Python**
* **Pandas** (for data manipulation and analysis)
* **Scikit-learn** (for `RandomForestClassifier`, `train_test_split`, `cross_val_score`)
* **Matplotlib** & **Seaborn** (for data visualization)
* **Jupyter Notebook** (for analysis and modeling)

---

## Task 1: Lounge Demand Forecasting

**Objective:** To analyze flight schedules and build a lookup table to help British Airways estimate lounge demand and optimize space at Heathrow Terminal 3.

### My Approach

1.  **Analyzed** and **grouped** 10,000 flights based on `HAUL` (Short/Long), `ARRIVAL_REGION` (e.g., Europe, North America), and `TIME_OF_DAY` (e.g., Morning, Midday, Evening).
2.  **Developed** a set of logical assumptions and multipliers to model premium travel behavior across these different flight groups.
3.  **Created** a final "Lounge Eligibility Lookup Table" estimating the percentage of passengers eligible for the Concorde Room (Tier 1), First Lounge (Tier 2), and Club Lounge (Tier 3) for any given flight category.

---

## Task 2: Predicting Customer Booking Behavior

**Objective:** To build a machine learning model to predict which customers are most likely to complete a booking, helping BA be more proactive in its sales process.

### My Approach

1.  **Data Preparation:** Loaded and cleaned the `customer_booking.csv` dataset. Performed one-hot encoding on categorical features (like `route`, `sales_channel`, `flight_day`) to prepare the data for modeling.
2.  **Model Training:** Built a `RandomForestClassifier` to predict the `booking_complete` target variable.
3.  **Model Evaluation:** The model was trained and evaluated, achieving:
    * **85.02% Accuracy** (from 5-fold cross-validation)
    * **85% Accuracy** (on the held-out test set)
    * **63% Precision** (for correctly identifying completed bookings)
4.  **Key Findings:** Analyzed the model's feature importances to identify the top drivers of booking completion. The top 5 predictors were:
    1.  Route (`route_TGGTR`)
    2.  Purchase Lead Time (`purchase_lead`)
    3.  Flight Hour (`flight_hour`)
    4.  Flight Day (`flight_day_Sat`)
    5.  Booking Origin (`booking_origin_Malaysia`)
5.  **Final Output:** Summarized these findings into a one-slide presentation for management, providing actionable recommendations.

---

```

## How to Use

1.  Clone this repository: `git clone https://github.com/your-username/BA_Data_Science_Simulation.git`
2.  Navigate to either the `Task_1_Lounge_Demand/` or `Task_2_Booking_Prediction/` folder.
3.  Open the Jupyter Notebook (`.ipynb`) to review the code and analysis.
