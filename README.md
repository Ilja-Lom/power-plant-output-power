# power-plant-output-power
This project aims at predicting the output power of a power station by utilising linear regression.

# Introduction to the data

This is a project based on the following dataset:
https://archive.ics.uci.edu/ml/datasets/combined+cycle+power+plant

The data comes from a Combined Cycle Power Plant, which utilises a combination of gas and steam turbines, and a heat recovery steam generator.

The data comes from a period of hourly 2006-2011 measurements when the power plant was at full load.

The data includes:

1.) Ambient Temperature (AT) in degrees Celsius.

2.) Ambient Pressure (AP) in milibar.

3.) Relative Humidity (RH) in %.

4.) Exhaust Vacuum (V) in cm/Hg.

5.) New hourly power output (PE) in MegaWatts.

# Purpose of analysis

The purpose of this analysis is to identify whether the power output (PE) is correlated to the other variables as predictor variables, and whether we can predict the power output using T, AP, RH, and V.

# Conclusions

There is a linear relationship between the predictor parameters, and the power output outcome variable. The linear regression model therefore achieves an R2-score of 93%, indicating a strong ability of the predictor variables to predict the output power of the power station.

As displayed in the 'actual value' Vs. 'residual' scatterplot, there is a fairly even distribution of residuals; indicating that this linear models fulfills one of the assumptions of linear regression, which is homoscedasticity.

Another assumption of linear regression is that the recording are independent of each other (no auto-correlation). This is true due to the nature of the data.

Multicollinearity - where two or more independent variables are highly correlated (gradient ~ 1.00). Using the scatter_matrix command for plotly express, this assumption is not broken.

# What have I learnt during this project?

1.) Testing for multicollinearity in Python. This was achieved using the scatter_matrix plot with plotly express.

2.) Checking the distribution of residuals in Python. I achieved this by creating a dataframe that stores the actual values, and the residual value. This was then plotted using plotly express with an Ordinary Least Squares trendline.



