# [Comparing Systems using Sample Data](https://www.cse.wustl.edu/~jain/cse567-17/k_13cs.htm)

## Sample
* From the french word, essample, which contains both sample and example.
* Two important notes:
	- One example is not theory
	- You cannot make a definite statement from a single sample

## Sample vs Population
* If we generate a distribution and we draw millions of random samples from this observation, the samples will not have the same mean as the population.
* Population characteristics are always written in greek, while sample characteristics are always written in english.

## Confidence interval
* A confidence interval is a interval for estimating a certain parameter, such as population mean. Using confidence interval we get a interval of acceptable values for the parameter we want to estimate, rather than a singular value.
* The likelihood that the real (unknown) value lies in this range is defined by our confidence level, and this is often defined in percentage (for example 95% confidence level).
* The end points of our confidence interval are called confidence limits.
* A higher confidence level leads to a larger confidence interval.
* Confidence in statistics means that: A claim of 95% confidence means that the researcher has seen one possible interval from a large number of possible ones, from which 19 out of 20 intervals contain the true value of the parameter.

### Cofidence interval meaning
* If we take 100 samples and construct confidence interval, with 90% confidence, for each sample, the interval would include the popoulation mean in 90 cases. And we can get this from 1 sample.
* For each sample, we get a interval where mew might lie. However, we are not 100% sure mew will lie there, hence the percentage defined. Mew does lie somewhere in the interval (fixed), but we are getting different intervals for each sample.

### Determining confidence interval
1. Find the number of samples, n
2. Calculate the mean of the samples (If we have indepedent variables then the central limit theorem states that our sample mean will resemble a normal distribution).
3. Calculate the standard distribution
4. Decide our confidence interval
5. Find the Z value for the selected confidence interval (look in a table)
6. Calculate: confidence interval = mean +- Z * s / sqrt(n)

For small samples (n < 30), we need to calculate the t value (from the t table) instead of z. We will look up t[1-alpha/2][n-1]. t can only be used if the population is normal.

For large samples you do not need the asumption of normal.

### Testing for a zero mean
* If the range includes zero, the mean could be zero.
* If the range does not include zero, the mean cannot be zero.

### Paired vs unpaired comparisons
* Paired: relationship between x\_1 and y\_1. Example: performance on i:th workload.
	- Use confidence interval of the difference.
* Unpaired: no relationship between x\_1 and y\_1. Example: n people on system A, n on system B.
	- Need something more sophisticated method.

### What confidence level to use?
* Depends on the problem.
* Base on the loss that you would sustain if the parameter is outside the range and what is the gain if the parameter is inside the range.
	- Low loss: Low confidence level is fine, for example, when buying a lottery ticket.
	- High loss: 90% that a bomb goes off correctly and 10% that it goes off randomly. This is not acceptable.
	- 50% confidecne level may or may not be too low. It all depends on the problem.
	- 99% confidence level may or may not be too high. It all depends on the problem.
* We can also do one sided confidence intervals. Also depends on the question at hand.
* We can also have confidence intervals for proportions.
	- Proportion = probabilities of various categories such as P(error) = 0.01 and P(no error) = 0.99

### Summary
* All statitics based on a sample are random and should be specified with a confidence interval
* If the confidence interval includes zero, the hypothesis that the population mean is zero cannot be rejected
* Paired observation -> Test the difference for zero mean
* Unpaired observation -> More sophisticated tests
* Confidence intervals apply to proportions too.
