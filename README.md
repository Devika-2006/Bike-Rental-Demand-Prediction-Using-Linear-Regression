# 🚴 Bike Rental Demand Prediction Using Linear Regression

---

# 📝 Project Overview

Bike sharing systems have become an important mode of transportation in many cities. Predicting bike rental demand helps transportation companies and city planners efficiently manage bike availability and improve customer satisfaction.

This project uses a **Linear Regression** model to predict the number of bike rentals based on weather conditions, seasonal information, temperature, humidity, wind speed, and time-related features. The model learns the relationship between these factors and the total number of bike rentals.

---

# 🎯 Objective

The main objectives of this project are:

- Analyze historical bike rental data.
- Predict the number of bike rentals using Linear Regression.
- Understand how weather and seasonal factors influence bike rental demand.
- Apply Machine Learning Regression techniques to a real-world dataset.

---

# 🛠️ Technologies Used

| Technology | Purpose |
|------------|----------|
| Python | Programming Language |
| Pandas | Data Manipulation |
| NumPy | Numerical Computation |
| Scikit-Learn | Machine Learning |
| Matplotlib | Data Visualization |
| Seaborn | Data Visualization |
| Google Colab | Development Environment |
| GitHub | Version Control & Project Hosting |

---

# 📊 Dataset Description

The dataset used in this project contains **17,379 hourly records** collected from a bike-sharing system.

It includes weather conditions, seasonal information, and time-related features that help predict the total number of bike rentals.

## Features (Input Variables)

| Feature | Description |
|----------|-------------|
| Season | Season of the year |
| Year | Year (2011 or 2012) |
| Month | Month of the year |
| Hour | Hour of the day |
| Holiday | Whether the day is a holiday |
| Weekday | Day of the week |
| Working Day | Whether it is a working day |
| Weather Situation | Weather condition |
| Temperature | Normalized temperature |
| Feeling Temperature | Normalized feeling temperature |
| Humidity | Relative humidity |
| Wind Speed | Wind speed |

### Target Variable

| Target | Description |
|---------|-------------|
| **cnt** | Total Bike Rental Count |

---

# 🔄 Project Workflow

```text
Dataset Loading
        ↓
Data Exploration
        ↓
Data Preprocessing
        ↓
Exploratory Data Analysis (EDA)
        ↓
Correlation Analysis
        ↓
Train-Test Split
        ↓
Linear Regression Model Training
        ↓
Prediction
        ↓
Model Evaluation
```

---

# 📈 Exploratory Data Analysis (EDA)

The dataset was explored using different visualization techniques to understand the relationship between the features and bike rental demand.

### Visualizations Performed

- Distribution of Bike Rental Count
- Correlation Heatmap
- Temperature vs Bike Rental Count Scatter Plot

### Key Observations

✅ Bike rental demand generally increases as the temperature rises.

✅ Weather conditions have a significant influence on rental demand.

✅ Higher humidity is associated with lower bike rental activity.

✅ Temperature and feeling temperature are strongly correlated.

✅ Bike rental demand varies depending on the season and hour of the day.

---

# 🤖 Model Building

A **Linear Regression** model was used to predict bike rental demand.

### Why Linear Regression?

- Simple and easy to understand.
- Suitable for predicting continuous numerical values.
- Helps identify relationships between input features and the target variable.
- Serves as a strong baseline model for regression problems.

---

# 📊 Model Performance

The model was evaluated using standard regression metrics.

| Metric | Score |
|---------|--------|
| Mean Absolute Error (MAE) | **104.80** |
| Mean Squared Error (MSE) | **19379.83** |
| Root Mean Squared Error (RMSE) | **139.21** |
| R² Score | **0.388** |

---

# 🏆 Project Results

The Linear Regression model successfully learned the relationship between weather conditions and bike rental demand.

### Overall Performance

- ✅ Mean Absolute Error (MAE): **104.80**
- ✅ Mean Squared Error (MSE): **19379.83**
- ✅ Root Mean Squared Error (RMSE): **139.21**
- ✅ R² Score: **0.388**

The evaluation results show that Linear Regression provides a useful baseline model for predicting bike rental demand. More advanced regression algorithms can be explored to improve prediction accuracy.

---

# 💡 Key Findings

🚴 Higher temperatures generally lead to an increase in bike rental demand.

🌦️ Weather conditions play an important role in influencing bike rentals.

💧 High humidity is associated with lower rental demand.

🕒 Bike rentals are generally higher during peak commuting hours.

📊 Linear Regression provides a simple and effective baseline model for predicting bike rental demand.

---

# 📂 Project Structure

```text
Bike-Rental-Demand-Prediction-Using-Linear-Regression/

├── screenshots/
│   ├── dataset_head.png
│   ├── dataset_shape.png
│   ├── dataset_info.png
│   ├── missing_values.png
│   ├── dataset_statistics.png
│   ├── distribution_histogram.png
│   ├── correlation_heatmap.png
│   ├── temperature_vs_rentals.png
│   ├── train_test_split.png
│   ├── model_trained.png
│   └── model_results.png

├── bike_rental_prediction.ipynb
├── hour.csv
├── requirements.txt
└── README.md
```

---

# 🚀 Future Improvements

- Compare Linear Regression with Decision Tree Regression.
- Compare Linear Regression with Random Forest Regression.
- Perform feature engineering to improve prediction accuracy.
- Tune model parameters for better performance.
- Build a Streamlit web application for real-time predictions.
- Deploy the model using cloud platforms.

---

# 🎓 Learning Outcomes

Through this project, I learned:

- Data Collection and Preprocessing
- Exploratory Data Analysis (EDA)
- Correlation Analysis
- Data Visualization
- Linear Regression
- Train-Test Split
- Regression Evaluation Metrics (MAE, MSE, RMSE, and R² Score)
- GitHub Project Documentation

---

# 📋 Requirements

Install the required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

# 👤 Author

**Devika S**

Computer Science Student | Machine Learning Enthusiast

---

# ⭐ Conclusion

This project demonstrates how **Linear Regression** can be applied to predict bike rental demand using weather, seasonal, and time-related features. It provided practical experience in data preprocessing, exploratory data analysis, regression modeling, and performance evaluation while strengthening my understanding of machine learning regression techniques and their real-world applications.
