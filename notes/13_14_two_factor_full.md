# [Two Factors Full Factorial Design without Replications](https://www.cse.wustl.edu/~jain/cse567-17/k_21ffd.htm)
* Two factor is used when there is two parameters that are carefully controlled.
	- Example: Compare several CPUs using several workloads
* Assumption: Factors are categorical. Otherwise use regression models.
* Goes through example 21.2
* This was using an additive model, but the factors might not add. Solution: multiplicative model.
	- Example: Processors and workload
* If we are missing observations
* All you have to do is carefully divide by the number of terms that you are adding (mean).
* Alternative method: put value there so he missing experiment adds up to zero.
* Everything is calculated normally, but we have the row and the colums to calculate row mean, column mean etc.

# [Two Factor Full Factorial Designs with Replications](https://www.cse.wustl.edu/~jain/cse567-17/k_22cie.htm)
* What do we get with replications?
* New term in the model, replications, that allows seperating out the interactions from experimental errors.
	- Without replications we ignore the interaction
* Assumption: All rows and colums sums are zero.
* Goes through example 22.1, 22.4 and 22.5
