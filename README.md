# Identifying High-Potential Real Estate Inventment Opportunities: A Case Study of Apex Assets Investments

#  1. Abstract 

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
.[Images](http://localhost:8888/view/Images/ROItrend.png)

#### 3.3. EDA

Having cleaned our dataset to only include Zip codes with top 10  prices,.[Images](http://localhost:8888/view/Images/ROIfor10zipcodes.png) we were left with the top 10 zipcodes displayed above. The 10 zipcodes seen here consisted of unique ID Zip codes between them. We were also able to explore the below:
- Summary Statistics
- Top 10 zipcodes with high ROI .[Images](http://localhost:8888/view/Images/roivscvfor10.png)
- Analysis of the top 10 zipcodes Value, ROI,CV
- Plotting monthly returns with their respective rolling mean and rolling std for each of the top 10 zip codes.[Images](http://localhost:8888/view/Images/Rollingmean16038.png)

## 4. Modeling 







## 5. Evaluation




## 6. Conclusion 





## 7. Recommendations


 
 ## For More Information
 For more info please review our full analysis in: [notebook]() and [slides]()


## Authors
1. Caroline Njoroge
2. Miriam Ongare
3. Mercy Ronoh
4. Philip Mweri
5. Chepkemoi Chepkemoi