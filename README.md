# Real Estate investment with short term rental
----------

The datasets from AirBnb and Zillow of New York City were analysed to identify Zipcodes where, if property were to be purchased and rented out short term, the time taken to generate profits through rental fees was identified.


## Assumptions

- Occupancy rate of 75%
- Availability of each property for rental is 365 days 
- Maintenance costs (such as cleaning fee) are fixed for each property, and not charged on the customer
- Properties are rented by a customer for a period of 1 week in average
- Rent for a customer in a listing is the same for both weekdays and weekends
- Rent charged for a listing scales linearly with number of customers
- Property tax is not considered when calculating time taken for ROI (break even point)
- Only 2 bedroom properties were selected for this analysis


The datasets can be found  at the [airbnb website](http://insideairbnb.com/get-the-data.html) and [zillow](https://www.zillow.com/research/data/)

## Key Insights from analysing the data
	
1. <b>Neighborhoods in Manhattan</b> offer an ROI with a median of 5.8 years, and containing the greatest number of favorable zip codes 
	- The most common property types that help attain this are Condominiums and Apartments
1. <b>Investing in larger properties</b> can increase revenue, as they can accommodate more guests. 
	- Rental charge (on a per person level) rises until 6 people are accommodated, and stabilizes after that
1. <b>Spreading investments conservatively</b> over Manhattan as well as Brooklyn can test the waters for occupancy rate and ROI projections. 
	- Manhattan is overall more expensive than Brooklyn, however Brooklyn has more Airbnb listings due to its relative affordability.


## Data

As mentioned above, the dataset can be found The datasets can be found  at the [airbnb website](http://insideairbnb.com/get-the-data.html) and [zillow](https://www.zillow.com/research/data/), along with the data dictionary.

## Analysis pipeline

Following the CRISP-DM cycle, the datasets was analyzed in an iterative fashion to build a final data pipeline

![alt_text]()

## Zillow Data set

The Zillow data set from 1996 to 2017, does not contain equal amount of information for all the zip codes present 

![alt_text]()

To address this, data from a time point where all the zip codes had no missing values was taken.

Thus the data was subset to contain information only from 2007-06 to 2017-06

![alt_text]()


## AirBnb Data set

The Airbnb dataset contained a highly skewed distribution of price, which was accounted for removing outliers

![alt_text]()

Properties that could accommodate more people had a steady increase in rent per person, but plateaued after 6 people were accommodated

![alt_text]()

Properties with higher number of amenities listed were fewer, but were more profitable to rent out

![alt_text]()

The property type had a direct impact on revenue generation and maintenance costs as well
Serviced apartments have the largest values for both price as well as cleaning fee

![alt_text]()

For neighborhoods with higher rent, the maintenance costs such as cleaning fee also proportionally increase
Maintenance costs are incurred every time a guest leaves (key assumption) and thus reduce overall profits

![alt_text]()

Neighborhoods that are more expensive  and containing higher number of rental properties could be located

While Manhattan listings are priced more, Brooklyn has a higher number of listings.

![alt_text]()

## Combined analysis

When the Zillow data and Airbnb data were combined, we could identify zip codes with the highest property cost and the highest rent

![alt_text]()

Upon grouping neighborhoods together, while also considering property type, monthly net revenue could be estimated, and ROI calculated

![alt_text]()

Once ROI time for neighborhoods was calculated, we chose the locations where we can attain the highest monthly revenue, with the lowest ROI time, and the property type associated

![alt_text]()

![alt_text]()

# Recommendations

1. <b>Neighborhoods in Manhattan</b> offer an ROI with a median of 5.8 years, and containing the greatest number of favorable zip codes 
	- The most common property types that help attain this are Condominiums and Apartments
1. <b>Investing in larger properties</b> can increase revenue, as they can accommodate more guests. 
	- Rental charge (on a per person level) rises until 6 people are accommodated, and stabilizes after that
1. <b>Spreading investments conservatively</b> over Manhattan as well as Brooklyn can test the waters for occupancy rate and ROI projections. 
	- Manhattan is overall more expensive than Brooklyn, however Brooklyn has more Airbnb listings due to its relative affordability.
 
----------

## References

1. http://insideairbnb.com/new-york-city/
1. http://insideairbnb.com/about.html
1. https://www.mashvisor.com/blog/airbnb-occupancy-rate-2019/
1. https://www.alltherooms.com/analytics/average-airbnb-occupancy-rates-by-city/



## Additional improvements

 - Improving property cost using the Zillow data by either collecting information from publicly available sources, or using time series forecasting to get a more accurate estimate of ROI
 - Validating or readjusting the occupancy rate after observation of property behaviour for 3-4 quarters
 - Estimating influence of applying discount rates
 - Factoring in property taxes to provide a more realistic NPV
 - Incorporating a price-prediction model for predicting estimated cash inflow using more detailed features from a listing.







