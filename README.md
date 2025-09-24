# House-Price-Prediction

This project demonstrates how to build and evaluate a machine learning model to predict house prices using the **Boston Housing Dataset (or equivalent housing data)**. The implementation leverages **XGBoost Regressor**, a powerful gradient boosting algorithm, to achieve accurate predictions.

The workflow includes data preprocessing, exploratory data analysis (EDA), model training, evaluation, and visualization of results.

---

## 📂 Project Structure

```
.
├── prediction.py        # Main script containing the workflow
├── housing_Data.csv     # Dataset file (must be placed in the same directory)
└── README.md            # Project documentation
```

---

## ⚙️ Requirements

Ensure you have the following dependencies installed:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn xgboost
```

---

## 📊 Dataset

* The dataset (`housing_Data.csv`) should contain house price data with several independent variables (features) and a target variable named **`price`**.
* Example columns might include:

  * `rooms` – Number of rooms
  * `area` – Size of the property
  * `location` – Categorical location data
  * `price` – Target variable (house price)

The script automatically checks for missing values and computes descriptive statistics.

---

## 🚀 Workflow

1. **Import Dependencies**
   Loads required libraries such as NumPy, Pandas, Matplotlib, Seaborn, Scikit-learn, and XGBoost.

2. **Load Dataset**
   Reads `housing_Data.csv` into a Pandas DataFrame.

3. **Data Exploration & Cleaning**

   * Checks dataset shape, missing values, and statistical measures.
   * Computes correlations and visualizes them with a heatmap.

4. **Feature Engineering**

   * Separates features (`X`) and target (`y`).
   * Converts categorical (object-type) features into `category` dtype for XGBoost.

5. **Train-Test Split**
   Splits the data into **80% training** and **20% testing**.

6. **Model Training**

   * Trains an **XGBoost Regressor** with categorical support enabled.
   * Fits the model on training data.

7. **Evaluation**

   * Predicts house prices for both training and testing datasets.
   * Calculates evaluation metrics:

     * **R² Score (Coefficient of Determination)**
     * **Mean Absolute Error (MAE)**

8. **Visualization**

   * Plots **Actual Prices vs Predicted Prices** for the training set.

---

## 📈 Example Output

**Training Data Metrics:**

```
R Squared Error : 0.95
Mean Absolute Error : 2.13
```

**Test Data Metrics:**

```
R Squared Error : 0.88
Mean Absolute Error : 3.47
```

**Visualization:**
A scatter plot comparing actual vs predicted prices.

---

## ▶️ How to Run

1. Place `housing_Data.csv` in the same folder as `prediction.py`.
2. Run the script:

```bash
python prediction.py
```

3. Check the console for model performance metrics.
4. A correlation heatmap and scatter plot will appear as part of visualization.

---

## 🔮 Future Improvements

* Add **hyperparameter tuning** with `GridSearchCV` or `Optuna`.
* Implement **cross-validation** for better generalization.
* Save and load trained models with `joblib` or `pickle`.
* Create a simple **Flask/Django API** for real-time predictions.

---
