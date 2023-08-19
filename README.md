[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/foXtNvtG)
# Project-ACM40960

# Sales Prediction : A Multivariate Approach

Incorporating ML techniques and ensemble models to enhance sales forecast leading to optimized inventory management and more effective sales strategies.


## 🚀 Motivation
In the rapidly changing business landscape, sales forecasting remains crucial for effective decision-making. It enables businesses to adapt to evolving customer behaviors, optimize resource allocation, manage inventory efficiently, and stay ahead of the competition. Accurate sales predictions are essential for navigating uncertainties and driving sustainable growth in the new world.

Machine learning has become increasingly valuable in sales forecasting due to its ability to analyze large volumes of data and uncover complex patterns. ML models can capture non-linear relationships, seasonal trends, and interactions among various factors to generate more accurate predictions. By incorporating ML techniques such as time series analysis and ensemble models, sales forecasting can be enhanced, leading to optimized inventory management and more effective sales strategies.


## :jigsaw: Architecture
![image](https://github.com/Devansh22201475/Project-ACM40960/assets/134631225/e6deca46-ede5-4422-a7d3-96f363163314)


## Data Understanding
*sales_train*.csv - the training set. Daily historical data from January 2013 to October 2015.

*test*.csv - the test set. You need to forecast the sales for these shops and products for November 2015.

*sample_submission*.csv - a sample submission file in the correct format.

*items*.csv - supplemental information about the items/products.

*item_categories*.csv  - supplemental information about the items categories.

*shops*.csv- supplemental information about the shops.

## Data fields
*ID* - an Id that represents a (Shop, Item) tuple within the test set

*shop_id* - unique identifier of a shop

*item_id* - unique identifier of a product

*item_category_id* - unique identifier of item category

*item_cnt_day* - number of products sold. You are predicting a monthly amount of this measure

*item_price* - current price of an item

*date* - date in format dd/mm/yyyy

*date_block_num* - a consecutive month number, used for convenience. January 2013 is 0, February 2013 is 1,..., October 2015 is 33

*item_name* - name of item

*shop_name* - name of shop

*item_category_name* - name of item category


## :hammer_and_wrench: Installation

Software Requirements:

[![Python 3.7+](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/release/python-360/)

Necessary Installation:

python
pip install xgboost
pip install lightgbm


Necessary Libraries:

python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.model_selection import train_test_split
from xgboost import XGBRegressor, plot_importance
from lightgbm import LGBMRegressor
from sklearn.metrics import mean_squared_error as MSE


## :bar_chart: Exploratory Data Analysis
![plot1](https://github.com/ACM40960/project-Devansh22201475/blob/main/Plots/Graph_1.png?raw=true)
The plot shows the distribution of year wise foot fall across all the stores. It is observed that the busiest year was 2013 and the count has decreased over the years.

![plot2](https://github.com/ACM40960/project-Devansh22201475/blob/main/Plots/Graph_2.png?raw=true)
The plot shows the distribution of month wise foot fall across all the stores. It is observed that the busiest month was January and the least busiest was November. The count fluctuates for the remaining year.

![plot3](https://github.com/ACM40960/project-Devansh22201475/blob/main/Plots/Graph_3.png?raw=true)
The boxplot here describes how the revenue is spread across months. As the y-limit is very large, the box seems like a line which is mostly around 0-5000 Rubel. Also, there are months with very high revenue like in November.

![plot4](https://github.com/ACM40960/project-Devansh22201475/blob/main/Plots/Graph_4.png?raw=true)
To visualize the boxplot better, this distribution plot depicts the revenue share. It is clear that the price of items are widely distributed from 0-5000 Rubel and very few above 20000 Rubel.

![plot5](https://github.com/ACM40960/project-Devansh22201475/blob/main/Plots/Graph_5.png?raw=true)
The plot here depicts the distribution of Top 10 Products over Stores based on the revenue. We observe the different stores revenue for the Top 10 selling products.

## :dart: Model Comaprision
![plot6](https://github.com/ACM40960/project-Devansh22201475/blob/main/Plots/Model_Comparision.png?raw=true)
## :atom: XGBoost Model

XGBoost is a gradient boosting algorithm that is known for its accuracy and speed, making it an ideal choice for demand forecasting tasks.
By using the XGBoost algorithm for demand forecasting, we can leverage the power of advanced machine learning techniques to make accurate predictions about future demand.


## :electron: LightGBM Model
The light gradient boosting machine algorithm – also known as LGBM or LightGBM – is an open-source technique created by Microsoft for machine learning tasks like classification and regression. It is quite similar to XGBoost as it too uses decision trees to classify data.

## :triangular_flag_on_post: Conclusion
![plot6](https://github.com/ACM40960/project-Devansh22201475/blob/main/Plots/Graph_6.png?raw=true)

The trend line plot here describes the sales of items per year. This gives us a clear idea of how the sales trend has changed over year for every month. We could see that the sales needs to be predicted for year 2015 for November (i.e. month 11) and December (i.e. month 12).

We have then used the XGBoost Model and LightGBM model to understand which model best suits the data and provides more accurate results. On success full implementation of both models, we found out that the Root Mean Squared Error i.e. one of the significant indicators of model fit and we observed that the LighGBM model was a better fit as compared to XGBoost model.

## References
▶Sunitha Cheriyan and Shaniba Ibrahim. “Intelligent Sales Prediction Using Machine Learning Techniques” 2018. *2018 International Conference on Computing, Electronics Communications Engineering (iCCECE)*

▶ K. Y. Yuta Kaneko. “A Deep Learning Approach for the Prediction of Retail Store Sales” 2016. *2016 IEEE 16th International Conference on Data Mining Workshops (ICDMW)*

▶ M. K. B. Marko Bohanec. “Explaining machine learning models  in sales predictions” 2017. *Elsevier*. 71. Pages 416–428

▶ B. M. Pavlyshenko. “Machine-Learning Models for Sales Time Series Forecasting” 2019. *2018 IEEE Second International Conference on Data Stream Mining Processing (DSMP), Lviv, Ukraine*

▶ Z. Huo. “Sales Prediction based on Machine Learning” 2021. *2021 2nd International Conference on E-Commerce and Internet Technology (ECIT)*


## Authors

- [@Advayta Zadoo (22201078)](https://www.linkedin.com/in/advayta-zadoo/)
- [@Devansh (22201475)](https://www.linkedin.com/in/devansh-7ab99a8a/)
