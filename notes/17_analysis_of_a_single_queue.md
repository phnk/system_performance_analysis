# [Analysis of A Single Queue](https://www.cse.wustl.edu/~jain/cse567-17/k_31asq.htm)
* Birth-death process
	- Jobs arrive one at a time
	- State = Number of jobs n in the system
	- Arrival of a new job changes the state from n to n+1 (a birth)
	- Departures of a job from the system changes the state from n to n-1 (a death)
	- Easily visualised in a diagram (see examlpe in the slides)
* Theorem: State probability
	- Caclulate the probability of being in a state n in a steady state system.
	- He goes through the proof.
* M/M/1 queue
	- most common type of queue
	- can be used to model single processor systems
	- assumption: interarrival times and service times are exponentially distributed and there is only one server.
	- no buffer or population size limitations and the service discipline is FCFS
	- only need to know mean arrival rate lambda and the mean service rate u
	- our state = number of jobs in the system
	- Results for M/M/1 queue: probability of n jobs in the system: p = (arrival rate/service rate)^n * p\_0.
	- The quanity lambda/u is called traffic intensity (ro)
	- p\_n = (1 - ro)*ro^n
	- By analysing p\_n as a series, we can find that n is geometrically distributed.
	- And we can define the utilization of the server: U = ro
	- The mean number of jobs in the system: E[n] = ro/(1-ro)
	- Variance of the jobs in the system: Var[n] = ro/(1-ro)^2
* Goes through Box 31.1 M/M/1 queue from the book
* M/M/m queue
	- Same formulas as above if m = 1 (good way to check that what you have dervived is correct)
* M/M/m/B queue
	- Has the same set of formulas, more complex.
* Many different queue examples in the textbook with all results
	- M/G/1
	- M/G/1/inf/inf/Process sharing
	- M/D/1
	- M/G/inf
	- etc
	- Just go to the boxes in the book when you need them
* Summary
	- Birth-death processes: Compute probability of having n jobs in the system
	- M/M/1 Queue: Load-independent. 
	- Traffic intensity: ro = lambda/u
	- Mean number of jobs in the system: ro/(1-ro)
	- Mean response time: (1/u)/(1-ro)
