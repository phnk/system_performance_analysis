# Computer performance analysis project
This is the project in the computer performance analysis project.  

The goal of this project is to examine how we can measure the performance of an autonomous solution performing the short-loading cycle and how can these metrics be embedded during training.
More specifically, how can a reinforcement learning agent use relevant metrics to improve its policy such that we are moving closer to human performance?
In addition, we also want to examine when and how the content from the course can be used for analysing the performance of the said solution.

Previous work has used two main metrics when measuring the human performance of operators. 
The first is productivity which is usually measured in kg of material per hour, while the second one is fuel usage/fuel efficiency which measures how much fuel is used per moved kg or how much fuel is used per hour.
Both of these metrics are difficult to measure between timesteps, which is what we want to do during training, hence making it difficult to directly optimize.
However, we can still use them to measure how well the solution is performing, when performing the full cycle.

Productivity and fuel usage are highly coupled such that if an operator wants to increase their productivity substantially, this will come at the expense of how much fuel is being used per moved kg.
So what most operators do is they have some productivity goal and then they try to decrease their fuel usage while still reaching that productivity goal.
It is also unclear how this can be achieved and measured when it comes to an autonomous system.

Some previous automation work has been done for the different sub-steps of the short-loading cycle, which all have used different metrics for measuring success.
When it comes to scooping, the metric most often used is the amount of weight or volume in the bucket at the end.
However, this is not a good metric for the entire cycle as it is possible to overfill the bucket for the navigation part.
For navigation it's either some pseudo productivity measurement using some assumed weight in the bucket, however, this is just a time measurement as productivity is moved weight/time unit.
Lastly, for navigation, some work has tried to minimize the distance of the generated path, which can also be problematic when taking material in the bucket.

From all of this, the scope of this work is the following:
1. Examine the plausibility of using productivity and fuel usage for measuring the full cycle and parts of the cycle.
2. Examine what other types of metrics exist that could be used for the short-loading cycle.
3. Examine if what we have learned in the course can be applied to this problem.

Hopefully, this work can be used for a section in the upcoming paper and form a basis for analysing the performance of a proposed system.
