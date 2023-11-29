## Objective
- Undestand which factors impact churn and how can we reduce churn?
- Find the probability of the specified event for a subject after specified time t.


## Terminology
- Survival analysis is defined as a collection of statistical longitudinal data analysis technique where time is a major factor.
- Events - survival analysis deals with the events related to failure. Definition of failure must be clear.
- Subject - represents the entity which is going through some phases and the failure (or the event) is attached to it.
- Failure time or Survival time - time taken till failure is referred to as the failure time or survival time.
- Censoring - it is caused by not observing some subjects for the full time till failure (or event) i.e. not observing a cusstomer or ciustomer doesn't churns out of the system before the end of the observation period. Example, we last observed a customer at time t1 and he churned later when we observed at time t2. So the customer churned out between t1 & t2 - in this case we don't know the exact time of churn, it is understood that the data is censored.
- Risk set - cohort of customers considered for churn/survival analysis.
- Survival Function - it returns the probability of an event occurring after time t.
    Mathematically, S(t) = P(T > t), 0 < t < infinity.
    S(t) gives the probability of a subject surviving after time t. S(t) is nothing but a probability distribution over time. 
    Theoretically, t ranges from 0 to infinity, S(t) will have values from 0 to 1.
    Survival function is represented by a decreasing smooth curve which begins at S(t) = 1 at t = 0.
    ![Survival Curve](https://github.com/tusharkumarsaxena/customer_analytics/blob/main/survival_analysis/images/Survival%20Function%20Curve.PNG)

    In practical scenarios, curves generated from real datasets may look broken or stepwise, as follows:
    ![Survival Curve - non-paramatric](https://github.com/tusharkumarsaxena/customer_analytics/blob/main/survival_analysis/images/Survival%20Function%20Curve%20-%20Non-parametric.PNG)
- Hazard Function - it is is opposite to survival & is churn rate. It can also be called failure rate.


## Why can't we use Regression for Survival Analysis?
The problem statement of survival analysis is quite similar to regression problem. A regression model can be built considering failure time (i.e. time elapsed from present to the actual churn event) which can be marked as target variable. That can still solve the problem by giving the predicted time of the next event, but it's compounded by uncertainity of exact churn time, i.e. censoring, hence Regression may give poor result.
Another reason is the distribution of time to event. If the failure time is normally distributed, we still could use a regression (or logistic regression model), but that is not the case. Distribution of time is either unknown or not normal at all.

## Pre-requisite for Survival analysis
1. Chances of Survival always decrease over time
2. Exact time of events are unknown or censored
3. High sensitivity about the uncertainty of actual event timings.


## Estimating Survival Distribution
Survival distribution is nothing but a probability distribution. Estimation of probability distribution can be modeled using either parametric or non-parametric approach.
- Parametric approach goes with a strong assumption and uses pre-defined standard probability distribution Survival function can be derived from density function. Standard probability distributions such as exponential, Weibull, Gumbel, etc. are good candidates for parametric density functions.
- Non-parametric approach - none of the pre-defined distributions are used. Rather, a custom estimator is built from the dataset, examples - Kaplan-Meier estimator.

## Survival Modeling
Dependent Variable: Tenure
Censoring Variable: Churned
Optimal distribution: Non-parametric Cox-PH Model

## Key features present in dataset
1. Customers who left the organization – Churn
2. Services that each customer has signed-up for – phone, multiple lines, internet, online security, online backup, device protection, tech support, and streaming TV and movies
3. Customer's account information – how long they’ve been a customer, contract, payment method, paperless billing, monthly charges, and total charges
4. Demographic info about customers – gender, age range, and if they have partners and dependents
