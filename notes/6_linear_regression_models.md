# [Simple Linear Regression Models](https://www.cse.wustl.edu/~jain/cse567-17/k_14slr.htm)

* Regression model: 
	- Predict a response for a given set of predictor variables.
	- Estimated value is called response variable.
	- The variables used to predict the response are called predictor variables.
	- When the estimated values is a linear function of predictors we call it linear regression.
	- **Simple** linear regression has only a single predictor.
	- Minimize the error in the model.
* Good model:
	- Regression models attempt to minmize the distance between the observations and the model line, in other words we try to minmize the error.
	- Choose a line that minmizes the sum of the squares of the errors
	- yhat = b\_0 + b\_1 * x. yhat is the predicted response, x is the predictor. b\_0 and b\_1 are fixed parameters.
	- The error is thus: e\_i = y\_i - yhat\_i.
	- Sum of the square errors (SSE).
	- We can estimate b\_0 and b\_1 through some functions. See example 14.1.
	- b\_1 and b\_0 is reached by d(SSE)/db\_1 and d(SSE)/db\_0.
* Allocation of variation
	- The higher R is the better the regression.
	- We can find this by calculating the following:
		1. Total sum of squares (SST). Measurement of y's variability and is called variation of y.
		2. SSR = SST - SSE
		3. SST = SSR + SSE
		4. R^2 = SSR/SST
	- R^2 = 1 -> Perfect fit
	- R^2 = 0 -> No fit
* Since the errors are obtained after calculating two regression parameters the errors have n-2 degrees of freedom.
	- SSE/(n-2) is called the mean squared error (MSE).
	- Standard deviation of errors = SQRT(MSE)
* Confidence intervals for regression parameters
	- Regression parameters b\_0 and b\_1 are estimates from a single sample of size n, hence they are random.
	- This means that there are true parameters of the population, beta\_0 and beta\_1. Thus b\_0 and b\_1 are just estimates.
	- Hence,we can calculate the confidence interval for b\_0 and b\_1 just how we have done it before.

