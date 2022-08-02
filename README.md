
# Perdict San Francisco AirBnB Prices

There is a startup company with a similar business model as Airbnb. The startup is in the San Franciso area, where the company runs its feasibility test.
The company asked me to create a model to predict the prices based on the Airbnb dataset they acquired. The dataset is limited, which does create possible problems. 

### About Airbnb : Airbnb is a community-based online platform for listing and renting local homes. It connects hosts and travelers and facilitates the process of renting without owning any rooms itself. Moreover it cultivates a sharing-economy by allowing property owners to rent out private flats


## Features

- Longitude and Lattitude 
- Room Type 
- Property Type
- Bathrooms
- Bedrooms
- Minimum Nights 

## Map of San Francisco by Room Type

![Screen Shot 2022-08-01 at 8 52 41 PM](https://user-images.githubusercontent.com/104875604/182275678-8e160fd8-203c-4268-8631-8a8f1f1ec4d0.png)

## Models Used For Predictions
- Random Forest Regressor
- Linear Regression
- Kmeans 
    - Used Kmeans to group the locations before modeling,which slightly improve the model. Here is a map of the Clustering![image](https://user-images.githubusercontent.com/104875604/182276896-aba244fa-2cb7-437c-81b9-d75954f2c68e.png)

## Key Findings 
![Screen Shot 2022-08-01 at 9 21 39 PM](https://user-images.githubusercontent.com/104875604/182277876-59e0a7e9-89a1-4937-acd1-134a7ff62145.png)

- There are significant outliers in the pricing data.

It is bad practice to drop outliers if these observations are legitimate, but I don't believe some of these outliers are legitimate. 
If these outliers are legitimate, the dataset doesn't contain the features to explain the significant price increase.
Since I do not have the features to explain the price increase, any price over $2,000 is executed from the model.
![Screen Shot 2022-08-01 at 10 33 19 PM](https://user-images.githubusercontent.com/104875604/182286222-fd779a98-7ebf-495a-ad0d-87adbbc8009e.png)

- Dropping any price over $2,000 per night helped with the significant outliers, which helped with the model's performance. 
- Dropping the six-bedroom also improved the model. There were only a couple sex-bedrooms, but they influence to average price. 

## Model Performance
The best model out of Random Forest Regressor and Linear Regression was Linear Regression with the score below: 
![Screen Shot 2022-08-01 at 9 39 49 PM](https://user-images.githubusercontent.com/104875604/182280048-0bc70876-273e-4cbe-af84-9b813b8f5dc8.png)

## Looking at the Errors in Predicted Prices
![Screen Shot 2022-08-01 at 9 53 52 PM](https://user-images.githubusercontent.com/104875604/182281946-fb35d429-7f1c-441a-afae-e538c90b3358.png)

The concerns about the prices outliers were warranted. The outliers that stand out are the harmful errors in the predicted price of the two-bedroom shared room. 

The model is under-predicting the prices more than over-predicting. 

## Possible Reasons:
Outliers in Price the model can not explain with features available. 

## Solutions to Improve the Model
1. Drop more outliers, but this is problematic. If there is a reason the price is high, the property's pricing will be incorrect. 

2. Add more features to the dataset to explain the price increase. 

- Square foot of property
- Property's Amenities
- These are two examples of features to add to the model. 

# Recommendation:

Based on the model's poor performance and the need to find features, I do not recommend using the current model due to the likelihood of mispricing the overnight rental. 

Mispricing during the initial go-live phase could be detrimental to the company. 
