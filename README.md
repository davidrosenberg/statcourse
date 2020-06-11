# Practical Statistics for Data Scientists
Just a placeholder for some ideas for a statistics class, at about the same level and with the same practical motivations as [DSGA 1003](https://github.com/davidrosenberg/mlcourse).

# Course Pitch
This course is largely about three main topics: parameter estimation, hypothesis testing, and confidence intervals.  We'll be discussing both classical and modern frequentist methods, as well as Bayesian analogues of these problems.  While we have theorems guaranteeing performance of many of these methods under certain assumptions, we want to gain intuition on how things work in a wide variety of situations, including when the theorem assumptions don't hold.  To this end, we'll spend a fair bit of time discussing ways to evaluate procedures empirically and developing our testbed to do so.  On the one hand we hope to get a visceral feel for the meaning of theorems by extensive illustration through simulation, and at the same time get an intuitive sense for what changes when the theorems don't apply.  Moreover, we'll gain experience in evaluating procedures in scenarios where we don't have any relevant theorems to guide us.  Once we have a firm foundation in performance evaluation, we'll follow a selection of the most interesting and practical methods from classical and modern statistics, comparing all of them through their performance on our testbed. 

# Topics
## Hypothesis Testing by Simulation
## Anomaly Detection / Powering a Test
- And what's the deal with [one-tailed vs two-tailed tests](https://stats.idre.ucla.edu/other/mult-pkg/faq/general/faq-what-are-the-differences-between-one-tailed-and-two-tailed-tests/)?
- Suppose we fix the maximum acceptable false alarm rate (i.e. Type 1 error) go some level, say 5%.
- And suppose our sample space is X, and our null hypothesis is some distribution P on X.
- So what we can do is to select any subset of X that has probability 0.05 under P.
- This will be our rejection region. If our observation falls in this region,
  we'll reject the null hypothesis. We'll have detected an anomaly.
- If P is true, then we are only rejecting 5% of the time.  So this method respects are maximum false alarm rate (our Type 1 error).
- But there are no other restrictions on how choose our rejection region.
- This is where things get interesting.
- We can 'focus the power' of our test (i.e our rejection region) in a particular area of the sample space (corresponding to particular types of deviations from the null hypothesis), or we can spread it around as "evenly" as possible to try to cover all possible deviations from the null hypothesis.
- For the standard example of [one-tailed vs two-tailed tests](https://stats.idre.ucla.edu/other/mult-pkg/faq/general/faq-what-are-the-differences-between-one-tailed-and-two-tailed-tests/), the two-tailed test is able to detect means that are either too high or too low, while the one-tailed test focuses on just one type of deviation, say too high.  For the same false alarm rate, the one-tailed test can detect smaller deviations from mean 0, but it will only detect means that are too high, and will not detect means that are too low.
- This difference doesn't seem that exciting in one dimension, but in higher dimensions, it becomes increasingly helpful to have a particular set of "alternative hypotheses" that you want to focus your attention on detecting.  
- Bring in the term power...

## Bandits vs A/B Testing
- [Google's Bandit FAQ](https://support.google.com/analytics/answer/2847021?hl=en&ref_topic=2844866)

## Mixed Effects Models
- What are they used for?  How do they unify various statistical approaches to generalized linear modeling?
- What are they mathematically?  How do they relate to regularized linear regression and empirical Bayes linear regression?

## Other resources
- http://www.statslab.cam.ac.uk/Dept/People/djsteaching/teaching17.html
