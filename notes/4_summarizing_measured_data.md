# Summarizing Measured Data

## Basic Probability and Statisticial concepts 
Started discussing it in part 3. 

***Independent events:*** Two events are called independent if and only if the occurence of one event does not in any way affect the probability of the other event. For example: coin toss. If we perform n number of coin tosses, c2 is not influenced by c1 or c3 or any other cn.

***Random Variable:*** A variable is called a random variable if and only if it takes one of a specified set of values with specified probability. For example: the outcome of a coin toss can be described by the sample space A = {heads, tails}. We can then introduce a random variable Y that models a $1 payoff for a successful bet as follows Y(w) = 1 if heads, else 0. In this case Y is the random variable. ***Poor explanation I would say***.

### Distribution functions (why are these used?)
* Cumulative Distribution Function (CDF): Starts at 0, ends at 1. Fx(a) = P(x <= a).
* Probability Density Function (derivative of F) (PDF): Starts at 0, ends at 0. f(x) = dF(x)/dx.
	- Why do we do this? Whats the point of getting f and using f?
* Probability mass function (PMF): f(xi) = pi
	- This is a function that gives the probability that a discrete random variable is exactly equal to some value. For example: If we have some sample space A = {1, 3, 7}, then the probability mass function COULD be (depends on probability defs of course) fY(y) = {0.2, 0.5, 0.3}. Sum(fY) should be 1.

### Mean (Expected Value), Variance, CoV
* Mean (which in this case is the same as Expected Value): Is the long-run average value of random variables. EV = Sum(P(xi) * Xi where EV is the expected value, P is the probability of the event and Xi is the event.
* Variance: is the expectation of the squared deviation of a random variable from its sample mean. Var(X) = E[X^2] - E[X]^2. Variance is a measurement of the spread between numbers in a data set.
* Coefficient of Variation: C.O.V = (Standard Deviation) / (Mean). Ratio of the standard deviation to the mean. 

### Covariance and Correlation
* Covariance: Measures how much two random variables vary together. Similar to variance, but variance only tells you how one varies whereas covariance tells you how much two variables vary together. cov(X, Y) = E[(X-E[X])(Y-E[Y])]. 
	- For indepedent variables the covariance is zero.
	- The other way is not true. If the cov = 0, they might still be dependent variables.
* Correlation Coefficinet: normalized value of covariance. In range: [-1, 1].
	- corr(X, y) = cov(X, Y) / (sigma x * sigma y)

### Sum of mean and variance
* The expected value can be summed and weighted by: E(a1x1 + .. + akxk) = a1*E(x1) + ... + ak*E(xk)
* ***Only for indepedent variables:*** The variance can be summed and weighted Var(a1x1 + .. + akxk) = a1^2*Var(x1) + .. + ak^2*Var(xk).

### Quantiles, Median and Mode
* Quantiles are cut points dividing the range of a probability distribution is equally big parts. Such as quartiles (four groups) or percentiles (100 groups).
* The median is the 50-percentile or 0.5-quantile of a random variable.
* The mode of x is the xi that has the highest probability pi. For example if we have p = {0.2, 0.5, 0.3} then the mode of x is x2.

### Central limit theorem
Given a population with mean u and standard deviation sigma and a sufficiently large random sample from the population with replacement (we put sample back), then the distribution of the sample means will be approximately normally distributed.

### Normal distribution
A normal distribution is a probability distribution that is symmetric about the mean showing that data near the mean are more frequence in occurence than data far from the mean. The mean from any probability distribution is normally distributed. The normal distribution is denoted as N(u, sigma).

Normal quantize can be used to say something about the mean.

#### Why?
There are two main reasons for the popularity of the normal distribution:
1. The sum of n independent normal variates is a normal variate.
2. The sum of a large number of independent observation from any distribution tends to have a normal distribution (central limit theorem). This is true for observations with finite variance.
	- Experimental errors caused by many factors are normally distributed.

## Summerizing Data by a single number (starts ~22:30 in part 2 lecture 4)
When we do measurement we get 100s of numbers, which no one will pay attention to. We need to be able to take this information and get it into single number form.

Three indices of central tendencies: Mean, Median, Mode.

Sample is whatever measurement we have done. Everytime we measure something, we will get a different sample or set of samples. Hence we get: Sample Mean, Sample Median and Sample Mode.
* Sample Mean: We obtain this by summing all observation and dividing over the number of observations.
* Sample Median: Obtained by sorting the observation and taking the middle observation. If no middle exist (even observations) take the median of the two values in the middle.
* Sample Mode: Plotting histogram and speciying the midpoint of the bucket where the histogram peaks. For categorical variables, the mode is the most common category.
Mean and median always exists, mode might not exist.

*** Cont at 31:30 ***
