# Cabestan_research_project


A Study of four financial time series.

Introduction :

We are given four assets : A,B,C and D and will attempt to predict the closing prices of these assets using ARIMA and VAR models. We fit ARIMA and VAR models at first for just the data coming from each asset, we will then run the combined data through the models after employing a dimensionality reduction to obtain slightly better scores. In all cases, our models are tested using a rolling forecast test, which is a form of Cross Validation for time series data. The final results can be summarized in the following tables.


    ARIMA	    VAR	    Naive	 VAR Combined	 VAR + PCA
A	0.997083	0.996208	 1.0	     0.994839	     0.998305
B	0.994859	0.991335	 1.0	     0.992670	     0.992507
C	1.009271	1.008781	 1.0	     1.011703	     1.015820
D	0.999472	1.006387	 1.0	     0.995893	     0.996674


The MASE score measures how effective the model is against the naive model that predicts tomorrows price as today's price. In the case of assets A,B and D we find that our models perform slightly better than the naive prediction. In the case of asset C, the naive model is best. It is very possible that the models will outperform the naive model if we were to forecast not just one days ahead but several days ahead. Rough results which we don't present here suggest this to be true.


   ARIMA	    VAR	     Naive	  VAR Combined	  VAR + PCA
A	0.153396	0.153176	0.153164	  0.157962	     0.159229
B	2.287908	2.279414	2.303413	  2.139894	     2.145245
C	0.005341	0.005357	0.005339	  0.005382	     0.005434
D	5.748741	5.740671	5.679302	  5.703751	     5.699656

We can also test our models using the mean squared error. We see above for instance that a VAR model for the combined data of all assets to predict asset B outperforms the naive model. However, the naive model beats the other methods in all other cases.

In every instance of fitting the model, we have tuned the parameters involved using AIC/BIC scores as well as a rolling forecast test.
