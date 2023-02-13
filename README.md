# Bike-Share-Predictive-Analytics-Python-Project
## Project Summary
- Data was taken from Bike Sharing Dataset (https://archive.ics.uci.edu/ml/datasets/bike+sharing+dataset)
- Build three models to predict bicycle rental.
- Side note: (1) This was a team project, I mainly contributed to the creation of model 2.

## Model 1: Multiple Linear Regression
- Preparing the data and Feature Engineering by carrying out outlier removal, categorical data transformation and treating the multicollinearity issue
- Understand the factors affecting the total number of users at any given hour
- Findings: 
  - Top three factors influencing the total number of users at any given hour: (1) hour of the day, (2) working day, and (3) humidity level.
  - The number of users at any given hour is also related to the square root of the humidity level by a coefficient of -159 which indicates a non-linear inverse relationship between the two variables.
- Inference: Most users rent bicycles as part of their journey to work. 

## Model 2: Time Series Model
- Holt-Winter’s triple exponential smoothing method was employed to analyse the seasonal component of the model, and to make predictions for the total monthly user count for the next half a year
- Bike users are the most active between May and September, followed by a sharp decline with the least active months being between November and February. We hypothesised that this could be attributed to the cold temperature in these periods when roads were slippery due to snow, making it less suitable for one to cycle around the city.

## Model 3: Logistic Regression
- Explore whether casual and registered users were renting based on different motivations or consumer behaviours
- Findings: The log-likelihood of larger casual use is higher on holidays and non-working days. It is also the lowest at 8AM and 6PM every day, between which it increases.
- Inference: Intuitively, a user is unlikely to cycle to work or school on a one-off basis, and likely makes this trip everyday. As such, the unlimited monthly use price is a more attractive offer and they would opt to be registered. Once registered, users are more likely to frequently use bikes since there is no marginal cost to them. Casual users only seem to exceed in periods where registered usage is extremely low, like working hours, or during specific instances like weekends and some holidays.

## Limitations:
- Insufficient data: Since we were given a dataset of two years, we were only able to aggregate the data to form 24 monthly data points, which may be insufficient to reliably forecast for the next year.
