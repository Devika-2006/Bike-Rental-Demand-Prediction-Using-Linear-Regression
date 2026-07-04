# 🚴 Bike Rental Demand Prediction Using Linear Regression
Predicting the number of bike rentals is crucial for bike-sharing companies and city planners to manage fleet availability, optimize operations, and improve user satisfaction. This project implements a **Machine Learning Regression** pipeline using Python to predict bike rental counts based on environmental, seasonal, and temporal features.

## 📝 Project Overview
Bike sharing systems have become an important mode of transportation in many cities. Predicting the number of bike rentals helps transportation companies and city planners better manage bike availability and improve customer satisfaction.
This project uses Machine Learning Regression to predict the number of bike rentals based on factors such as season, weather, temperature, humidity, wind speed, and time of the day. A Linear Regression model is trained to learn the relationship between these features and the total number of bike rentals.
---
## 🎯 Objective
*   **Analyze** historical bike rental demand patterns to discover key trends.
*   **Evaluate** how weather, temperature, humidity, wind speed, and time of day influence bike rental counts.
*   **Train** a baseline Linear Regression model to predict the total hourly rental count (`cnt`).
*   **Measure** the performance of the model using standard regression evaluation metrics.
The main objectives of this project are:
*   Analyze bike rental demand using historical data.
*   Predict the number of bike rentals using Linear Regression.
*   Understand how weather and environmental factors affect bike rentals.
*   Apply Machine Learning Regression techniques to a real-world dataset.
---
## 🛠️ Technologies & Libraries Used
| Technology / Library | Purpose |
## 🛠️ Technologies Used
| Technology | Purpose |
| :--- | :--- |
| **Python 3.14+** | Core Programming Language |
| **Pandas** | Data Ingestion, Manipulation & Clean-up |
| **NumPy** | Numerical Operations |
| **Matplotlib & Seaborn** | Exploratory Data Analysis & Visualization |
| **Scikit-learn** | Model Selection, Training, and Evaluation |
| **Python** | Programming Language |
| **Pandas** | Data Manipulation |
| **NumPy** | Numerical Computation |
| **Scikit-Learn** | Machine Learning |
| **Matplotlib** | Data Visualization |
| **Seaborn** | Data Visualization |
| **Google Colab** | Development Environment |
| **GitHub** | Version Control & Project Hosting |
---
## 📊 Dataset Details (`hour.csv`)
The dataset contains **17,379 hourly records** representing bike-sharing rentals in a 2-year history. The key columns are:
*   `instant`: Record index
*   `dteday`: Date of the record
*   `season`: Season ($1$: spring, $2$: summer, $3$: fall, $4$: winter)
*   `yr`: Year ($0$: 2011, $1$: 2012)
*   `mnth`: Month ($1$ to $12$)
*   `hr`: Hour of the day ($0$ to $23$)
*   `holiday`: Whether the day is a holiday or not
*   `weekday`: Day of the week
*   `workingday`: If day is neither weekend nor holiday ($1$), otherwise ($0$)
*   `weathersit`: Weather situation category ($1$ to $4$)
*   `temp`: Normalized temperature in Celsius
*   `atemp`: Normalized feeling temperature in Celsius
*   `hum`: Normalized humidity
*   `windspeed`: Normalized wind speed
*   `casual`: Count of casual users
*   `registered`: Count of registered users
*   `cnt`: Count of total rental bikes (Target Variable, sum of `casual` and `registered`)
## 📊 Dataset Description
The dataset contains **17,379 records** of hourly bike rental information.
---
### Features (Input Variables)
| Feature | Description |
| :--- | :--- |
| **🌸 Season** | Season of the year |
| **📅 Year** | Year (2011 or 2012) |
| **📆 Month** | Month of the year |
| **🕒 Hour** | Hour of the day |
| **🎉 Holiday** | Whether the day is a holiday |
| **📍 Weekday** | Day of the week |
| **💼 Working Day** | Whether it is a working day |
| **🌦️ Weather Situation** | Weather condition |
| **🌡️ Temperature** | Normalized temperature |
| **🌤️ Feeling Temperature** | Normalized feeling temperature |
| **💧 Humidity** | Relative humidity |
| **🌬️ Wind Speed** | Wind speed |
## 🔄 Machine Learning Workflow
### Target Variable
| Target | Description |
| :--- | :--- |
| **🚴 Bike Rental Count (cnt)** | Total number of bikes rented |
```mermaid
graph TD
    A[Data Loading & Preview] --> B[Exploratory Data Analysis]
    B --> C[Data Preprocessing & Feature Selection]
    C --> D[Train-Test Split 80/20]
    D --> E[Linear Regression Model Training]
    E --> F[Evaluation Metrics MAE, MSE, RMSE, R²]
---
## 🔄 Project Workflow
```
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
### 1. Exploratory Data Analysis (EDA)
*   Visualized the distribution of the target variable `cnt` (skewed distribution showing higher frequency for low-demand hours).
*   Analyzed temperature features against rental count, indicating a strong positive correlation where higher temperatures (up to a threshold) increase demand.
*   Plotted a correlation matrix heatmap to check for collinearity (e.g., high correlation between `temp` and `atemp`).
---
### 2. Preprocessing & Feature Engineering
*   Dropped identifiers and leak variables (`instant`, `dteday`, `casual`, `registered`) that directly sum to the target.
*   Selected independent variables: `season`, `yr`, `mnth`, `hr`, `holiday`, `weekday`, `workingday`, `weathersit`, `temp`, `atemp`, `hum`, `windspeed`.
## 📈 Exploratory Data Analysis (EDA)
During the analysis phase, several interesting patterns were observed.
### 3. Model Training & Splitting
*   **Split Ratio:** 80% Training Data, 20% Testing Data (`random_state=42`).
*   **Model:** Ordinary Least Squares Linear Regression.
### Key Observations
*   ✅ Bike rentals generally increase as the temperature becomes warmer.
*   ✅ Weather conditions have a noticeable impact on rental demand.
*   ✅ Humidity and wind speed slightly affect the number of bike rentals.
*   ✅ Temperature and "feeling temperature" are highly correlated.
*   ✅ Bike rental demand varies depending on the season and hour of the day.
---
## 📈 Model Performance & Evaluation
Evaluating the model on the test dataset yielded the following results:
## 🤖 Model Building
A Linear Regression model was used to predict bike rental demand.
| Metric | Score / Value | Description |
| :--- | :--- | :--- |
| **Mean Absolute Error (MAE)** | `104.80` | Average absolute prediction error in rental count. |
| **Mean Squared Error (MSE)** | `19,379.83` | Average squared difference between predictions and actuals. |
| **Root Mean Squared Error (RMSE)** | `139.21` | Standard deviation of the residuals. |
| **R² Score (Coefficient of Determination)** | `0.388` | Explains $\approx 38.8\%$ of the variance in rental demand. |
### Why Linear Regression?
*   Simple and easy to understand.
*   Suitable for predicting continuous numerical values.
*   Helps identify relationships between input features and the target.
*   Serves as a strong baseline regression model.
---
## 🚀 How to Install and Run Locally
## 📊 Model Performance
The model was evaluated using standard regression metrics.
### 1. Clone or Move to the Directory
Ensure you are in the project folder:
```bash
cd Bike-Rental-Demand-Prediction-Using-Linear-Regression
```
| Metric | Score |
| :--- | :--- |
| **Mean Absolute Error (MAE)** | `104.80` |
| **Mean Squared Error (MSE)** | `19379.83` |
| **Root Mean Squared Error (RMSE)** | `139.21` |
| **R² Score** | `0.388` |
### 2. Set Up a Virtual Environment (Optional but Recommended)
```bash
python -m venv .venv
# On Windows (PowerShell):
.venv\Scripts\Activate.ps1
# On Linux/macOS:
source .venv/bin/activate
```
---
### 3. Install Dependencies
```bash
pip install -r requirements.txt
## 🏆 Project Results
The Linear Regression model successfully predicted bike rental demand based on weather and time-related features.
### Overall Performance
*   ✅ **Mean Absolute Error (MAE):** `104.80`
*   ✅ **Mean Squared Error (MSE):** `19379.83`
*   ✅ **Root Mean Squared Error (RMSE):** `139.21`
*   ✅ **R² Score:** `0.388`
The model learned the relationship between environmental conditions and bike rental demand, providing a useful baseline for future improvements.
---
## 💡 Key Findings
*   🚴 **Temperature** has a positive influence on bike rental demand.
*   🌦️ **Weather conditions** affect the number of bikes rented.
*   💧 **Higher humidity** generally reduces bike rental activity.
*   🕒 **Rental demand** changes throughout the day depending on commuting hours.
*   📊 **Linear Regression** provides a simple baseline model, though more advanced regression algorithms may achieve better accuracy.
---
## 📂 Project Structure
```
Bike-Rental-Demand-Prediction-Using-Linear-Regression/
├── screenshots/
│   ├── distribution_histogram.png
│   ├── correlation_heatmap.png
│   ├── temperature_vs_rentals.png
│   ├── train_test_split.png
│   └── model_results.png
├── bike_rental_prediction.ipynb
├── hour.csv
├── requirements.txt
└── README.md
```
### 4. Run the Analysis Jupyter Notebook
Ensure you have Jupyter installed (`pip install jupyter`), then run:
---
## 🚀 Future Improvements
*   Compare Linear Regression with Decision Tree Regressor and Random Forest Regressor.
*   Perform feature engineering to improve predictions.
*   Tune model parameters for better performance.
*   Build a web application using Streamlit.
*   Deploy the model for real-time bike rental prediction.
---
## 🎓 Learning Outcomes
Through this project, I learned:
*   Data Collection and Preprocessing
*   Exploratory Data Analysis (EDA)
*   Correlation Analysis
*   Regression Algorithms (Linear Regression)
*   Train-Test Split
*   Model Evaluation using MAE, MSE, RMSE, and R² Score
*   GitHub Project Documentation
---
## 📋 Requirements
Install the required Python libraries:
```bash
jupyter notebook bike_rental_prediction.ipynb
pip install pandas numpy matplotlib seaborn scikit-learn
```
---
## 🔮 Future Improvements & Recommendations
While the baseline Linear Regression model provides a starting point, a score of $R^2 \approx 0.388$ indicates that the relationship is non-linear.
*   **Feature Engineering:** Extract cyclical features for time and calendar parameters (sine/cosine transformation on `hr` and `mnth`).
*   **Non-Linear Models:** Train and compare Tree-Based methods such as:
    *   *Decision Tree Regressor*
    *   *Random Forest Regressor* (often achieves $R^2 > 0.85$ on this dataset due to hourly/weather thresholds)
    *   *Gradient Boosting Machines* (e.g., XGBoost, LightGBM)
*   **Regularization:** Implement Ridge and Lasso Regression to prevent potential overfitting and perform feature selection.
## 👤 Author
**Devika S**
*Computer Science Student | Machine Learning Enthusiast*
---
## ⭐ Conclusion
This project demonstrates how Linear Regression can be used to predict bike rental demand using weather and time-related features. The model successfully learned the relationship between the input variables and the target value, providing a solid foundation for understanding regression techniques and building more advanced predictive models in the future.
