# [Introduction to Time Series Analysis](https://www.cse.wustl.edu/~jain/cse567-17/k_37tsa.htm)
* What is a stochastic process?
	- Ordered sequence of random observations 
	- Can be analyised using time series analysis.
* What is a time series?
	- Time series = Stochastic process.
	- Can be plotted as a function of time.
	- Examples: stock price over time, video frames, etc.
* Time series models
* Autoregressive models: predict the variable as a linear regression of the immediate past value.
	- Stationary process: unconditional joint probability distribution does not change when shifted in time.
	- Autocorrelation: the degree of similarity between a time series and a lagged version of itself.
	- White noise: if errors are normal independent and identically distributed with zero mean and variance they would be called white noise sequences.
	- White noise autocorrelations: There is a possibility to have a non-zero variance.
	- AR(p): multiple linear regression.
	- Backward shift operator: B^k*xt = x(t-k).
* Determining the order of AR(p).
	- The highest p is the order of AR(p) model for the series
	- This sequence of last coefficients is also called "Partial Autocorrelation function (PACF)".
* Moving average models: the current value is dependent on the current and past error terms.
* MA(q) models where q is order.
* Autocorrelaations for MA(q) is only non-zero for k =< q.
* Duality of AR(p) vs. MA(q).
	- Determining the coeffficients of AR(p) is straight forward, but determining order p requires an iterative procedure.
	- Determining the order q of MA(q) is straight forward, but determining coefficients require an interative procedure.
	- You choose your pain.
* Non-stationarity: Integrated models
	- Something is changing over time that should not be changing over time.
	- For example: mean, variance, etc.
	- If the change is approximately linear or parabolic, we can model it as white noise (different order equations).
* ARMA and ARIMA models
	- Its possible to combine AR, MA, and I models.
	- And using algebraic manipulations its possible to transform AR models to MA models and vice versa.
* Sometimes non-stationarity is due to seasonality
	- For example: the mean temperature is December is always lower than that in November and in May its always higher than that in March -> Temperature has a yearly season.
	- This example could be modelled as I(12).
* Seasonal ARIMA (SARIMA) models.
* Case study 37.1: Mobile Video.
