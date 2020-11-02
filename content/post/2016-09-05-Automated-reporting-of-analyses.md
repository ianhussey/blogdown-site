---
layout: single
title: "Automated reporting of statistical analyses"
sitemap: true
date: 2015-09-05
---

If you were trained on SPSS you're probably accustomed to the idea that running and analysis and reporting an analysis are entirely seperate stages in writing a paper. However, it doesn't have to be so.

The results returned by most stats packages have the important data spread out over a number of different tables. This always seemed inefficient to me, given that a huge proportion of users are all looking to produce APA styled output at the end of the day.

A recent paper demonstrated that this idea might not just be driven by my laziness: an analysis of 250,000 published psychology papers suggests that roughly 50% included at least one p value that was inconsistent with its reported test statistic and degrees of freedom. More worryingly, in 12.5% of cases, the inconsitency was large enough to imply that the significance of the test may have been misreported or misinterpreted (Nuijten, Hartgerink, van Assen, Epskamp, & Wicherts, 2015).

Automating this step between running tests and reporting results would therefore seem to be a logical step. Packages such as ezANOVA and schoRsch can already do a lot of this for you by returning APA styled results, e.g., `"F(1, 28) = 3.21, p = .02, n2p = .05"`. This can have accuracy benefits, and could also provide additionally strict pre-registration criteria if so desired. For example, one could script key parts of a results section to be automatically written before data is collected. 

I've written some scripts to complete this generation by also reporting the test setup, descriptive statistics, the interpretation of the effect size and the test of the null hypothesis. For example, 

`"An independent t test demonstrated significant differences of medium effect size between condition A (n = 52, M = 0.11, SD = 0.33) and condition B (n = 48, M = -0.1, SD = 0.35), t(96.77) = 3.07, p = 0.003, d = 0.61, 95% CI [0.2, 1.03]."`

I've included the following tests for now:

- Independent t test (Welch).
- 2X2 mixed within-between ANOVA (for between groups pre-post designs).
- ANCOVA with single covariate (time point 2 as DV, condition as IV, time point 1 as covariate: for between groups pre-post designs).
- Bayesian BEST test (Kruschke, 2013), a Bayesian alternative to the independent t test.

You can get the code [here](https://github.com/ianhussey/AutomatedReporting).

You can also check reporting results post hoc using statscheck, see [here](https://github.com/ianhussey/StatisticalReportingAssessment) for a working implementation. This can be useful for checking manuscripts before submission, or within a peer review, or post publication, etc.



