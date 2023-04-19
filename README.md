# Customer success
By: 

Swire Coca-Cola is seeking to improve its ability to predict the success of new restaurants in its market. To achieve this goal, we will analyze census data, consumer reviews, customer attributes, and Swire's sales to these customers. The data will be used to build a predictive model that can estimate the success of new customers based on historical results. The project will deliver a predictive model, a report on the methodology and results, a software implementation of the model, training and support for stakeholders on how to use and interpret the results, and a live presentation to showcase the findings and explain the methodology and results. 

## Problem Statement



## Exploratory Data Analysis (EDA)

The EDA notebook [link to notebook here](EDA_Swire_coca_cola.html) explores the dataset and provides insights into the distribution of the features, the correlation between the features, and the target variable. The notebook also includes visualizations to help understand the data.

## Modeling

The modeling notebook [link to notebook here](Modeling_Alvaro_Gonzalez.html) or [here](https://ajgonza.github.io/Capstone-Project/)presents the machine learning pipeline used to train and evaluate the model. The pipeline includes data preprocessing, feature engineering, model selection, hyperparameter tuning, and evaluation metrics. The notebook also discusses the performance of the model and provides recommendations for improving the model.

## External Data

The project uses data from the United States Census Bureau provided via the [tidycensus](https://walker-data.com/tidycensus/) package. The heatmap displaying the 10 most important variables on TOTAL_PROFIT can be found [here](census_var_imp.png). Please refer to the presentation for variable definitions.

![Variable Importance Heatmap](https://github.com/ajgonza/Capstone-Project/blob/d791bec42adb07a41f3246613f891422a45c7c48/census_var_imp.png)

## Slides Presentation
[link to notebook here](Customer_success_slides.pdf)

## Conclusion

In conclusion, this project demonstrates the importance of building a machine learning model to predict customer churn for subscription-based services. The EDA notebook provides insights into the data, while the modeling notebook presents a machine learning pipeline to build and evaluate the model. The model achieved good performance, but there is still room for improvement. Future work can focus on exploring different models, tuning more hyperparameters, and collecting more data to improve the model's performance.
