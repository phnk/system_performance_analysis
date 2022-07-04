# [Other Regression Models](https://www.cse.wustl.edu/~jain/cse567-17/k_15orm.htm)
* Multi linear regression models
	- Instead of 1 x, you have k x
* Analysis of variance
	- Test the hypothesis that SSR is less or equal to SSE.
	- Degrees of freedom = Number of indepdent values requires to compute
* F-Test: Test if the test statistic has an F-distribution under the null hypothesis
	- Take any SSi and SSj with vi and vj degrees of freedom, the ratio of (SSi/vi)/(SSj/vj) has an F distribution with vi numenator number of degrees of freedom and vj denominatior degrees of freedom
	- Hypothesis that the sum SSi is less than or equal to SSj is rejected at alpha significant level, if the ratio is greater than the 1-alpha quiantile of the F-variate
	- This procedure is also known as F-test
	- The F-test is used to check: Is SSR significantly higher than SSE?
	- MSR = SSR/K & MSE = SSE/(n-k-1)
	- MSE = Variance of Error
	- MSR/MSE has F[k, n-k-n1] distribution
	- IF the computed ratio is less than the value read from the table, the null hypothesis cannot be rejected at the stated significance level.
* Problems with multicollinearity
	- Two lines are said to be collinear if they have the same slope and same intercept
	- Can be represented in one dimensions
	- When two predictor variables are linear dependent, they are called collinear (two collinear lines are NOT indepedent)
	- Problem: Contradictory results from various significance tests.
	- High correlation: Eliminate one variable and check if significance improves. 
	- For example: Large memory has a high correlation with more disk I/Os. Use one rather than both.
	- ***Lesson: Adding a predictor variable does not always improve regression and if the variable is correlated to another predictor, it may reduce the statistical accuracy of the regression.***
* Regression with categorical predictors
	- We have categories instead of values as predictors. For example: PC and Mac.
	- We need to code our categories by numbers, such as 0 and 1 or -1, +1 (recommendation)
	- If we have more categories, do not code by for example, 1, 2, 3 but rather introduce two predictor variables where x1 = 1 if type A else 0 and x2 = 1 if type B else 0.
	- This gives: (x1, x2) = (1, 0) = Type A, (0, 1) = Type B and (0, 0) = Type C.
	- Levels: Number of values that a categorical variable can take. 
	- If we want to represent a categorical variables with k levels, then we define k-1 binary variblaes: xj = 1 if jth value, 0 otherwise.
	- We can get different conclusions from different assumptions. To know what is "correct" we need to have domain knowledge.
* Curvilinear regression
	- Is if the relationship between response and predictor is non-linear but can be turned into a linear form.
	- For example: y = bx^a can be turned into log y = log b + a*log x
	- Basically the same as subsitution in maths.
* Transformation: Generalization of Curvilinear
	- Do some transformation to the variables to make them analysable
	- Transformations should come from physical consideration (domain knowledge)
	- Basically the same as subsitution in maths.
* Transformation: Generalization of Curvilinear
	- Do some transformation to the variables to make them analysable
	- Transformations should come from physical consideration (domain knowledge)
	- If your data covers several orders of magnitute, you should start looking into transformations
	- If the data is homogeneous variance assumption of the residuals is violated, you should start looking into transformations
* Outliers
	- Any observation that is atypical may be an outlier
	- Including the outlier might change the conclusions and be misleading
	- Excluding the outlier might change the conclusions and be misleading
	- This has to be decided by domain experts
	- To find outliers: scatter plot the data
	- Can also be because a bug in the code/simulation/measurement instruments/etc
* Common mistakes in regression
	1. Not verifying that the relationship is linear
	2. Relying on automated results without visual verification
	3. Attaching importance to numerical values of regression parameters. If the paarameter is too small, it can sometimes be ignored
	4. Not specifying confidence intervals for the regression parameters
	5. Not specifying the coefficient of determination
	6. Confusing the coefficient of determination and the coefficient of correlation
	7. Using highly correlated variables as predictor variables
	8. Using regression to predict far beyond the measured ranged. (if we measure for a month, we cant predict years in the future)
	9. Using too many predictor variables
	10. Do not have to choose the best R^2. A lower R^2 might be for a better range. This has to do with domain knowledge
	11. Measuring only a small subset of the complete range
	12. Assuming that a good predictor variable is also a good control variable. This simply means that its highly correlated, and that does not mean its a good control variable. The predictor works both ways, control usually only works one way.
* Summary
	- Too many predictors can lead to a weak model
	- Categorial predictors should modelled using binary predictors
	- Curvilinear regression is a transformation to a linear relationship
	- Outliers: Use system knowledge to include/exclude. Check measurements and for bugs. Do not just remove outliers. They usually exist for a reaso
	- Common mistakes for regression: no visual verifaction, control vs correlation
