
# Perdict San Francisco AirBnB Prices

There is a startup company with a similar business model as Airbnb. The startup is in the San Franciso area, where the company runs its feasibility test.
The company asked me to create a model to predict the prices based on the Airbnb dataset they acquired. The dataset is limited, which does create possible problems. 

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
![Screen Shot 2022-08-01 at 9 21 28 PM](https://user-images.githubusercontent.com/104875604/182279182-f8ff5d44-ef38-4eec-9c8f-5e0d190eef0d.png)
-Dropping any price over $2,000 per night helped with the significant outliers, which helped with the model's performance. 

## Model Performance
The best model out of Random Forest Regressor and Linear Regression was Linear Regression with the score below: 
![Screen Shot 2022-08-01 at 9 39 49 PM](https://user-images.githubusercontent.com/104875604/182280048-0bc70876-273e-4cbe-af84-9b813b8f5dc8.png)


