# sb-ultimate-challenge
Ultimate Technologies Challenge

# Part 1 - Exploratory data analysis

Please see the following notebook for login EDA

[1-login-eda.ipynb](1-login-eda.ipynb)

# Part 2 - Experiment and metrics design

[2-experiment-and-metric-design.ipynb](2-experiment-and-metric-design.ipynb)



# Part 3 - Predictive Modeling

Please see the following notebooks for detailed work:

* [3.1-ultimate-eda.ipynb](3.1-ultimate-eda.ipynb)
* [3.2-ultimate-feature-engineering.ipynb](3.2-ultimate-feature-engineering.ipynb)
* [3.3-model_training-lr.ipynb](3.3-model_training-lr.ipynb)

For predictive modeling, I used Logistic Regression to predict whether a user is active or not.

I considered using decision tree for this exercise but ultimately decided on using Logistic Regression mainly because:
* Decision Trees tend to overfit
* Logistic Regression is easier to interpret

Our initial model, gave us 58% accuracy. After feature selection, we were able to improve the model performance to 71.5%

### Insight

The following factors have a positive impact on users staying active:

* more rides in the first 30 days
* iphone users
* ulimate black users

These factors have a negative impact on users staying active:

* users with longer average distance

Users in Kings Landing are more likely than users from other cities to stay active with Winterfell being the least likely in being active

Interestingly, average rating of driver and by driver also have an negative impact of on user staying active although impact to our model after removing these was relatively low (~0.002) so we can probably ignore these variables.

Higher average surge prices also has a negative impact on customers staying active. However, this metric depends on time user requests rides which we have no insight to. This variable has been removed from the model.

### Recommendations

Target the following factors since they are highly correlated with users staying active

* Increase number of rides for new users in the first 30 days
* Offer promotions for users who take shorter trips
* iPhone users
* Target users from Kings Landing
* Offer promotions to encourage users to become Ultimate Black users


