# Healthcare-Service-Wait-Time-Prediction

## Dataset Description

This dataset contains healthcare service records generated for analysis and predictive modeling purposes. The data was created using Mockaroo to simulate realistic healthcare service patterns while maintaining privacy and data protection standards.

### Dataset Overview
- **Total Records**: 500
- **Time Period**: 2022
- **Purpose**: Predict patient waiting times in healthcare facilities

### Features Description

| Feature | Description | Data Type |
|---------|-------------|-----------|
| customer_id | Unique identifier for each customer | Integer |
| arrival_time | Time when the customer arrived at the facility | Datetime |
| service_start_time | Time when the service began | Datetime |
| service_end_time | Time when the service was completed | Datetime |
| waiting_time_minutes | Duration between arrival and service start | Integer |
| service_type | Type of service (treatment, consultation, examination) | String |
| customer_rating | Customer satisfaction rating (1-5 scale) | Integer |
| staff_name | Name of the staff member providing service | String |
| department | Department where service was provided | String |
| location | Facility location | String |

### Data Generation Methodology
- Data was generated using Mockaroo
- Relationships and patterns were designed to reflect realistic healthcare service scenarios
- Time distributions were modeled based on typical healthcare facility operations

## Project Objective

The main objective is to develop a machine learning model that can predict patient waiting times based on various factors such as service type, department, time of day, and current facility load.

### Analysis Goals
1. Identify key factors influencing waiting times
2. Understand peak service hours and their impact
3. Analyze relationship between waiting times and customer satisfaction
4. Develop accurate waiting time predictions for better resource allocation

## Model Development

The project includes:
1. Exploratory Data Analysis (EDA)
2. Data preprocessing and feature engineering
3. Model development using Random Forest Regressor
4. Model evaluation and performance metrics

## Usage

```python
# Example code for loading and preparing the data
import pandas as pd
from src.data_preparation import prepare_features
from src.model import train_waiting_time_model

# Load the data
df = pd.read_csv('healthcare_service_data.csv')

# Prepare features
X, y = prepare_features(df)

# Train model
model, metrics = train_waiting_time_model(X, y)
```

## Future Improvements
- Incorporate real-time facility capacity data
- Add seasonal patterns and special event impacts
- Include more detailed service categorization
- Develop API for real-time predictions

## Disclaimer

This is a synthetic dataset created for portfolio demonstration purposes. While it aims to reflect realistic patterns in healthcare services, it should not be used for actual healthcare service planning without proper validation against real-world data.
