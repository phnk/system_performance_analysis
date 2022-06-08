# [Course Introduction](https://www.cse.wustl.edu/~jain/cse567-17/index.html)

## Why does this course exist?
1. Many paper has large problems. This is a course on analysis any system, algorithm, or component.
2. This includes measurement, statistical modeling, experimental design, simulation, and queueing theory.
3. Lastly, how to avoid common mistakes in performance analysis.

Book: ["The art of computer systems performance analysis"](https://www.cse.wustl.edu/~jain/books/perfbook.htm)

## Learning objectives
1. Specifying performance requirements. Is the availiability important? Is the delay important?
2. Once we have these requirements, how do we evaluate design alternatives? 
3. We have to be able to compare two or more systems.
4. Determining the optimal value of a parameter (system tuning)
5. Finding the performance bottleneck incase we have a system that is not performing well enough
6. Characterizing the load on the system. How do we decide the workload on the system?
7. Determining the number and sizes of components. How much CPU/ram/sharding do we need?
8. Predicing the performance at future loads (forcasting). How much traffic do we think we need? What factor do we increase that with? What do we do incase of lower/higher traffic?

## Some basic terms
1. System: Any collection of hardware, software, and fireware. (Other def later on, very flexiable term)
2. Metrics: Critera used to evaluate the performance of the system. (We have a security system, how do you measure the performace? Encryptions per second? Some other metric?)
3. Workloads: The requests made by the user of the system.

## Structure of the course
### Overview of performance evaluation
Introduction (this), Common mistakes and how to avoid them, Selection of techniques and metrics.

### Measurement techniques and tools
Types of workloads, popular benchmarks, monitors, logs, load drivers, capacity planning, etc.

### Propability theory and statistics
Distributions, summarizing measured data by a single number, sample statistics, confidence interval, regression models, etc.

### Experimental design and analysis
Introduction to experimental design, factorial design.

### Simulation
Types of simulation, model verification and validation, RNG and how to test RNG, distributions, how long should we run the simulation?, etc.

### Queueing theory
Introduction, queueing networks, operational laws, convolution algorithm, etc.

### Stochastic prcoesses
Different types of time series models, heavy-tailed distributions, short-range and long-range dependent process, etc.
