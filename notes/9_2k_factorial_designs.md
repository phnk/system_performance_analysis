[2k Factorial Designs](https://www.cse.wustl.edu/~jain/cse567-17/k_172kd.htm)
* k factors, each at two levels
	- This is easy to analyze
	- Helps in sorting out impact of factors
	- Good at the beginning of a study
	- Valid only if the effect is unidirectional
	- For exmaple: 2 factors at 2 levels = 2^2
* Example
	- Two x variables, both are binary. 2^2 factorial design. All 4 possible combinations.
	- Analyse using some model, calculate a solution from the observation. We get the effect.
	- Use the -1 +1 trick to make things cancel out and get nice mathematics in the end.
	- Easy way to do this. Write down in a table similar to a truth table in boolean algebra. (Sign table method)
	- We get 4 equations and solve it by adding all values and dividing by 4 (4 equations).
	- Calculate the coeffients, qs.
	- Sum of the coefficients is zero. These are called contrast.
	- Calculate their variation. For 2^2 design: SST = SSA + SSB + SSAB. Important: Variation is not equal to variance.
* General 2^k Factorial Designs
	- k factors at two levels each.
	- 2^k experiments
	- 2^k effects. Lots of effects
* Summary
	- 2^k design allows k factors to be studied at two levels each
	- Can compute main effects and all multi-factors interactions
	- Easy computation using sign table method
	- Easy allocation of variation using squares of effects
