# [2^(k-p) fractorial designs](https://www.cse.wustl.edu/~jain/cse567-17/k_19ffd.htm)
* 2^(k-p) fractorial designs are experimental designs constisting of carefully chosen subets (fraction) of the experiments runs of a full fractorial design.
	- This subset is chosen to exploit the sparsity-of-effects principle, allowing us to expose information about the most important features of the problem studied, while using a fraction of the effort.
	- [Example](https://en.wikipedia.org/wiki/Fractional_factorial_design#Example_fractional_factorial_experiment)
* Full number of factors
	- Full fractorial design is too expensive because we have a large number of experiments. For example: 10 factors -> 1000 experiments. 
	- Use a fractional fractorial design instead.
* 2^(k-p) designs allows us to analyze k factors with only 2^(k-p) experiments.
	- p = 1: requires only half as many experiments
	- p = 2: requires only a quater of the experiments
* Fractorial design features
	- Full fractorial design is easy to analyze due to orthogonality of sign vectors.
	- Fractional factorial design aslo use orthogonal vectors.
* To create a sign table for 2^(k-p) design
	1. Prepare a sign table for a full factorial design with k-p factors
	2. Mark the first column I
	3. Mark the next k-p colums with the k-p factors
	4. Of the 2^(k-p)-k+p-1 columns on the right, choose p columns and mark them with p factors which were not chosen in step 1.
* Confounding: is a variable that influences both the dependent variable and the independent variable, causing a spurious assciation. 
	- [Example](https://en.wikipedia.org/wiki/Confounding#Control)
	- Some designs can have that two different qs have the exact same sum of qs. So its not representing individual, but rather the sum of eachother.
	- They are confunded together. This is not a problem IF the sum of qs is negligible. However, that comes from domain knowledge.
	- Different designs will have different confoundings. 
	- Given just one fonfounding, it is possible to list all other confoundings.
	- Rules: I is treated as unity. Example: I = ABCD. Any term with a power of 2 is erased. Multiply both sides, with for example, A and you get A = A^2BCD = BCD
	- In a 2^(k-p) design, 2^p effects are confounded together.
	- We need to know the confounders to know what effects can be neglibile.
* Design resolution
	- Order of an effect = Number of terms. For example: Order of ABCD = 4. Order I = 0
	- Order of a confounding = Sum of order of two terms. For example: AB = ACDE is of order 5.
	- Resolution of a design is the minimum of orders of all confoundings
	- A design of higher resolution is considered a better design
* Summary
	- Fractional factorial designs allow a large number of variables to be analyzed with a small number of experiments
	- Many effects and interactions are confounded
	- The resolution of a design is the sum of the order of confounded effects
	- A design with higher resolution is considered a better design

