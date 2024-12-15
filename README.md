Hello,

This is the README file for my submission to the Module 20.1 Capstone Project assignment. The python jupyter notebook for this assignment can be found here https://github.com/lalbritten01/LAlbri10_UCBerkelyAI/blob/UC_Berkeley-Car-Price_Assignment/Practical_Application_Assignment_11_1_What_Drives_the_Price_of_a_Car_.ipynb

The jupyter python notebook linked above has information from a dataset of internet traffic data and the EDA to understand the dataset and also begin to understand if the internet traffic data follows a pattern that can be accurately forecasted by the Hawkes self exciting point process.

The internet traffic data shows a consistent trend of internet traffic over the 230 days that it covers, with an average of around 4100 visits per day.

In this preliminary EDA I wanted to explore if the Hawkes Process may be a good estimator of internet traffic data as a self exciting point process. In future capstone assignments, I hope to continue to evaluate the Hawkes Process and its ability to 
forecast the internet traffic data studied here. I will evaluate other methods such as simple linear regression and also Exponential Smoothing to contribute to a discussion of just how difficult forecasting the internet traffic data in the study here may be,
however I also believe the Hawkes process is particularly interesting because we can evaluate the quality of forecast predictions in real time as new data rolls in. As with any forecast, we can evaluate accuracy with MAPE and other similar metrics.
However I believe the Hawkes process can be evaluated in more ways than this that may be interesting. First, as the Hawkes Process forecasts are based on an average of a number of runs of simulations, we can assign a p-value to Holdout and Out-of-time (OOT) data both in training
and also potentially in real time if a forecast model is live in production. Second, we can use the Hawkes process associated compensator to further evaluate our confidence in the Hawkes Process forecasts.

In this preliminary analysis, the Hawkes Process shows promise that it may be able to forecast the internet traffic data. After being trained on 30 days of internet traffic data, the Hawkes Process simulation average predicts that internet traffic over the next 10 days will be 33K visits
compared to the 28.7K visits that actually occured over the 10 days following the training data set window. Importantly 25.5% of the simulation predictions are within 10% error of the 28.7K visits that occur in the Holdout data set window. In the next iteration of the Capstone project,
I will further evaluate the Hawkes Process' forecast accuracy on the internet traffic data set, using the compensator and simulation distributions to evaluate forecast prediction confidence in 'real-time' scenarios, and I will also compare the Hawkes Process forecast accuracy to other forecasting methods
such as Linear Regression and Exponential Smoothing to contribute to a dialogue evaluating the difficulties of forecasting the internet traffic data set and modeling techniques that may be suited to forecast traffic event data accurately.
