# Ride Price Prediction using Machine Learning

## Project Overview
This project predicts ride prices using Machine Learning based on features such as distance, duration, traffic, weather, demand level, and ride type.  
Two models are implemented:  
- **Linear Regression** to estimate ride costs.  
- **Logistic Regression** to classify rides as high-cost or low-cost.  

The workflow includes data generation, preprocessing, encoding, scaling, model training, and performance evaluation.

## Dataset Description
The dataset is **synthetic** and generated directly in the notebook. It contains 200 rides with the following information:  
- Ride distance in kilometers  
- Ride duration in minutes  
- Time of day  
- Traffic level  
- Weather  
- Demand level  
- Ride type (standard or premium)  

The target variable `ride_price` is calculated based on a combination of these features.

## Features Used and Justification
| Feature | Why it was chosen | Influence on ride price |
|---------|-----------------|------------------------|
| `distance_km` | Longer rides generally cost more | Directly proportional to price |
| `duration_min` | Longer rides increase fare | More time spent → higher cost |
| `time_of_day` | Ride demand changes at different times | Peak hours → higher prices |
| `traffic_level` | Traffic affects ride duration | Higher traffic → longer rides → higher cost |
| `weather` | Weather affects demand and conditions | Rainy → higher price due to slower rides and higher demand |
| `demand_level` | High demand periods can increase price | Surge pricing may apply → higher cost |
| `ride_type` | Different ride types have different pricing | Premium rides cost more than standard rides |

**Feature considered but excluded:**  
- `passenger_count`: Excluded because most rides are single passengers, providing little variation.

## How to Run the Notebook
1. Open `ride_price_model.ipynb` in [Google Colab](https://colab.research.google.com/).  
2. Run the notebook cells sequentially.  
3. The dataset is generated automatically, so no CSV upload is needed.  
4. The notebook produces:
   - Linear Regression predictions with Mean Absolute Error (MAE)  
   - Logistic Regression classification with Accuracy and Confusion Matrix  

## Key Findings
- Linear Regression effectively estimates ride prices using the given features, with MAE indicating the average prediction error.  
- Logistic Regression can classify rides as high-cost or low-cost based on feature patterns, achieving good accuracy.  
- Features like distance, duration, demand level, and ride type have the largest impact on ride price.  
- Traffic and weather also contribute to pricing, showing that external conditions matter in ride cost estimation.