# [Common mistakes](https://www.cse.wustl.edu/~jain/cse567-17/k_02mst.htm)

## Common mistakes in evaluation
1. No goals. Started working on simulation, but does not know why or what the end goal is.
2. Biased goals. "To show that THIS system is better than THAT system".
3. Unsystematic approach. 
4. Analysis without understanding the problem.
5. Incorrect performance metrics. How do we find the correct one?
6. Unrepresentative workload. We should use workloads that are representative of the real world.
7. Wrong evaluation techniques.
8. Overlook important parameters. Lets say x is the thing driving performance, but we do not measure x. Things we can measure, but not change.
9. Ignore significat factors, things we can measure and change.
10. Inappropriate experimental design.
11. Inappropriate level of detail. How deeply we simulate the problem. How detailed is the simulation.
12. No analysis. 
13. Erroneous analysis.
14. No sensitivity analysis. You have to make some assumptions. When you assume things you have to make a sensitivity analysis. How sensitive is our analysis to the assumptions?
15. Ignoring errors in input.
16. Inproper treatment of outliers.
17. Assuming no change in the future. 
18. Ignoring variability. Everything is a random number.
19. Too complex analysis. If you do a complex analysis, make sure that you can present it.
20. Improper presenmtation of results.
21. Ignoring social aspects.
22. Omitting assumptions and limitations. 

## Checklist for avoiding common mistakes
The same list
1. Is the system correctly defined and the goals clearly stated?
2. Are the goals stated in an unbiased manner.
3. Etc. etc.

## Systematic approach to performance evaluation
***Case study***: remote pipes vs RPC. System has a definition. Services (What is the system doing): Small data transfer (Service 1) or large data transfer (Service 2).  
***Metrics***: No errors or failures, rate, time, resource per service, resource = Client, server, network.  
Now we can write down many metrics: Elapse time per call, meximum call rate per unit of time, local CPU time per call, Remote CPU time per call, number of bytes sent per call.  
***System parameters***: Speed of the local/remote CPU, speed of the network, overhead interfacing with the channels, overhead interfacing with the network, reliability.  
***Workload parameters***: Time between sucessive calls, number of size of the call parameters, etc.  
***Factors***: Type of channel: remote pipes and RPCS. Size of the Networks. Size of the call parameters. Number of consecutive calls.  
***Evaluation technique***: Prototypes implemented -> measurements. Use analytical modeling for validation.  
***Workload***: Synthetic program generating the specified types of channel requests. Null channel rquests.  
***Experimental design***: Full factorial experimental designs with 2^3 x 11.  
***Data analysis***: Analysis of variance for the first three factors. Regression for number nof sucessive calls.  
***Data presentation***: The final result will be plotted as a function of the block size n.
