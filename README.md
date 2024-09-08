
# Analyzing price of used cars

When analzing and predicting the price of a used car, there are a lot of factors in play. It is known that some cars increase in value as they age while most devalue with age. We're trying to evaluate the various features that affect the price of a used car. 

Looking at the initial dataset available, we see that there are a lot of records with junk for data that skew the data by quite a bit. 


![App Screenshot](/images/Skewed.png)


As are considering used cars and most used cars that sell aren't of the ultra premium kind we're going to limit ourselves to cars under $100,000 and see how the mean price is distributed with the condition of the cars.


![App Screenshot](/images/Unskewed.png)

We can look at various factors of the used car and see how the prices are distributed. Just taking a look at all the models and the mean of their prices we can see brands carry a good resale value and what cars a dealership can consider carrying in stock. We can see that some brands like Land Rover might have a high premium value intially but their value is quite low as a used vehicle. 

![App Screenshot](/images/make_price.png)

If we look at another feature, this time color, we see that initially it doesn't look like it plays a big factor when it comes to the selling price.

![App Screenshot](/images/color-price.png)

The dataset has a lot of columns that aren't in the proper format so they had to be converetd to numerical values as well as covert the categorical columns into numerical using one-hot-encoding process. Some of the columns such as vin number were dropped as they don't provide any value in the value of the car. 
Once the intial dataset was prepped, we were able to see that for any model, the odometer is the most important factor in deciding the price of a used car. 

![App Screenshot](/images/odometer-imp.png)

Odometer has a negative impact on price as we all know. 

![App Screenshot](/images/odo-negaitve.png)

With the value of cars we see a linear trend when considering odometer value but bulding a model with just the odometer results in a very bad accuracy as the Linear regressoin model demostrated with the accuracy of only 19%. 

Running a Multiple Linear Regression model with  yealds a better result with 57% on training data and 55% on test data.

I also ran the Rigde model that yealded 62.5% accuracy on the training data with 59% on the test data. 





