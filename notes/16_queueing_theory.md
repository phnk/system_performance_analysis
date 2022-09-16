# [Introduction to Queueing Theory](https://www.cse.wustl.edu/~jain/cse567-17/k_30iqt.htm)
* Basic components of a queue
	1. Arrival process
	2. Service time distribution
	3. Number of servers
	4. Waiting positions
	5. Population size
	6. Service discipline (like FIFO)
* To specify a queue we use Kendall Notation (A/S/m/B/K/SD) where,
	1. A: Arrival process
	2. S: Service time distribution
	3. m: Number of servers
	4. B: Number of buffers (system capacity)
	5. K: population size
	6. SD: Service discipline
* Arrival Processes
	- Arrival times: t1, t2...
	- Interarrival times: tau\_j = tj - t(j-1)
	- tau\_j form a sqeuence of independent and identically distributed (IID) random variables
	- Notation:
		1. M = Memory less = Exponetial
		2. E = Erlang
		3. H = Hyper-exponetial
		4. D = Deterministic = Constant
		5. G = General = Results valid for all distributions
* Service time distribution
	- Time each student spends at the terminal
	- Service times are IID
	- Distribution: M, E, H, D, or G
	- Device = Service center = Queue
	- Buffer = waiting process
* Service disciplines: How do you service the customers
	- The "normal" is First-come-first-served (FCFS)
	- Sometimes you use Last-Come-First-Served (LCFS) = Stack
	- Last-Come-First-Served with Preempt and Resume (LCFS-PR) (Take in the middle of your service)
	- Round-robin (RR) with a fixed quantum.
	- Etc etc.
* Example: A (M/M/3/20/1500/FCFS) queue
	- What do we mean?
	1. M: Memoryless arrival process (Exponential)
	2. M: Memoryless service time distribution (Exponential)
	3. Three servers
	4. 20 Buffers = 3 service + 17 waiting. After 20 all jobs are lost
	5. A total of 1500 jobs can be serviced (population size)
	6. FCFS: First-come-first-served service discipline
* A default queue is: G/G/1 = G/G/1/INF/INF/FCFS
* Do you always analyize queues individually?
* Exponential distribution
	- 1 Queue
* Erlang distribution
	- If you take many memoryless servers and put in series, the sum of these has a erlang distribution
* Hyper-exponential distribution
	- If you take many memoryless servers and put them in parallel, the sum of these has a hyper-exponential distribution
	- Called hyper because the coefficient of variation > 1
* Group arrivals/Service (Bulk arrival/service)
* Notation:
	- M^([x]): x represents the group size
	- G^([x]): a bulk arrival or service process with general inter-group times.
	- Example:
		1. M^([x])/M/1: Single service queue with bulk (poisson) arrivals and exponential service times.
* Key Variables
	- Tau - Inter-arrival time
	- Lambda - Mean arrival rate
	- s = Service time per job
	- mu = Mean rate per server
	- Total service rate for m server is m*mu
	- n = number of jobs in the system (queue length)
	- n_q = Number of jobs waiting
	- n_s = number of jobs receiving service
	- r = Response time or the time in the system
	- w = Waiting time
* Rules for all queues
	1. Stabilitry condition: Arrival rate must be less than service rate (lambda < m * mu)
	2. Number in system versus number in queue: n = n_q + n_s
	3. Number versus time: 
		- If jobs are not lost due to insufficient buffers then Mean number of jobs in the system = Arrival rate * Mean response time. 
	4. Mean number of jobs in the queue = Arrival rate * Mean waiting time (Little's law)
	5. Time in system versus time in queue: r = w + s where r, w and s are random variables.
* Types of stochastic Processes
	6. If the service rate is independent of the number of jobs in the queue, Cov(w, s) = 0. We will assume this is true.
* Littles law applies to any system where the number of jobs that enters the system is equal to those completing service.
	- Goes through proof of little's law
* Applications of little's law
	- Applying to just the waiting facility of a service center
	- Mean number in the queue = Arrrival rate * Mean waiting time
	- Similarly, for those currently reciving the service, we have
	- Mean number in service = Arrival rate * Mean service time
* Poisson distribution
	- If the inter-arrival times are exponentially distributed, number of arrivals in any given interval are Poisson distributed.
	- M = memory less arrival = Poisson arrivals
	- M also called poisson process
* Stochastic Processes
	- Process: function of time
	- Stochastic process: random varibles wihch are functions of time
* Different types of stochastic processes
	- Discrete (is countable). If discrete we call it a stochastic chain
	- Continuous (non countable).
	- Markov. Future states are independent of the past and depend only on the present.
		1. Markov chain: discrete state markov process
	- Birth-death processes
		1. The discrete space Makrov process in which the transitions are restricted to neighboring states.
		2. Process in state n can only go to state n+1 or n-1
	- Poisson process
* PASTA (Poisson Arrivals See Time Averages)
	- You should not deterministcally sample, you should sample using an exponential distribution. Why?
	- You should use poisson sampling (explained above).
