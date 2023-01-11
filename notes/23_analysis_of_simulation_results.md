# [Analysis of Simulation Results](https://www.cse.wustl.edu/~jain/cse567-17/k_25asr.htm)
* Model verification = Debugging
* Model validation = Correct compared to the real world system
* Four possibilities:
	- Unverified, invalid
	- Verified, invalid
	- Unverified, valid
	- Verified, valid
* Model verification techniques
	- Top down modular design: divide and conquer
	- Anti-bugging: Self-checks (asserts for example)
	- Structured walk-through
	- Detemrinistic models
	- Run simplified cases
	- He says trace everything but just use a debugger?
	- On-line graphic displays
	- Continuity test
	- Degeneracy tests: Try extereme configurations
	- Consistency tests
	- Seed independence
* Model validation techniques
	- Validation means that the model is equal to the real world
	- Validation techniques for one problem may not apply to another problem
	- Check assumptions that they hold
	- Input parameter values and distributions
	- Output values and conclusions
	- Techniques: Expert intuition, Real system measurement, theoretical results.
	- Experts usually knows if the results are incorrect. For example: higher throughput in a link when packet loss goes up.
	- Real system measurement compares the results to real system data.
	- Theoretical results we compare the theory to the results of the simulation. Problem is that both the theory and the simulation might be invalid. For example: we make the same assumptions for both, where these assumptions do not hold.
* Transient removal
	- Generally steady state perofrmance is interesting.
	- Achieved by removing the inital part.
* Transient removal techniques
	- Long run
	- Proper initialaztion
	- Truncation
	- Initial data deletion
	- Moving average of independent replications
	- Batch means
* Sometimes in some simulations we are interested in the initial part of the simulation (transient performance)
* When exiting the simulation we have to deal with the leftover entities somehow.
	- Example: when we close the doors to a store the leftover enties (the customers outside) can not enter.
	- So what happens to the statiscs we compute?
	- When there are many entities leftover the statistics might be incorrect.
* Stopping criteria: when to stop the simulation.
	- Run until we have a confidence interval that is narrow enough.
* Variance estimation methods
	- Independent replications
	- Batch means (also called sub-samples)
	- Method of regeneration (Raj has never used this in any application)
