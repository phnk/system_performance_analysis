# [One Factor Experiments](https://www.cse.wustl.edu/~jain/cse567-17/k_20ofe.htm)
* Change design, make it more general
* Until now, we have 2 levels, 2^k, 2^(k-p) etc.
* Now we will do multiple levels.
* Start with simple example: many levels, 1 factor.
* On factor experiments are used to compare alternatives of a single categorical variable.
* The model used in single factor designs is: yij = u + aj + eij
	1. The effects are calculated so sum of effects, aj, is 0
	2. We compute the effects by creating a table with column sums, column mean and lastly, column effect (aj). 
	3. We then estimate the experimental errors by calculating sum of squared error (SSE).
	4. We then calculate the allocation of variation by calculating SST (the total variation), SSA (the sum of square of effects) and then taking 100 * (SSA/SST) to get the percentage of variation explained by the factor.
	5. We now need to perform an analysis of the variance to figure out if the factor is significant. This analysis is shorted to ANOVA. This is done by creating an ANOVA table.
	6. We can use an F-test to check if SSA is significantly greater than SSE.
	7. To make sure that the factor is significant we calculate our confidence interval for the effects. If the confidence interval for the effect includes zero, it is not significant. Parameter estimation equations can be found in table 20.5.
* See page 341 in the book for a better bullet point list.
* This type of analysis is presented under a set of assumptions
	1. The effects of various factors are additive
	2. The errors are additive
	3. The errors are indepdent of the factor levels
	4. The errors are normally distributed
	5. The errors have the same variance for all factor levels
* As normal, these can be verified by using the visual tests described previously (regression, 2^(k-p), etc)
* This is under the assumption that our sample sizes are equal. If they are unequal we can still analyze it, but you need to divide it by the number of observations added. Each effect will have a different degree of freedom so we need to be careful when doing the analysis such that we actually use the correct degree of freedom.
* Summary
	- Model for one factor experiments, yij = u + aj + eij. Sum aj = 0.
	- Computation of effects
	- Allocation of variation, degrees of freedom
	- ANOVA table
	- Standard deviation of errors
	- Confidence intervals for effects and contrasts.
	- Model assumptions and visual tests

