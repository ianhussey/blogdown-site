---
layout: single
title: "Linear mixed effects models"
sitemap: true
date: 2017-07-14
---

Most experiments using reaction time data separate scoring and analysis. That is, the study captures a large number of reaction times for each participant, then reduces this down to a smaller number of metrics (e.g., mean reaction time, *D* scores, etc), and then analyses these metrics. In doing so, we can throw away the variance associated with each participant's performance and unnecessarily decrease the power of our analysis. 

Mixed effects modelling provides an accessible alternative that does away with data scoring. These include the "fixed" effects that people are accustomed to in traditional ANOVAs and also "random" effects that can vary between participants in unknown ways. For example, a typical (fixed effects) ANOVA model might take the following general form:

```{r}
Mean_RT ~ block * condition
```

Note that it requires you to calculate mean reaction times before analysis, and that the variance around each participant's mean is not modeled. As such, no distinction is made between two participants both with a Mean_RT of 1000ms where one has an SD of 100ms and the other 900ms. 

We might want to instead include all the reaction time data (perhaps trimming outliers). However, to do so, our model would have to acknowledge the non-independence of the multiple reaction times provided by each participant. To do this, we can include a random regression intercept for participant in a mixed effects model:

```{r}
RT ~ block * condition + (1 | participant)
```

We could also go further and acknowledge that the between block effect likely differs in magnitude between participants and not just between conditions. This might be the case for a task such as the Implicit Association Test. 

```{r}
RT ~ block * condition + (block | participant)
```

A model like this provides a reasonable way to analyse data from a mixed within-between factorial design, such as a between groups IAT study. 

An annotated implementation of this model in R, along with example data, can be found in my post [here](http://mmmdata.io/linear_mixed_effects_models).



