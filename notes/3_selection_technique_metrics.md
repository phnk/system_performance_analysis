# [Selection of Techniques and Metrics](https://www.cse.wustl.edu/~jain/cse567-17/k_03tam.htm)
How do we select an evaluation techniques and how do we select our metrics?

## Criteria for selecting an evaluation technique
Three techniques: Analytical modelling, Simulation and Measurement. These have all different ctiterion, such as we can only measure things postprototype. We also need to know how fast we need the results. Do we want the result in a few minutes, a few hours, or a few days?  
Our criterions are Stage, Time required, Tools, Accuracy, Trade-off evaluation, Cost and Saleability.

## Three rules of validation
1. Do not trust the result of a simulation model until they have been validated by analytical modelling or measurement.
2. Do not trust the result of an analytical model until they have been validated by simulation or measurement.
3. Do not trust the result of a measurement until they have been validated by analytical modelling or simulation.

## Selecting Perforamce Metrics
Step 1: What does the system do (in terms of services)? This can then be graphed in different ways to visualise it.

Include: Performance time, rate, resources. Error rate, probability. Time to failure and duration.  
Consider including: Mean and variance. Individual and Global.  
Selection criteria: Low-variability. Non-redundancy. Completeness.

## Case study
Who congestion control algorithms.

Service: Send packets from source to destination, in order.  
Possible outcomes:
1. Some packets are delivered in order to the correct dest
2. Some packets are delivered out of order to the correct dest
3. Some packets are delivered more than once.
4. Some packets are dropped.

Performance: 
1. If packets are delivered in order.
	- Time-rate-resource:
		+ Response time (time)
		+ Throughput (packet/time)
		+ Processor time at source (time)
		+ Processor time at dest (time)
		+ Processor time per packet on dest (time/packet)
	- Variability of the response time (Retransmissions)
		+ Response time in terms of delay inside the network (time)
2. If packets are delivered out of order
	- Probability of this occuring
3. If we get duplicate packets
	- Probability of this occuring
4. Lost packets
	- Probability of this occuring
5. Disconnection
	- Probability of this occuring

NOTE: This is not in the course, but there are examples of OTHER things that we need to take into account. In this example we are working with shared resources. To make this work we have to use some type of fairness so we can decide who gets the throughput.

Throughput and delay is however redundant so we can instead use Power = Throughput / Response time.  
This redundancy can be understood by: if throughput is low, the delay will be high and vice-versa.

## Commonly used metrics
1. Response time and Reaction time
	- Depends on definition (of course)
2. Capacity
3. Turnaround time (time between submission of a batch job to output)
4. Stretch factor (ratio between response time of multithreaded program to non multithreaded)
5. Throughput (rate, something/unit of time)
6. Efficiency (usable capacity to nominal capacity)
7. Utilization (fraction of time the resource is busy)
8. Reliability (probably of error, time to error)
9. Availability (time to failure, time to repair)

## Setting performance requirements
"The system should be x and y. It should not do a. It should not have b property."
As an example for a router: "The probability of any bit being in error must be less than 1e-7"
