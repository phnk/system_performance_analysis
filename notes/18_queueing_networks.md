# [Queueing Networks](https://www.cse.wustl.edu/~jain/cse567-17/k_32qn.htm)
* What is a queueing network?
	- Model in which jobs departing from one queue arrive at another queue (or possible the same queue)
* Open Queueing networks
	- External arrivals and departures
	- Number of jobs in the system varies with time
	- Throughput = arrival time
	- Goal: To characterize the distiribution of jobs in the system
	- Can be memoryless
* Closed queueing network
	- No external arrivals or departures
	- Total number of jobs in the system are constant
	- "OUT" is connected to "IN"
	- Throughput: the flow of jobs in the OUT-to-IN link
	- Number of jobs is given, determine the throghput
	- Clearly not memoryless
* Are non memoryless queues always markov?
* Mixed queueing networks
	- Open for some workloads and closed for others (two classes of jobs)
* The simples network will be a series network
	- k M/M/1 queues in series
	- Each individual queue can be analayzed independently of other queues
* General open network of queues
	- Product form networks are easier to analyze
* Closed product-form networks
	- Arrivals cannot be poisson
* Machine repairman model
	- A number of working machines with a repair facility with one or more servers
	- Whenever a machine breaks down its put in an infinite queue waiting to be repaired until a repairman is free
* Central server model
	- Computers are multiple queues (CPU, disk, etc)
	- CPU is the central server that schedules visits to other devices
	- After service at the I/O devices the jobs return to the CPU
* Types of service centers
	- Fixed-capacity service centers: service time independent of number of jobs.
	- Delay centers of initite server: No queueing. Jobs spend the same amount of time in the queue no matter what.
	- Load-dependent service centers: Service rate may depend upon the load or the number of jobs in the device.
* Summary
	- Open, closed and mixed queueing networks
	- Product form networks: any network in which the system state probability is a product of decives state proabilities.
	- Jackson, BCMP, Denning and Buzen
	- Service centers: fixed capacity, delayed centers, load dependent
