# Price Prediction Using Range

## 📌 Project Overview

This project uses **Machine Learning** to predict the price of an item based on its **Range** value. The dataset is divided into training and testing sets, and a machine learning regression model is trained to learn the relationship between Range and Price.

The predicted prices are then compared with the actual prices to evaluate the model's performance.

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Jupyter Notebook / Google Colab
* Matplotlib

## 📂 Dataset

The dataset contains the following important columns:

* **Range** – Input feature used for prediction.
* **Price** – Target variable that the model predicts.

## 🔄 Project Workflow

1. Import the required libraries.
2. Load the dataset.
3. Select `Range` as the input feature.
4. Select `Price` as the target variable.
5. Split the dataset into training and testing data.
6. Train the machine learning regression model.
7. Predict prices using the test data.
8. Compare actual and predicted prices.
9. Evaluate the model's performance.

## 💻 Data Preparation

```python
X = df[["Range"]]
Y = df[["Price"]]

X_train, X_test, Y_train, Y_test = train_test_split(
    X, Y, test_size=0.2, random_state=42
)
```

## 📊 Actual vs Predicted Price

The actual and predicted prices are compared using a Pandas DataFrame:

```python
comparison = pd.DataFrame({
    "Actual Price": Y_test["Price"].values,
    "Predicted Price": y_pred
})

print(comparison)
```

## 📈 Model Evaluation

The model can be evaluated using common regression metrics such as:

* Mean Absolute Error (MAE)
* Mean Squared Error
