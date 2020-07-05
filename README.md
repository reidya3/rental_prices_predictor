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
    2. [Engineering features](#subparagraph1)
3. [Another paragraph](#paragraph2)



## Background <a name="background"></a>
I wanted to understand rental price behaviour in Dublin against various features such as location and the size of the property. My goal was to create a model that predicted the rental price based on such attributes so that I could make a more informed decision, when I try to enter the rental market next year. Rent.ie is Ireland's newest and freshest lettings website offering renters an alternative to the Daft lettings section when looking for rental accommodation and flatshares. They are focused on 18-25 year olds and aim to be the top renting website for this demographic.

## Data Collection <a name="collect"></a>
The data collection notebook can be found [here](notebooks/Data_collection.ipynb)

### 1. Web Scraping <a name="subparagraph1"></a>
 I created a scraper tool to scrape over 2,500 property descriptions from rent.ie using python and selenium. With each job, we got the following:
 Listed property price(€)	Address	Bedroom(s)	Bathroom(s)	Property desc	Week YN	Month YN	Furnished Status
- Listed property price(€)
- Address
- Number (s)
- Bathroom(s)
- Property description

Salary Estimate
Job Description
Rating
Company
Location
Company Headquarters
Company Size
Company Founded Date
Type of Ownership
Industry
Sector
Revenue
Competitors
 


