## Use Foursquare Data to Enhance Property Valuation Models

### Introduction

Property valuation models are used to estimate the market value of a property based on its characteristics, sales history and market information. Such models are widely used in different fields. For example, municipal governments use the models to estimate the property tax base, banks and insurance companies use the models to determine the risks associated with mortgage loans, and individual home buyers and sellers or real estate agents use the models to decide on the price they set or offer on a property.

One of the most popular types of property valuation models is the hedonic model, which estimates the market value of a property based on the characteristics of the home and its environment. Typically, the models are specified as a regression model, where the dependent variable is the market value of the home, while the independent variables normally include age, floor area size, lot size, dwelling type (such as single-detached, semi-detached, or apartment), number of floors, bedrooms and bathrooms, etc.

The value of a home is influenced not only by its internal characteristics, but also by characteristics of the neighbourhood it is in. Neighbourhood amenities, such as parks, schools, shopping and dinning, often have a direct impact on house prices. While internal characteristics are often easier to measure and collect, data on the external amenities are much difficult to gather. The lacking of such data often leads to less-than-optimal property valuation models.

### Data

For this project, we will utilize property sales and characteristics data, published by the Province of Nova Scotia, Canada as open data, to create a base hedonic model. Neighbourhood amenities, retrieved using the Foursquare API, are then added to the model to assess the impact of adding neighbourhood amenity data on the accuracy of property valuation models.

Property sales and characteristics data from Nova Scotia are provided in three tables: Parcel land sizes, residential dwelling characteristics, and parcel sales history. The parcel land size table contains the lot size of each property measured in acres and square feet. The residential dwelling characteristics table contains information on each property including the year the property was built, square footage (i.e. floor area size), number of storeys, bedrooms and bathrooms, availability of garage and finished basement, and construction quality of the property. The parcel sales history table contains the sales dates and prices of each property. The tables are cross-referenced by the assessment account number, and contain property addresses and map coordinates as well.

Neighbourhood amenities data from Foursquare are retrieved using the Foursquare API, and contain venue name, location, category (for example park or restaurant), description, price and rating. 

For this project, we will select around 900 properties from the Halifax metropolitan area, and for each property, retrieve the nearest amenities from Foursquare. The two datasets are then joined together to produce a final dataset which will be used to create two hedonic models (with and without neighbourhood amenities). Results are then compared to identify the impact of using neighbourhood amenities in the model.

### Acknowledgments

This project uses information licensed under the Open Data & Information Government License – PVSC & Participating Municipalities. This project uses locational data provided by Foursquare.


