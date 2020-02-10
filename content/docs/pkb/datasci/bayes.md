---
Title: "Bayes"
---

# Bayes Theorem

#### Resources

{{< youtube BrK7X_XlGB8 >}}

[BetterExplained](https://betterexplained.com/articles/an-intuitive-and-short-explanation-of-bayes-theorem/)

[Calculator](https://stattrek.com/online-calculator/bayes-rule-calculator.aspx)

## Bayesian Networks

[Visualisation Tool](http://www.cs.man.ac.uk/~gbrown/bayes_nets/)

---

https://www.youtube.com/playlist?list=PLwJRxp3blEvZ8AKMXOy0fc0cqT61GsKCG

https://blog.dominodatalab.com/using-bayesian-methods-to-clean-up-human-labels/

Think about how to create data so that it's useful for modeling
    Don't just take anything for granted and start modeling straight away
Graphical models are not as hard as they used to be


X variable = features, predictors, parameterization
Y variable = labeled data for predictions
    These can be icky, consider standardised testing:
        Correctness of discrimination parameter (telling difference between who knows right and wrong); guessing parameter in multiple choice. Aggregates of these issues...
    Bayes Net - graph of dependency relationships encoding probability of event vs real occurrences
    Generative models are 'joint distributions over x's and y's'.
        The Bayesian posterior function is looking for an estimate which is the /mean/ over all possible ways we can parametrize our model.
    Stanislaw Ulam
    Gaussian stuff
Using one set of annotations and 'contextualising it' with Bayesian methods over X & Y allows conversion into labels which are mean of all sensible labels.
