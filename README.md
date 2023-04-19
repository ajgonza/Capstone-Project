# Customer success
By: 
[Addison Faber](https://github.com/addyb0y) \
[Stephen Smart](https://github.com/stephenpsmart)\
[Brian Bombasi](https://github.com/bombasibrian)\
[Alvaro Gonzalez](https://github.com/ajgonza)

Swire Coca-Cola is seeking to improve its ability to predict the success of new restaurants in its market. To achieve this goal, we will analyze census data, consumer reviews, customer attributes, and Swire's sales to these customers. The data will be used to build a predictive model that can estimate the success of new customers based on historical results. The project will deliver a predictive model, a report on the methodology and results, a software implementation of the model, training and support for stakeholders on how to use and interpret the results, and a live presentation to showcase the findings and explain the methodology and results. 

## Problem Statement
Swire Coca-Cola is struggling to systematically identify the success, profitability, and sales of potential B2B customers. The investment of time, capital, and operating expenses are at risk. Depending on the perceived profitability of the potential customer, Swire can adjust pricing and operational support to make their bid more attractive.

Offering competitive bids to a company that eventually fails will cause a significant loss of investment.

The purpose of this project is to identify and determine two factors:

1) Predict which B2B customer will be successful (exceed the break-even point)

2) How successful a specific customer will be (projected sales)

Success Metrics. How will stakeholders judge whether the project was a success?

Success will be determined by two metrics:

1) How well the utilized analytical models can identify the two factors listed above for both of the following:

a. Current customers

b. New or future customers

2) By determining major contributing factors relating to a B2B customer’s success that may have been unknown by previous contributors and stakeholders alike.

The analytical methods that will be utilized for this project are:

1) Data cleaning and exploration

2) Deployment of predictive model(s) to determine success

3) Supporting/exploratory visualizations

4) Report creation and execution

The current project will provide deliverables along with a select number of predictive models (example if a classification model is deployed only one will be created and tested) and supporting material in a report format. The focus will only be on B2B clients and not B2C.

Future projects could include additional analytical models and testing. The project will be finished by early April 2023. Each of the four points above will be achieved approximately every 2 weeks from the creation of this business problem statement.

Recommendations And Analysis

It is our theory that by utilizing feature engineering and clustering, Swire should be able to build their own regression/classification models to predict profit, transactions, overall risk, and customer lifetime value more accurately.

Due to the disparate geographical nature between Swire’s B2B Partners, as well as the strong contributing factor location has on a business’s success, building any model based off of the entire dataset is futile.

The main argument of our theory is that a cluster (or specific location) containing current B2B Partners will be able to better contribute to the accurate prediction of a potential B2B Partner that Swire is vetting out. If ABC Business is being evaluated by Swire, we can draw on the current knowledge of the cluster to understand if the potential B2B partner, let's say a restaurant, is a good fit for the area. We would compare census data of the area or cluster in question against Coke's target customers or demographics for that area. Next, utilizing Yelp data to understand how well similar current B2B Partners are performing, such as similar restaurants, along with the performance of all restaurants in the area to evaluate general performance. The final piece is evaluating the current B2B Partners’ wait times from Google Analytics. A variety of metrics can be used from Google to understand, overall, how busy and therefore successful a current B2B Partner is. The hypothesis is that the longer the wait times, the busier the Partner is and the more revenue the Partner is generating.

Overall, the more successful a Current and Potential B2B Partner is predicted to be the more likely Coca-Cola’s sales will be higher. Sales are directly related to customer traffic and perception of the Current and Potential B2B Partner. Therefore, we can sufficiently conclude that predicting the overall success of the B2B Partners will help us to better predict profit, transactions, overall risk, and even customer lifetime value for Swire Coca-Cola.


## Exploratory Data Analysis (EDA)

The EDA notebook [link to notebook here](EDA_Swire_coca_cola.html) explores the dataset and provides insights into the distribution of the features, the correlation between the features, and the target variable. The notebook also includes visualizations to help understand the data.

## Modeling

The modeling notebook [link to notebook here](Modeling_Alvaro_Gonzalez.html) or [here](https://ajgonza.github.io/Capstone-Project/)presents the machine learning pipeline used to train and evaluate the model. The pipeline includes data preprocessing, feature engineering, model selection, hyperparameter tuning, and evaluation metrics. The notebook also discusses the performance of the model and provides recommendations for improving the model.

The models were evaluated on several metrics, and the data was split into train, validation, and test sets, with a cross-validation of 3 folds. After reviewing the different measures, we will choose the model with the highest average net benefit. We analyzed the confusion matrix and cost matrix to identify the types of errors the model was making and the cost of each error.

                    |Predicted high risk    |Predicted low risk

	Actual high  |	0    				       | -3733  	
	
	Actual low  | -1300		                  | 1300
 
The cost is related to how it affects the customer's lifetime profit over 3 years. The cost of not signing a good customer is 3733, while the cost of signing a bad customer is 1300. This decision was made based on the median of a high-risk customer, which is 1300 below the median CLTV for 3 years. and a good prediction of a low risk will increase the CLTV by 1300.

The best model was a SVC linear when using all the features of transaction history and products CLVTS. The model had an average net benefit of 1087. in test  and 1077.37  on validation. This types of models take clos to 90 minuts to run.

When the minority class was weighted and run using a grid search for the best  weight was 10 for all models. And the best model was newton logistic regression with a score of 1064.

And finally we run the models to see there performance with fewer features. The best model was the logistic regression by not high diference from other models. This evaluation shsws that reducing to demographic and characteristics of the customers will not higly affect the model performance and will be easier to implement.

## External Data

The project uses data from the United States Census Bureau provided via the [tidycensus](https://walker-data.com/tidycensus/) package. The heatmap displaying the 10 most important variables on TOTAL_PROFIT can be found [here](census_var_imp.png). Please refer to the presentation for variable definitions.

![Variable Importance Heatmap](https://github.com/ajgonza/Capstone-Project/blob/d791bec42adb07a41f3246613f891422a45c7c48/census_var_imp.png)

## Slides Presentation
[link to notebook here](Customer_success_slides.pdf)

## Conclusion

In conclusion, this project demonstrates the importance of building a machine learning model to predict customer churn for subscription-based services. The EDA notebook provides insights into the data, while the modeling notebook presents a machine learning pipeline to build and evaluate the model. The model achieved good performance, but there is still room for improvement. Future work can focus on exploring different models, tuning more hyperparameters, and collecting more data to improve the model's performance.
