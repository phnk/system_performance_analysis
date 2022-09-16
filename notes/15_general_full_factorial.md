[General Full Factorial Designs With k Factors](https://www.cse.wustl.edu/~jain/cse567-17/k_23agd.htm)
**Poor sound the entire lecture**

* Covariate is a factor that cannot be controlled for but can be measured.
	- Example: Temperature
	- Can be added as a predictor in a regression model
* General Full factorial designs with k factors
	- Model k factors gives 2^k-1 effects.
	- k main effects
	- (k over 2) two factor interactions
	- (k over 3) three factor interactions
	- and so on.
* Case study 23.1
	- For page swaps: Realises that the only interaction that has a non negliable interaction is DM, creates a simplified model that only cares about that interaction rather than all of them.
* Observation method
	- Used to find the best combinations.
	- Example: Scheduler design
	- Three classes of jobs:
		1. Word processing
		2. Interactive data processing
		3. Background data processing
	- Five factors 2^(5-1) design
* Looks into the table for example 23.1, uses row 7 and 11 to conclude that to get high throughput for word processing jobs we should:
	- Not have any preemption (A = - 1)
	- The time slices should be large (B = 1)
	- The fairness should be on (E = 1)
	- The queue assignment and requeueing does not matter.
* Ranking method (same example)
	- Sort the experiments
	- From the sort we can see what options give a consistently high score and what options give a considently lower score
	- This gives:
		1. A = -1 (no preemption) is good for word processing jobs
		2. A = 1 is just bad (all at the bottom)
		3. B = 1 (large time slice) is good for such jobs.
		4. B = -1 No strong negative conclusion can be made.
		5. C = 1 If there is a choice, it should be 1 (there are two queues).
		6. The effect of E is not clear as E = 1 is on both the top and the bottom with no mix.
		7. If the rop row is chosen, then E = 1 is a good choice.
* Range method
	- Range = Maximum - Minimum
	- Factors with large range are important
	- Memory size is the most influential factor as the range is large
	- The order for the next are Problem program, deck arrangement, and replacement algorithm
* Summary
	- A general k factor design can have k main effects and multiple factor interactions (two factor interactions, three factor interactions and so on)
	- Information methods:
		1. Observation: Find the highest or lowest response
		2. Ranking: Sort all responses
		3. Range: Largest - smallest average response

