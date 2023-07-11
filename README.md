# Phase-2-Project-Readme: House Sales in King County, USA

Author: Joseph Kinuthia Githinji

Student pace: Full Time

Scheduled project review date/time: 1 Week

Instructor name: Anthony Muiko / Winnie Anyoso

## Overview

This project aims to address the business problem faced by a real estate agency, which is to provide homeowners with advice on how home renovations can increase the estimated value of their homes. The analysis utilizes multiple linear regression modeling on the King County House Sales dataset. By examining the relationships between various features of the houses and their sale prices, the model identifies significant factors influencing the sale price, enabling the agency to offer actionable insights to homeowners. The results include a metric describing the overall model performance, such as R-squared, to assess how well the model explains the variation in the sale prices, and at least two regression model coefficients. The recommendations provide guidance to homeowners on renovation decisions that align with their budget and have the potential to maximize the increase in their property's value.

## Business Problem

The business problem this project aims to solve is to provide homeowners with advice on how home renovations might increase the estimated value of their homes and by what amount. This addresses a pain point for the real estate agency as they aim to assist homeowners in making informed decisions about their renovations and potentially maximize the value of their properties.

***
### Questions to consider:

*Which features of a house have a significant impact on its sale price?

*How does each feature contribute to the variation in sale prices?

*How accurately can we predict the sale price of a house based on its features?

***
These data questions are crucial to understand the factors that influence the sale price of a house and to quantify the impact of each feature. By answering these questions, homeowners can leverage actionable insights regarding which features they should focus on during renovations to maximize the potential increase in their property's value.

These questions are important from a business perspective because they allow the real estate agency to provide tailored recommendations to homeowners. By identifying the features that have a significant impact on the sale price, the agency can guide homeowners in making renovation decisions that are more likely to yield a higher return on investment. 

Accurate predictions of sale prices can further assist homeowners in setting appropriate listing prices and negotiating offers, ensuring they make informed decisions throughout the selling process. Ultimately, this analysis adds value by providing data-driven insights to homeowners, helping them maximize the estimated value of their homes and achieve their goals in terms of renovation and property value.


## Data Understanding

***
Questions to consider:
* Where did the data come from, and how do they relate to the data analysis questions?

The data was sourced from a real estate agency and contains information on house sales in King County. The dataset is relevant to our data analysis questions as it allows us to explore the relationships between various house features and the sale price. By analyzing these relationships, this project provides insights and recommendations to homeowners regarding home renovations.

* What do the data represent? Who is in the sample and what variables are included?

The data represent houses sold in King County, USA. Each observation in the dataset represents a unique house and includes various variables related to the house's attributes, such as the number of bedrooms, bathrooms, square footage, condition, location, and more. The sample consists of houses sold within a specific time period in King County.

* What is the target variable?

The target variable in this analysis is the "price" column, which represents the sale price of the houses. This is the variable we aim to predict using the other independent variables in the dataset.

* What are the properties of the variables you intend to use?

The project uses various independent variables (features) from the dataset to predict the sale price. These variables include the number of bedrooms, bathrooms, square footage, condition, grade, presence of waterfront, view quality, year built, year renovated, location coordinates, and more. These variables have different data types, including numerical, categorical, and geographic coordinates. It will assess the properties of these variables, handle missing values, outliers, and transform them as necessary for the regression modeling process. 

***

# Modelling

*Data Preprocessing: This step involves handling missing values, handling categorical variables (encoding), scaling numerical variables.

*Exploratory Data Analysis (EDA): This involves analyzing and visualizing the data to gain insights into the relationships between variables, identifying patterns, and detecting outliers or anomalies.

*Baseline Model: Fit a baseline model, such as simple linear regression, using a single predictor variable (e.g., sqft_living) to establish a baseline for model comparison.

*Model Building: Build multiple regression models by selecting a combination of predictor variables based on domain knowledge, correlation analysis, and feature importance. Fit the models using an appropriate regression algorithm (e.g., Ordinary Least Squares).

*Model Evaluation: Evaluate the performance of the models using metrics such as R-squared, adjusted R-squared, and F-statistic. Compare the models to determine which one provides the best fit to the data.

*Summarize the findings of the analysis and provide recommendations based on the regression models.

# Modelling Results
***
When comparing the three models, here are some key observations made from the project:

*Model 1:

R-squared: 0.493
This model includes only the "sqft_living" variable as a predictor.
The model explains approximately 49.3% of the variance in the target variable, "price".
The coefficients indicate that, on average, for each unit increase in square footage, the price is expected to increase by $280.8630.

*Model 2:

R-squared: 0.501
This model includes four predictor variables: "sqft_living", "sqft_above", "sqft_living15", and "bathrooms".
The model explains approximately 50.1% of the variance in the target variable.
The coefficients indicate the expected change in price for each unit increase in the respective predictor variable, while holding other variables constant.

*Model 3:

R-squared: 0.606
This model includes multiple predictor variables, such as sqft_living, sqft_above, bedrooms, waterfront_YES, floors, grade_11 Excellent, grade_10 Very Good, grade_7 Average, grade_13 Mansion and grade_12 Luxury.
The model explains approximately 61.8% of the variance in the target variable.
The coefficients represent the expected change in price for each unit increase in the respective predictor variable, considering the effects of other variables in the model.

Based on the R-squared values, Model 3 has the highest level of explained variance compared to the other models. This suggests that Model 3 performs better in capturing the variation in the target variable, "price". However, it is important to note that there might be other factors or variables that could further improve the model's performance.

*Comparison of the models:

The R-squared value increases from the first model (0.493) to the second model (0.501) and further to the third model (0.618). This indicates that each subsequent model explains a higher percentage of the variance in house prices, suggesting improved model performance.

The inclusion of additional variables in the second and third models allows for a more comprehensive understanding of the factors influencing house prices. While the first model solely relies on 'sqft_living', the third model expands further by incorporating many variables.

Overall, the third model demonstrates the highest R-squared value and includes a more extensive set of predictor variables, indicating the best fit to the data and potentially capturing more of the underlying relationships between predictors and house prices.
***

## Conclusions
***
Based on the analysis conducted, the following conclusions can be drawn:

Predictor Variables: The p-values associated with the coefficients in Model 3 indicate that '(sqft_living, sqft_above, bedrooms, waterfront_YES, floors, grade_11 Excellent, grade_10 Very Good, grade_7 Average, grade_13 Mansion and grade_12 Luxury) have a significant impact on housing prices (p-values < 0.05). This suggests that these predictors are important factors to consider when predicting housing prices.

Model Performance: The R-squared values of the models indicate that they explain a significant portion of the variance in house prices. The third model, which includes a combination of numerical and categorical variables, performs the best with an R-squared of 0.618. This suggests that the model can capture approximately 60.6% of the variability in house prices.
***

## Recommendations

Utilize the Third Model: Based on the performance metrics, it is recommended to use the third model as it provides the best fit to the data and includes a comprehensive set of predictor variables. This model can be used to estimate house prices based on the given features.

Further Analysis: Explore additional variables and interactions that may have an impact on house prices. Consider incorporating more advanced techniques such as feature engineering, dimensionality reduction, or non-linear models to capture complex relationships and improve the model's predictive power.

## Limitations

The analysis is based on a specific dataset, and the conclusions and recommendations are specific to that dataset. The generalizability of the models may be limited to similar housing markets and geographical areas. 

The models used in this analysis are relatively simple linear regression models. They assume a linear relationship between the predictors and the target variable, which may not always hold true. More complex relationships, interactions between predictors, and nonlinear patterns may exist in the housing market, which are not captured by these models.

The presence of multicollinearity among the predictors can affect the interpretation and reliability of the coefficient estimates. 

## Improvement Opportunities:

Feature Engineering: Explore additional transformations or combinations of variables that may enhance the predictive power of the model. Feature engineering techniques like polynomial features, logarithmic transformations, or interaction terms could capture non-linear relationships.

Cross-Validation: Implement cross-validation techniques to assess the models' performance on unseen data and mitigate overfitting issues. This helps ensure that the models generalize well beyond the training dataset.

External Data: Incorporate additional external data sources, such as neighborhood characteristics, economic indicators, or property market trends, to enrich the models and capture more comprehensive insights into house price dynamics.

Model Deployment: Develop a user-friendly interface or application that allows stakeholders to input property features and obtain estimated house prices. Regularly update the model with new data to improve its accuracy and relevance over time.

By considering these recommendations and addressing the limitations, the business can make informed decisions regarding house pricing, property valuation, and investment strategies.
***
