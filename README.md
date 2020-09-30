# Evaluating Home Price Trends for Buyers in King County

The process of purchasing a new home is one that takes a considerable amount of diligence. Most purchasers set out to buy a home as a way of creating a permanent residence for them and their families. As a result, buyers go through several visits and deliberations before finally being able to settle in on the home they will live in for the rest of their lives. The focus of this project is based on housing sale data based in King County, WA. In order to help first time home buyers, I set out to answer several questions in order to help buyers. In addition, I created a linear regression model in order to help determine what are the key factors in determining a house's price.

# Data Setup and Column Descriptions:

The dataset used in this project consists of house sale data from May 2014 to May 2015 from King County, WA. It contains over 20,000 separate house sales that were made over this period of time. The data set can be found at the following link: https://www.kaggle.com/harlfoxem/housesalesprediction

The dataset was presented as a csv file. Certain aspects of the data needed to be cleaned before I could analyze it any further. The following columns descriptions were used for my analysis.

## Column Names and Descriptions for Kings County Data Set
* **id** - unique identified for a house
* **dateDate** - house was sold
* **pricePrice** -  is prediction target
* **bedroomsNumber** -  of Bedrooms/House
* **bathroomsNumber** -  of bathrooms/bedrooms
* **sqft_livingsquare** -  footage of the home
* **sqft_lotsquare** -  footage of the lot
* **floorsTotal** -  floors (levels) in house
* **waterfront** - House which has a view to a waterfront
* **view** - Has been viewed
* **condition** - How good the condition is ( Overall )
* **grade** - overall grade given to the housing unit, based on King County grading system
* **sqft_above** - square footage of house apart from basement
* **sqft_basement** - square footage of the basement
* **yr_built** - Built Year
* **yr_renovated** - Year when house was renovated
* **zipcode** - zip
* **lat** - Latitude coordinate
* **long** - Longitude coordinate
* **sqft_living15** - The square footage of interior housing living space for the nearest 15 neighbors
* **sqft_lot15** - The square footage of the land lots of the nearest 15 neighbors

# Questions Answered:

For my analysis, I decided to focus on various features of the homes in King County. I wanted to take a look at some of the historical house design trends I could find. These trends should, in theory, reflect the market at the time and be a reflection of what homeowners are currently desiring. Being able to indicate historical trends will allow us to predict the current market and which features are highly desirable to home buyers.The following questions were answered in this project: 

* How has the average size of a house changed over the years? How does a home's age affect its price?

* How has an average home's yard space changed over the years? How much does a house’s yard space affect its price?

* How have a home’s bedroom/bathroom ratio changed over the years? What effect does this ratio have on a home's price?


# Question 1: House Size and Home Price Trends

I wanted to observe how the average size of a home had changed over time. The dataset we were given goes back to the early 1900s and goes up to current times. I wanted to see if we could notice any changes in the way houses were being designed. I plotted the average living space square footage over the year a house was built for all houses. In addition, I wanted to see whether there are any notable price trends when comparing modern and historical homes.

![Living Space Over Time](/images/LivingSpace_Over_Time.png)

![House Prices Over Time](/images/HousePrices_Over_Time.png)

There is a clear trend in houses becoming larger on average. After the 1940s, homes were being designed to be bigger with the highest peak so far being observed in the early 2000s.

House prices on the other hand fluctuated greatly. While there has been some degree of increase in home prices, it is not as significant when compared to the living space increase. It is also interesting to note that the highest peaks were for pre-war homes as well as some modern homes. This indicates how pre-war homes are revered for their novelty and historical aspects in spite of the generally smaller sizes.

# Question 2: Yard Area

Another aspect of a home that I wanted to evaluate was the impact of having an actual yard. Having a large yard can be desirable for certain home buyers who are looking to extend their homes as well as provide space for entertainment. I plotted the square footage of a home compared to its price as well as the average square footage of a yard compared to when a home was built.

![YardSqft_and_Price](/images/YardSqft_and_Price.png)

![YardSqft_Over_Time](/images/YardSqft_Over_Time.png)

I observed that there was a positive correlation between a yard's square footage and the overall price. A large yard, however, was not indicative of an costly house because the most expensive homes had hardly any or none at all.

The average yard square footage for a home has gone down in recent years. Early homes enjoyed much more luxury when it came to space and zoning, something that is not prevalent in current times. It explains why developers are forced into building vertically.

# Question 3: Bedroom / Bathroom Ratio

Another aspect of home design that I wanted to see whether it had changed is the ratio of bedrooms to bathrooms. As the average family size has generally gotten smaller over the years, one would think that home designers would build homes to better accommodate a smaller tight knit family. One such accommodation would be to make sure that there were enough bathrooms for the members of the family to live comfortably. I wanted to take a closer look to see how homes have changed to adapt to family needs.

![BedBathRatio_Over_Time](/images/BedBathRatio_Over_Time.png)

![BedBathRatio_Price](/images/BedBathRatio_Price.png)

For this purpose, having a lower bedroom/bathroom ratio is highly desirable as it allows for more family members to be accommodated at once. There is a clear decrease in this ratio after the 1960s. This can be attributed to smaller family sizes as well as larger homes being able to fit more rooms. There is also a general increase in price associated with lower ratios.

# Modeling Home Prices:

Creating a linear regression model for the home prices went through a number of iterative processes. Multiple models were tried out and iterated upon to find out the best model for measuring home prices. Ultimately, the final model that was settled on produced a R-Squared value of 0.712, meaning that the model explains roughly 71% of the variability of the house prices around its mean.

# Future Studies:

In addition to the questions above, there are number of questions that came to my mind in the process of designing this project. There are many more questions home buyers have before finally closing a deal on a house. I wanted to evaluate the following questions for future studying.

* **What effect does crime and safety in a neighborhood have on a home’s price?**

Homeowners all want to live in the safest neighborhood possible. Using crime data from the King County website, I wanted to see which zipcodes and cities had the least amount of crime and see whether that corresponds to higher house prices.

* **What other home features and designs have an impact on a house’s price?**

Bedrooms and bathrooms are important when picking out a house but so are a number of other features that were not included in this dataset. Garages, sheds, as well as other luxurious features like pools/hot tubs are also desirable when evaluating a house.

* **How does proximity to public amenities affect a home’s price?**

Having easy access to amenities like parks, popular restaurants, and public transportation are all desirable features when evaluating a neighborhood. I want to observe whether living close to such attractions corresponds to high home prices.

Link to Medium blog for this project: https://medium.com/@msf894/flatiron-school-project-2-king-county-housing-dataset-d123dc9b6b3f
