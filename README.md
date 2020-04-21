### E-commerce website A/B test results

In this project, we analyze the results of an A/B test performed by an e-commerce website. The objective is to determine 
the probability of converting after seeing the old webpage or the new page. For that purpose, we tested the feature on 
two groups: a control group and a treatment (or experiment) one. The control group viewed the old page while the treatment 
group viewed the new one.

After setting our null and alternative hypotheses to be: 
                                                    H0: p_old ≥ p_new
                                                    H1: p_old < p_new

We simulated the test 10,000 times on a sample distribution of ab_test population.

By plotting the distribution from the null and comparing against the actual observed difference in conversion rates, the 
results didn't prove to be statistically significant enough to justify making changes to the website. With a p-value of 
approx. 0.9, we would fail to reject the null and keep the old webpage in place. We also used the built-in Python module 
statsmodels and arrived at the same conclusion.

By fitting a logistic regression model, we seek to predict two possible outcomes: conversion or no conversion. We see from 
the results summary table above that the likelihood of converting given that an indidividual was in the treatment group isn't 
statistically significant with a p-value of 0.19 (two-sided), confirming once again that we should stick with the old webpage.

Lastly, we added a country variable to our regression model to see whether the region where individuals were located affected 
the conversion rate. With a p-value over the conventional threshold of 0.05, we would conclude here that the region isn't a 
determining factor contributing to the conversion rate.
