# Vehicle-Price-Prediction

## Description
This project implements a vehicle price prediction model using machine learning techniques. The model predicts the price of vehicles based on various features such as make, model, year, mileage, and more.

## Dataset
The dataset used for this project is stored in `dataset.csv`. It contains various features related to vehicles, including:
- Make
- Model
- Year
- Mileage
- Price
- Transmission
- Fuel type
- Body type
- And more...

## Data Visualization
Visualizations were created to analyze the data and understand the relationships between features. Key visualizations include:
- Residual plots to evaluate model performance.
  ![Residual plot](https://github.com/user-attachments/assets/79c2e83c-6289-45f0-9243-b805bb89cf10)

- Distribution plots for price and mileage.

## Machine Learning Models
The following machine learning models were implemented:
- **Random Forest Regressor**: Used for predicting vehicle prices based on the features provided.
- **Ridge Regression**: An alternative model that can be used for comparison.

## Data Preprocessing
Data preprocessing involved handling missing values and cleaning the dataset. Rows with missing target variable `price` and important feature `mileage` were dropped to ensure data integrity. Infrequent categories in the `make` and `model` columns were grouped into an "Other" category to reduce noise and improve model generalization.

## Feature Engineering
Feature engineering included creating a new feature `age` by calculating the difference between the current year (2025) and the vehicle's manufacturing year. Additionally, the target variable `price` was log-transformed to reduce skewness and improve model performance.


## Evaluation Metrics
Model performance was evaluated using Mean Squared Error (MSE) and R-squared (R2) metrics. The following results were obtained:
- Mean Squared Error: [0.02524552643345379]
- R-squared: [0.7922197639245788]

## Model Persistence
The trained model pipeline was saved to a file using pickle, allowing for easy reuse and deployment without retraining.

## Prediction Function
A function was defined to predict the price of a new vehicle based on its specifications. 

### Example Usage
```python
predicted_price = predict_price(
    make='jeep',
    model='wagoneer',
    year=2024,
    cylinders=6,
    fuel='Gasoline',
    mileage=10000,
    transmission='Automatic',
    body='SUV',
    exterior_color='Red',
    interior_color='Black',
    drivetrain='Four-wheel Drive',
    age=2
)
print("Predicted Price: ", predicted_price)
```
## Conclusion
This project successfully developed a Random Forest regression model to predict vehicle prices based on various features. The preprocessing and feature engineering steps improved model accuracy and robustness. The evaluation metrics indicate reasonable performance, and the saved model and prediction function facilitate easy deployment and use for new vehicle price predictions.

