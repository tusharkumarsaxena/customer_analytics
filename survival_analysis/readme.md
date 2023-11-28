Terminology
- Survival analysis is defined as a collection of statistical longitudinal data analysis techniques where time is a major factor.
- Events - survival analysis deals with the events related to failure. Definition of failure must be clear.
- Subject - represents the entity which is going through some phases and the failure (or the event) is attached to it.
- Failure time or Survival time - time taken till failure is referred to as the failure time or survival time.
- Survival Function - it returns the probability of an event occurring after time t. Mathematically, S(t) = P(T > t), 0 < t < infinity.
    S(t) gives the probability of a subject surviving after time t. S(t) is nothing but a probability distribution over time. 
    Theoretically, t ranges from 0 to infinity, S(t) will have values from 0 to 1. Ideally, survival function is represented by a decreasing smooth curve which begins at S(t) = 1 at t = 0.
![Survival Curve](https://github.com/tusharkumarsaxena/customer_analytics/blob/main/survival_analysis/images/Survival%20Function%20Curve.PNG)
