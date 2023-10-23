# Restaurant-Revenue-Prediction---Regression
**Introduction:**
Food industry plays a crucial part in the enhancement of the country’s economy. This mainly plays a key role in metropolitan cities. Where restaurants are essential parts of social gatherings and in recent days there are different varieties of quick-service restaurants like food trucks and takeaways. With this recent rise in restaurant types, it is difficult to decide when and where to open a new restaurant
**Type of Machine learning problem:**
We are asked to predict the revenue of the restaurant in a given year, this problem can be best framed as a Regression problem.
Dataset: https://www.kaggle.com/c/restaurant-revenue-prediction
**File Description**
train.csv - the training set. Use this dataset for training your model.
test.csv - the test set. To deter manual "guess" predictions, Kaggle has supplemented the test set with additional "ignored" data. 
**Data Details**
Id : Restaurant id.
Open Date : opening date for a restaurant
City : City that the restaurant is in. Note that there are unicode in the names.
City Group: Type of the city. Big cities, or Other.
Type: Type of the restaurant. FC: Food Court, IL: Inline, DT: Drive Thru, MB: Mobile P1, P2 - P37: There are three categories of these obfuscated data. Demographic data are gathered from third party providers with GIS systems. These include population in any given area, age and gender distribution, development scales. Real estate data mainly relate to the m2 of the location, front facade of the location, car park availability. Commercial data mainly include the existence of points of interest including schools, banks, other QSR operators.
Revenue: The revenue column indicates a (transformed) revenue of the restaurant in a given year and is the target of predictive analysis. Please note that the values are transformed so they don't mean real dollar values.

**Evaluation Metric:**
The most efficient and commonly used evaluation metrics in regression problems.
**Root Mean Squared Error(RMSE):**
RMSE is the most popular evaluation metric where it follows an assumption that errors obtained are unbiased and follow a normal distribution. RMSE is the square root of average squared residuals/errors.
Residuals = y_actual - y_predicted IMG1.png

Here, the errors are squared before they get averaged, this implies that higher weight is assigned to larger errors which means model performance gets drastically affected when large errors are present.
The Squareroot in RMSE makes the scale of the errors be in scale as the scale of the target variable.
Example: Let's consider target variable 'revenue' has its unit in 'dollars', then RMSE will have its unit in 'dollars'.
The Square term in RMSE prevents canceling the positive and negative error values.
As RMSE is highly affected by outlier values, it is mandatory to handle outliers from the data before using this metric. Lower the value better is the performance of the model.

**Root Mean Squared Logarithmic Error(RMSLE):**
RMSLE is similar to RMSE but where the error term is calculated at a logarithmic scale.
In the case of RMSE, the presence of outliers increases the error term to a very large value. But, in the case of RMLSE, the outliers are drastically scaled-down. When we don't want to influence results, if there are large errors then RMSLE can be taken into consideration.
IMG4.png
Here we are adding 1 as a constant to both actual and predicted values because if the logarithmic term is 0 then it reaches infinitely large. \

Predicted value - SMALL & Actual value - SMALL : RMSE and RMSLE are same
Either Predicted value or Actual value - LARGE : RMSE > RMSLE
Predicted value - LARGE & Actual value - LARGE : RMSE > RMSLE

**In this dataset, actual and predicted values are large. Hence we can consider RMSE as an evaluation metric.**
