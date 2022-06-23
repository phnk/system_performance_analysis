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

### Determining confidence interval
1. Find the number of samples, n
2. Calculate the mean of the samples (If we have indepedent variables then the central limit theorem states that our sample mean will resemble a normal distribution).
3. Calculate the standard distribution
4. Decide our confidence interval
5. Find the Z value for the selected confidence interval (look in a table)
6. Calculate: confidence interval = mean +- Z * s / sqrt(n)


