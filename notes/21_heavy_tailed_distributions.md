# [Introduction to Heavy-Tailed Distributions, Self-Similar Processes, and Long-Range Dependence](https://www.cse.wustl.edu/~jain/cse567-17/k_38lrd.htm)
* What is heavy-tailed distributions?
	- HTDs are distributions whose tail is not exponetionally bounded.
	- Most real world phenomenon follows a heavy tailed distribution.
	- Example: Distribution of wealth, file sizes, CPU times of jobs, etc.
	- An example of a heavy-tailed distribution is the Weibull distribution.
* Power Law Distriubtions
	- Is a subset of heavy tailed distributions, such that all power law distributions are heavy tailed but no all heavy tailed distributions are power law.
	- Example of power law distribution is Pareto distribution.
* Effect of Heavy tail
	- Many outliers
	- Sampling from this will result in mostly small values with few large values.
	- Sample statistics, such as mean, may have a large variance meaning we need many samples for meaningful confidence.
	- Sample mean is generally under-estimated compared to the population mean.
	- Simulations of heavy-tailed input will require long runtime to reach a steady state and even then the variance can be large.
	- Need many observations to reach a high digit accuracy.
	- For example: In some situations we would need 10^101 observation for a single decimal digit accuracy.
	- Central limit theorem applies only to observations from distributions with finite variances.
* Some heavy-tail examples:
	- M/PT/1 queue
	- PT/M/1 queue
* Heavy-tailness also imples predictability.
* How to check for the heavy tail?
	- Make a Q-Q like plot on a log-log graph assuming a Pareto distribution.
	- Find alpha from the splot of the best-fit line.
	- Good fit = High R^2 = Power law
* How do we KNOW that our distribution is?
	- The lower the alpha, the heavier the tail is.
* Self-similarity
	- When zoomed, the sub objects have the same shape as the original object.
	- Also called fractals.
* Self-similar proces
	- Scaling in time = scaling in magnitude.
	- Statstical similarity -> Similar distributions with similar mean and variance.
	- Similar variance -> self-similar in the second order
	- Similar higher order moments -> self-similarity of higher oders
	- All moments similar -> Strictly self-similar.
* Short range dependence (SRD)
	- A process is said to be short-range dependent if the dependence of observation diminishes fast.
	- Another way: Sum of autocorrelation function is finite.
* Long range depdence (LRD)
	- A process is said to be long-range dependent if the dependence of observation decays more slowly than exponential decay.
	- Another way: Sum of autocorrelation function is infinite.
* Example of processes with LRD
	- Aggregation of a large number on-off process with heavy-tailed on-times or heavy-tailed off times results in long-range dependence.
	- Internet traffic
	- Resource demands
	- Congestion and feedback.
* Effects of Long range dependence
	- Long range dependences invalidates all esults for queueing theory obtained using Poisson processes, the buffer sizes required to avoid overflow can be off by thuasands.
* Self-similarity vs. LRD
	- Not equal
	- Self-similar can be either SRD or LRD.
* If we want to analyse the LRD we need to generate a LRD sequence.
* From observations we can generate the hurst exponent for LRD analysis..


