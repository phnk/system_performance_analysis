# [2^k r Factorial Designs](https://www.cse.wustl.edu/~jain/cse567-17/k_172kd.htm)
* If you do the same experiment r times, what is the effect?
* r replications of 2^k experiments > 2^k*r obervations -> Allows for estimation of experimental error (e)
* Experimental error = Measured value - Estimated value. The error should sum to 0.
* Example:
	- From the effects, estimated response, measured response and errors table:
	- Calculate estimated response
	- Calculate experimental errors
	- Calculate allocation of variation (SST)
* What is the advatance of replication?
	- We get the variability
	- We can calculate confidence intervals for effects
* Contrast: Linear combination with sum cofficients = 0. In other words: If our coefficients add up to zero we will call it a contrast.
* What is contrast? Why do we use it?
* We can calculate the confidence interval for our predictions also since we have replication.
* We are repeating what we did in regression. We have a set of assumptions:
	1. Errors are statistically indepdent
	2. Errors are additive
	3. Errors are normally distributed
	4. Errors have a constant standard deviation
	5. Effects of factors are additive (observations are independent and normally distributed with constant variance)
* To see if these are true we do visual tests like we did in regression
* Above has been additive models. But these are not always valid, for example, if the effects do not add. E.g execution time of workloads.
* We can however achieve an addatitive model by using substitution. For example, if our execution time is calculated by y = w/v this can, with log rules, become log(y) = log(w) - log(v). We can then substitute logs to get an additive model where the output is a log.
* After you have log(y) = some value we can just raise it to log and get the real y.
* Transformations considerations:
	- Go from multiplicative to additive
	- See: Box-cox family of transformations
	- Knowledge about the system behaviour should always take precedence over statistical considerations.
* Visual tests for 2^kr designs
	- Scatter plot of errors versus predicted resoponses should not have any trend
	- The Normal qunatile-quantile plot of errors should be linear
	- Spread of y valuyes in all experiments should be comparable
* Importance vs significance
	- Importance = parameters or models that explain a high percent of variation
	- Significant = Parameters or models whose confidence interval does not include zero
	- We want to have both these properties. If we only have importance, run more experiments. If we only have significance, ignore the parameter and see if the model is still significant.

