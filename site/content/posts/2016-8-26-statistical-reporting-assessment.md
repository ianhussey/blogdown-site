---
layout: single
title: "Statistical Reporting Assessment"
sitemap: true
date: 2016-8-26
---

Even if your data and code are publicly available, you can still fall at the last hurdle by not reporting the correct numbers in a manuscript. Luckily, the [`statcheck`](http://rpubs.com/michelenuijten/202816) library can check this for you. 

Specifically, it:

1. extracts all the analyses reported in your manuscript
2. takes the test statistics and df and recomputes p values
3. compares the recomputed p value with the p value reported in the manuscript to check for reporting errors, and also for APA compliance.

This can also be very useful when peer reviewing others' manuscripts! `statcheck` provides an option to read `.pdf` files, although this requires XPDF, which I've found tricky to get installed correctly on Mac.

Download the [current release](https://github.com/ianhussey/StatisticalReportingAssessment/releases/) or check out the [project page](https://github.com/ianhussey/StatisticalReportingAssessment/) if you'd like to see the most recent code or contribute to the project.  