# Ride Price Estimation System

## Project Overview
This project builds an end-to-end machine learning system to estimate ride prices based on trip and contextual features.

The objective is to simulate a real-world machine learning workflow, including dataset design, data preprocessing, regression modeling, classification modeling, and ethical analysis.

## Dataset Description
The dataset was synthetically generated and contains 250 rows.

**Target Variable:**  
- ride_price

**Features Used:**  
- distance_km  
- duration_min  
- time_of_day  
- traffic_level  
- weather  
- demand_level  
- vehicle_type  

The dataset includes both numerical and categorical variables.

**Feature Justification:**  
- Distance and duration directly impact operational cost.  
- Demand level and weather simulate surge pricing.  
- Vehicle type reflects service tier differences.  
- Traffic level and time of day model contextual pricing variations.

**Excluded Feature:**  
- driver_rating (excluded because it does not directly affect pricing in most systems).

## Models

### 1. Linear Regression
Used to predict continuous ride prices.  

**Evaluation Metrics:**  
- Mean Squared Error (MSE)

### 2. Logistic Regression
Used to classify rides as:  
- High-Cost  
- Low-Cost  

**Evaluation Metrics:**  
- Accuracy  
- Confusion Matrix

## Key Findings
- Distance is the most influential feature in ride price prediction.  
- Premium vehicle selection significantly increases ride cost.  
- The regression model successfully captured pricing trends.  
- Classification model achieved strong accuracy in distinguishing high-cost rides.

## Ethical Considerations
- Surge pricing may unintentionally disadvantage certain areas.  
- Model inaccuracies could cause unfair pricing.  
- Synthetic data limits real-world generalization.

## How to Run This Project
1. Clone the repository  
2. Open `ride_price_model.ipynb` in Google Colab or Jupyter Notebook  
3. Run all cells in order

**Dependencies:**  
- pandas  
- numpy  
- matplotlib  
- scikit-learn
