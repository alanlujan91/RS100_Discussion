This repository provides an analysis of the trend in forecast errors made by the Tealbook/Greenbook(GB) and the Survey of Professional Forecasters(SPF) for measures of the unemployment rate and real growth in personal consumption expenditures from 1982 to 2017. Below is a brief description of the main data and code used to produce the main results of this exercise.

The data on forecasts for unemployment and consumption made by the [federal reserve (Tealbook/Greenbook)](https://www.philadelphiafed.org/surveys-and-data/real-time-data-research/philadelphia-data-set) and the [mean across private forcasters](https://www.philadelphiafed.org/surveys-and-data/real-time-data-research/mean-forecasts) are provided by the Philidelphia Fed. Data on [realized values of the forecasted variables](https://fred.stlouisfed.org/) are provided by the St. Louis Fed. The subfolder "data" contains the raw and cleaned versions of each of these datasets.

The subfolder "code/main" performs the "main" tasks of this exercise using the cleaned data. First, the data are used to compute annual forecasts for the unemployment rate and real growth in personal consumption expenditures by comparing forecasts in a given period versus forecast for up to four quarters ahead (depending on whether the measured variable is a *level* or *growth rate*). The same is done for the observed variables over the same horizon. From there, the absolute value of the difference between these annual and observed forecasts are computed. Lastly, standard statistical techniques are used to analyze the trend in these GB and SPF absolute forecast errors. 

The code file "reproduce.py" can be accessed to see the order in which these programs were run to produce the results. The code "rerproduce.sh" will allow the user to reproduce the results from the terminal.
