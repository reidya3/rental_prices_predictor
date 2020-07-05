# Rental Prices In Dublin
## Project Overview
- Created a tool that estimates rental prices in Dublin(MAE- €302.68) to help prospective renters negotiate their rental price when applying to rent a property.
- Scraped over 2,500 property descriptions from rent.ie using beautiful soup and selenium.
- Performed in-depth EDA.
- Engineered features using google maps/places  API such as the distance to the city centre and the average rating of restaurants in an area to quantify an area's exclusivity.
- Engineered additional features from the text of each property description
- Optimized Linear, Lasso, Random forest, and Gradient Boosted Regressors using gridsearhCV to reach the best model.

## Table of contents
1. [Background](#background)
2. [Data Collection](#collect)
    1. [Web Scraping](#subparagraph1)
    2. [Engineering Features](#subparagraph2)
3. [EDA](#eda)



## Background <a name="background"></a>
I wanted to understand rental price behaviour in Dublin against various features such as location and the size of the property. My goal was to create a model that predicted the rental price based on such attributes so that I could make a more informed decision, when I try to enter the rental market next year. Rent.ie is Ireland's newest and freshest lettings website offering renters an alternative to the Daft lettings section when looking for rental accommodation and flatshares. They are focused on 18-25 year olds and aim to be the top renting website for this demographic.

## Data Collection <a name="collect"></a>
The data collection notebook can be found [here](notebooks/Data_collection.ipynb)

### 1. Web Scraping <a name="subparagraph1"></a>
 I created a scraper tool to scrape over 2,500 property descriptions from rent.ie using python and selenium. With each property, we got the following:
- Listed property price(€)
- Address
- Number of bedrooms
- Number of bathroom
- Property description
- if the rental price is listed per month
- if the rental price is listed per week
- if the property is furnished or not

### 2. Engineering Features <a name="subparagraph2"></a>
Does the location of a property matter that much when renting a house? Many people in dublin would agree, as driving cars is impractical due to the huge volumes of traffic coming into the city, public transport is not very affordable and biking under windy rain just sucks! Here, I pick three locations O'connel bridge, IFSC and 'silicon docks'. After this, I find the distance between the loaction of the each property and the revelant point.

How do we measure the effect of trendiness or popularity in a qauntitative way? Popular areas tend to have bettter amenties such as resturant's. I choose google places API to get an average review rating of resturants nearby(1.5km radius) and an average price level. Again, details of how I did this can be found in the notebook above.

In addition, I engineered other features from the text of each property description such as the postcode. This can be found in the [rent EDA notebook.](notebooks/rent_EDA.ipynb)

Data cleaning also took place. Details of which can be found in the two aforementioned notebooks.

## EDA
I discovered a number of cool insights. Detailed examination of these can be found [EDA notebook.](notebooks/rent_EDA.ipynb)

### Examples:

##### Rental Price Heatmap Of Dublin
<img src="data/dublin_heat_map.png" alt="drawing" width="600"/>

#### Correlation matrix
<img src="data/correlation.png" alt="drawing" />

#### Histograms Of Rental Prices listed per month or per week
<img src="data/histogram_house_type.png" alt="drawing"/>

#### Wordcloud of property descriptions
<img src="data/WordCloud.png" alt="drawing" width="400" />








 


