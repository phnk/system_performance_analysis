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

To select mean, median, or mode use this flowchart (guideline not a rule):
1. If the data it categorical? -> Use mode
2. If total of interest? -> Use mean
3. Is the distribution skewed? -> Use median
4. Otherwise use mean

Some examples:
* Most used resource in a system: Resources are categorical -> Mode used
* Interarrival time: Total time is of interest (we sum up all the arrival times) -> Mean is the proper choice
* Load on a computer: Highly scewed distribution -> Median
* Average Configuration (CPU, GPU, Memory of machines): Meadian due to skewness of the distribution

Question: How do you know a distribution is skewed? Well, practice will make you be able to "see it" instantly...

### Common misuses of means:
* Using mean with significantly differnt values.
* Mean poor choice if the distribution is skewed. You look if the samples in the distribution they should be close to the mean when calculating the mean. Mean is not always meaningful.
* Multiplying the means -> E(x * y) =/= E(x)E(y). This is only true for indepdendent random varibles.
* Taking a mean of a ratio with different bases

### Geometric mean
* Is defined as the product of n observations values raised to the power of 1/n 
* Geometric mean is used if the product of the observations is of interest.
* For example: calculate average cache hit/miss ratios in CPUs.

### Different means
* Arithmetic mean: (sum of observations) / (number of samples)
* Geometric mean (of ratios): (product of observations) ^ (1 / (number of observations))
* Harmonic mean: (number of observations) / (sum (1 / observation))
* Weighted harmonic mean: Same as the above but multiply each observation with a set of weights (same of different)

### Summary
* Three things: mean, median and mode.
* There are some guidelines for this.
* We decided to use mean. There are different means.
	- Arithmetic mean
	- Geometric mean
	- Harmonic mean
	- Weighted arithmetic/geometric/harmonic mean
* Geometric mean is not always the right answer for the ratio case.

### Variability (dispertion)
There are several way to measure varability. However the only two actually used is variance and percentiles

#### Range
* Range = Max - min.
* Larger range means higher varability.
* Range as a lone metric is not very useful.
* Min often comes out as zero and the maximum is usually some outlier.
* Unless our variable is bounded, increasing the number of observations leads to an increase of max and a decrease in max.
* Range is only useful if the variable is bounded.

#### Variance
* s^2 = 1/(n-1) sum^n\_i=1 (x\_i - xbar)^2, where xbar = 1/n sum^n\_i=1 x\_i  
* We are using s because sigma is over the entire population and here we are looking at variance for a sample or set.  
* The divisior for s^2 is n-1 and not n as only n-1 observations are indepedent.  
* Degrees of freedom: the number of independent terms in a sum.  
* Variance is expressed in units which are square of the units of the observations. For example: if x\_i is in metre, then the unit of variance is metre^2. This is not very ideal for us as the variance will change depending on the unit of s. Better to use standard deviation.  
* Coefficient of variance (COV) should be used as it takes the variability of the measurement out of the consideration.  

#### Percentiles
* Specifiying the 5-percentile and 95-percentile has the same impact as specifying min/max.
* This can be done for any variable, does not have to be bounded.
* Percentiles are defined in natrual numbers between 0 and 100. 
	- We can also express them as fractions [0, 1]. Then they are called quantiles (fractile).
	- 0.5 qunatile is the same as 50-percentile
* Decitiles is the multiple of 10% such that the first decile is 10-percentile, second the 20-percentile and so forth.
* Quartiles is the multiple of 25%.
* alpha quatriles can be estimated by [(n-1)*alpha+1]. [.] means we round to nearest integer.
	- To be precise, we use linear interpolation for continouous variables.

#### Semi inter-quatile range
Some metric never used.

#### Mean absolute deviation
* Good point: No need to square root or multiplication
* Negative point: "I am not sure?????????????????"

#### Comparision
* Range is affected by outliers. Do not use.
* Sample variance is also affected by outliers but the effect is lessened.
* Mean absolute deviation is next in resistance to outliers
* SIQR is very resistant to outliers.
	- SIQR is preferred to standard deviation if the distribution is highly skewed

#### Selecting the index of dispersion
1. Is the distribution bounded? -> Use range
2. If the distribution is unimodal symmetrical? -> use C.O.V
3. Otherwise use percentiles or SIQR
But also it is also very dependent on the problem. 

### Determining distribution of data
* ***The simplest way to determin the distribution is to plot a histogram***
	- Count observations that fell into each cell or bucket
	- The key problem is determining the cell size
	- Small cells: large variation
	- Large cells: small variation
	- Cell size makes it possible to reach different conclusions about the distribution.
	- Rule: if any cell has less than 5 observations, then the cell size should be increased.
* Best way Raj has found to find the distribution of a set of data: ***Quantile-Quantile plot***
	- You are trying to fit a distribution to the data.
	- On one axis we plot the quantile observations and on the other the qunatiles of the distribution we "think" the data is. If the relationship is linear, its that distribution.
