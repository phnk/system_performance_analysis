# [Introduction to Simulation](https://www.cse.wustl.edu/~jain/cse567-17/k_24its.htm)
* Common mistakes in simulation
	- Inappropriate level of detail
	- Improper language.
	- Unverified Models: bugs.
	- Invalid Models compared to reality.
	- Improperly handled initial conditions.
	- Too short simulation: need confidence intervals
	- Poor choice of random number generators.
	- Improper selection of seeds.
* Other causes of simulation analysis failure
	- Inadequate time estimate
	- No achievable goal
	- Incomplete mix of essential skills
	- Inadequate level of user participation
	- Obsolete or nonexistent documentation
	- Inability to manage the development of a large complex computer program
	- Mysterious results
* Checklist for simulations:
* Before simulations start
	- Is the goal of the simulation specified correctly?
	- Is the level of detail appropriate?
	- Does the simulation team include all required personel?
	- Has sufficient time been planned for the creation of said simulator?
* Checks during development
	- Has the RNG been tested for uniformity and independence?
	- Is the model reviewed regularly with the end user?
	- Is the model documented?
* Checks during runtime?
	- Is the runtime length appropriate?
	- Are the intial transients removed before computing?
	- Has the model been verified?
	- Has the model been validated?
	- If there is any suprising results, have they been validated?
	- Are seeds non overlapping?
* Terminology
	- State variable.
	- Event: changes to the state.
* Types of models
	- Continuous state model
	- Discrete state model
	- Deterministic model
	- Probabilistic model
	- Static model
	- Dynamic model
	- Linear model
	- Non-linear model
	- Open model
	- Closed model
	- Stable model
	- Unstable model
* Type of simulations
	- Emulation: Using hardware
	- Monte Carlo simulation
	- Trace-driven simulation
	- Discrete event simulation
* Monte carlo simulation
	- Static simulator
	- To model some probalistic phenomenon
	- Need pseudo-random generator
	- Used for evaluating non-probablistic expressions using probalistic methods
* Trace-driven simulation
	- Trace = Time oredered record of on a system
	- Input = Trace
	- Used to analyze or tuning resource management algorithms: paging, cache, etc.
	- Example: Page reference patterns
	- Should be independent of the system under study
* Advantages of trace-driven simulation
	- Credibility
	- Easy vvalidation
	- Accurate workload
	- Detailed Trade-offs
	- Less randomness
	- Fair comparison between different simulations
	- Similarity to the actual implementation
* Disadvantages of trace-driven simulation
	- Complexity (in how detailed, not time complexity)
	- Representativeness
	- Finiteness
	- Single point of validation
	- Detail
	- Trade-off: Difficult to change workload
* Discrete event simulation
	- Events pushing it forward
	- Same as lab 5 in the java course.
	- Discrete state is not the same as discrete time.
