# Cabestan_research_project


A Study of four financial time series.

Introduction :

We are given four assets : A,B,C and D and will attempt to predict the closing
prices of these assets using ARIMA and VAR models. We fit ARIMA and VAR models at first 
for just the data coming from each asset, we will then run the combined data through the 
models after employing a dimensionality reduction to obtain slightly better scores. In all 
cases, our models are tested using a rolling forecast test, which is a form of Cross Validation
for time series data. The final results can be summarized in the tables in the notebook. 


The MASE score measures how effective the model is against the naive model that predicts tomorrows price as today's price. In the case of assets A,B and D we find that our models perform slightly better than the naive prediction. In the case of asset C, the naive model is best. It is very possible that the models will outperform the naive model if we were to forecast not just one days ahead but several days ahead. Rough results which we don't present here suggest this to be true.


We can also test our models using the mean squared error. We see above for instance that a VAR model for the combined data of all assets to predict asset B outperforms the naive model. However, the naive model beats the other methods in all other cases.

In every instance of fitting the model, we have tuned the parameters involved using AIC/BIC scores as well as a rolling forecast test.
