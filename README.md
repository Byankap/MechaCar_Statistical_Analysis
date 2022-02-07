# MechaCar_Statistical_Analysis
R and RStudio
## Background
Working for AutosRUs' newest prototype, MechaCar, which is suffering from production troubles. Purpose is to review production data and perform the following: perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes, collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots,  run t-tests to determine if the manufacturing lots are statistically different from the mean population, design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers.
Data tools:  tidyverse, dplyr, ggplot2
## Deliverable 1: Linear Regression to Predict MPG
### Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
Based on the Pr(>|t|), vehicle length and vehicle ground can statistically provide non-random variance to the model; having an impact on miles per gallon to the MechaCar prototype. The rest, have a p-value that has random variance to the dataset. 
### Is the slope of the linear model considered to be zero? Why or why not?
The p-value is 5.35e-11, since it is smaller than 0.05%, there is evidence to reject the null since the slope is not zero. 
### Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
The linear model r-squared of 0.71, so 71% of mpg predictions can be determine by this model effectively. 
![Alt text](https://i.imgur.com/HtGwFWg.jpg)

## Deliverable 2: Summary Statistics on Suspension Coils
Two objectives: obtain the suspension coil’s PSI continuous variable across all manufacturing lots and the following PSI metrics for each lot: mean, median, variance, and standard deviation.
### The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?
The Suspension Coil dataset contains the testing of capacities of multiple suspension coils from three lots.
Data from all manufactoring lots:
![Alt text](https://i.imgur.com/RgTnNLe.jpg)
Each lot separately:
![Alt text](https://i.imgur.com/j3NyZGP.jpg)
Based on the entire population of the production lot, the variance is 62.3 PSI, within the range of 100 PSI of the variance requirement. While Lot1 and Lot2 are within the 100 PSI variance requirement, Lot3, has a larger variance performance (170.3). Lot3 has a a full lot level. 

## Deliverable 3: t-Tests on Suspension Coils
Objective is to perform t-tests to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch.
This is the summary of the t-test results across all manufacturing lots:
![Alt text](https://i.imgur.com/Gss3Aow.jpg)
Based on the summary data, the mean is 1498.8 and the p-value of 0.06, rejecting the null due to insufficient evidence. 
Based on each lot summary:
Lot1: p-value is 1, rejecting the null to due no statistical difference between the observed sample mean and the mean.
Lot2: p-value is 0.61, same comment as Lot1.
Lot3: p-value is 0.04, lower than the significance level of 0.05, rejecting the null since the mean are not statistically different. 
Lot3 processes need to be checked for system and product fails since the quality of products are not meeting criteria. 

## Deliverable 4: Study Design: MechaCar vs Competition
Write a short description of a statistical study that can quantify how the MechaCar performs against the competition. In your study design, think critically about what metrics would be of interest to a consumer: for a few examples, cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating.
In your description, address the following questions:
What metric or metrics are you going to test?
Independent variables include: safety ratings, drive package, engine, resale value, annual cost of ownership, mpg. Dependent variable would be the selling price.
What is the null hypothesis or alternative hypothesis?
Null Hypothesis(Ho): MechaCar is correctly priced based on its performance key factors.
Alternative Hypothesis(Ha):  MechaCar is NOT correctly priced based on its performance key factors.
What statistical test would you use to test the hypothesis? And why?
A multiple linear regression test would be used to determine the hightest predictability impact of price and independent factors. 
