# Identifying High-Potential Real Estate Inventment Opportunities:
![Real estate image](https://github.com/dukebaya/Real-Estate-ForecastingTime-Series/raw/main/images/Real%20estate%20image.jpg)

Apex Assets Investment is an investment firm that buys and sells real estate in the USA and is facing challenges as to how they should make their investments. They have consulted us to provide guidance this issue to ease their process.
We have used data from .[Zillow Research](https://www.zillow.com/research/data/). to achieve this objective. Zillow Research publishes top-tier Zillow Home Value Index (ZHVI): A measure of the typical home value and market changes across a given region and housing type.  It reflects the typical value for homes in the 35th to 65th percentile range.We have cleaned the data, forward filling of missing values, and anything else that would disturb the research. Time Series Modelling has been used in this notebook to produce future forecast property values based on previous observations, to identify underlying trends/ patterns within the data over time and to detect any signs of seasonality within the data provided. These factors will contribute towards determining how Apex Assets Investment build their portfolio.

# 2. Business Understanding

## 2.1. Overview
Apex Assets Investments is a real estate firm which provides state of art opportunities in the real estate scope such as housing. However, it is grappling with a cahllenge on the beest avenues to do the investing. The primary goal of this project is to 
 to analyse the factors that will determine the best zipcodes to invest in and build and time series model that will forecast the real estate prices of various zipcodes and provides insights and recommendations based on the built time series model in this project. The target stakeholders are executives, product managers, marketing teams, finance and account teams, and contact centre team at Apex Assets Investments. The data used can be accessed from [here](https://www.zillow.com/research/data/).

## 2.2. Business Problem

In today's competitive real estate market,  Apex Assets Investments faces the challenge of finding the best lucrative places to invest. With countless zip codes, fluctuating prices, the pursuit of optimal investment destinations poses a the task that can feel overwhelming. The objective is clear: pinpoint the top 5 zip codes with the highest potential for profit while managing risks wisely.

To tackle this challenge, Apex Assets Investments turns to data and analysis using the time serries model. By studying past trends and using advanced forecasting techniques, they aim to uncover hidden opportunities in different zipcodes. But it's not just about numbers—it's also about understanding communities, local developments, and what makes each area unique. 

With this approach, Apex Assets Investments can make informed decisions that not only benefit their investors but also contribute positively to the neighborhoods they invest in. Ultimately, it's about finding the right balance between growth and stability in the ever-changing world of real estate.


### 3.  The Dataset Understanding and Preparation

The dataset used contains housing information from July 1996 to April 2018 obtained from [here](https://www.zillow.com/research/data/).The dataset has numerous features such as RegionID, RegionName, City, State, CountyName etc. distributed across 14723 rows and 272 columns. Of these 272 columns, 7 of the columns are described below. The remaining 265 columns are records of the given Zip code’s average home value between April, 1996 and April, 2018. The other 7 columns are:

‘RegionID’- Each record contained a unique ID number. *’RegionName’-This is the column that provides the Zip code for the given row. *’City’- The name of the city in which the Zip code is located. *’State’- The name of the State in which the City is located. *’Metro’-The name of the Metro region. *’CountyName’-The name of the County *’SizeRank’- The ranking of the particular Zip code’s size relative to other records in the dataset.

Our project goal was defined by our Business Problem where our stakeholder was only interested in purchasing a home within a zipcode with high Return On Investment.

#### 3.1. Data Preparation
We investigated the data to identify:
- Previewed the dataset.
- Checked the dataset , analytics for missing values, datatypes and summary
- Checked the unique values in the first 7 columns

#### 3.2. Feature Engineering

We did some conversion of the data into the below formats:
- Change the dates to datetime values
- Rename the RegionName to Zipcodes

#### 3.3. EDA

Having cleaned our dataset to only include Zip codes with top 10  prices,.[Images](http://localhost:8888/view/Images/ROIfor10zipcodes.png) we were left with the top 10 zipcodes displayed above. The 10 zipcodes seen here consisted of unique ID Zip codes between them. We were also able to explore the below:
- Summary Statistics
- Top 5 zipcodes with high ROI [images](http://localhost:8888/view/images/Top%20zips%20by%20EDA.jpg)
- Analysis of the top 10 zipcodes Value, ROI,CV [images](http://localhost:8888/view/images/Top%2010.jpg)


## 4. Modeling 
Train Test Split: The script splits the time series data into training and testing sets, ensuring 80% of historical data is allocated for training to train the model effectively while keeping 20% for evaluation. The Performance baseline before modeling gives a ROI of 21.39% from 2016 to 2018. This will later be compared to the modeling and prediction results

To find the five zipcode areas that are the most optimal for real estate investment ,
 We ran an Auto Arima time series models on every all the zipcode areas of concern individually by means of functions . 

We used this model due to the nature of data and it various advantages such as the ability automatically selects the optimal values for the p, d, and q parameters, as well as seasonal parameters (P, D, Q, m) if applicable. This removes the need for manual parameter tuning, saving time and effort.

[images](http://localhost:8888/view/images/Model%20Accuracy.jpg)

## 5. Evaluation
The script evaluates the accuracy of the trained models by comparing their predictions on the testing set with actual values, providing insights into the performance of the models in predicting future trends. On average the model's predictions were roughly 8.2% off from the actual values from our test set. The model is giving a lower ROI. Since we have a low margin of error we are comfortable to proceed with the mordeling.
## 6. Conclusion 

In our investigation to assess the effectiveness of our models, we uncovered compelling evidence suggesting their efficacy. By employing an exploratory data analysis (EDA) approach on our training dataset to identify five cities for investment and subsequently simulating investments in those selected cities on our test dataset, we realized a notable 21.39% return on investment. Comparatively, when leveraging modeling techniques to predict the optimal five cities for investment within New York over the duration of our test dataset, we attained a respectable 17.27% return on investment. This analysis underscores the value of our models' recommendations, indicating that even if their predictive accuracy is not exceptionally high, their insights remain valuable..


## 7. Recommendations

These are the top 5 zipcodes by ROI one year out, as predicted by our models, and serve as our final recommendations.
[images](http://localhost:8888/view/images/Final%20predictions.jpg)
Aspen
Bridgehampton
Amagansett
Brookline
Cambridge

 
 ## For More Information
 For more info please review our full analysis in: [notebook](http://localhost:8888/notebooks/Phase4_Group_13%20(4).ipynb) and [slides](http://localhost:8888/files/Apex%20Assets%20Investments%20Presentation.pdf)


## Authors
1. Caroline Njoroge
2. Miriam Ongare
3. Mercy Ronoh
4. Philip Mweri
5. Chepkemoi Chepkemoi
