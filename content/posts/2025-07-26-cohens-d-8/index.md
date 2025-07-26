---
title: "If researchers find Cohen's d = 8, no they didn't"
layout: single
date: "2025-07-26"
sitemap: true
---

I've spent a lot of time thinking about the plausibility of standardized effect sizes in the last year. From a trustworthiness assessment perspective, (standardized) effect sizes have a great combination of being commonly reported, easy to look into, having values that are range in their plausibility, and - when they go wrong - being at least somewhat diagnostic of other things having also gone wrong. 

They are in the top left corner which makes them Cool and Good. For these reasons, they are useful to include in our critical thinking when reading any article or, more formally, as part of a Trustworthiness Assessment (e.g., using [Wilkinson et al.'s (2025) INSPECT-SR](https://www.medrxiv.org/content/10.1101/2024.11.25.24316905v3) tool).

<br>

![](conjoined_triangles_of_trust.png)

<br>

In this post, I focus on Cohen's *d* standardized mean difference effect sizes.

So, how large an effect size should make us balk? 

On the one hand, and let's get this out of the way nice and quickly: nuance is needed, fields differ, etc. Psychophysics, for one, defies the norms of other fields because their effects are legitimately huge. 

On the other hand, literally no-one is proposing that effect sizes beyond a specific cut-off be used to send you to Science Naughtiness Jail. Rather, the question is what rules of thumb might be useful heuristics for readers to think about the credibility of the work they read. 

One useful starting point is to have an intuition for norms in the literature. Bogdan (2025)](https://doi.org/10.1177/25152459251323480) scraped data from 173,926 psychology articles published between 2004 and 2024 and extracted p values and effect size metrics. His article is worth a read. Further analysis of that data set can tell us lots about the distribution of Cohen's *d* effect sizes in the psychology literature as a whole. 

I extracted 23,089 Cohen's *d* effect sizes that were explicitly reported in text (e.g., "Cohen's *d* = 0.21"). It can also be estimated from *t*-tests' degrees of freedom and *t* values, akin to how statcheck also recomputes *p*-values from these ([Nuijten et al., 2016](10.3758/s13428-015-0664-2)). For the sake of simplicity, let's assume all t-tests are independent rather than dependent, as the Cohen's *d* calculation differs slightly between them although it doesn't change the distribution very much.

<br>

![](bogdan_cohens_d.png)

<br>

The right tail of these distributions is very long, so I take only the 0-99th percentiles. 

Or in percentiles:

<br>

| Percentile | \|$d$\| | \|$d_s$\| estimated from *t* test |
| ---------- | ------- | --------------------------------- |
| 1          | 0.02    | 0.02                              |
| 5          | 0.07    | 0.09                              |
| 10         | 0.13    | 0.17                              |
| 25         | 0.29    | 0.36                              |
| 50         | 0.56    | 0.71                              |
| 75         | 1.01    | 1.34                              |
| 90         | 1.61    | 2.4                               |
| 95         | 2.3     | 3.4                               |
| 99         | 7.14    | 7.48                              |

<br>

Half of all explicitly reported Cohen's *d* values are less than .56. Once you're seeing Cohen's *d*s of 2 you are in the top 10%-ish of effect sizes - and indeed the sort of effects that generate them. 

Again, before anyone gets angry, I acknowledge that this doesn't differentiate between what is generating these effect sizes of course, which could range from population level interventions (which might have small effect sizes but be meaningful) to manipulation checks (which are often necessarily large, e.g., are these positive words more positive than these negative words). Caveat emptor, use your brain, etc. It could be broken down by subfield etc but that's beyond the scope of this post (see also [Glaser et al., 2023](https://osf.io/h368x)).

My emerging personal rule of thumb is that Cohen's *d* > 2 are often questionably plausible and invite more thought, and Cohen's *d* > 4 or 5 is *usually* borderline silly for things other than manipulation checks or positive controls ([Hilgard, 2021](https://doi.org/10.1016/j.jesp.2020.104082)).

This isn't to say that very large Cohen's *d* values of 5 or so can't occur; they can but they require a combination of very little variance within conditions and very large differences between conditions (i.e., the definition of Cohen's *d*). 

### Where you might see Cohen's *d* > 4 or 5

What sort of things produce Cohen's *d* values of 4 or 5 and are plausible? 

- "Chocolates are more desirable than human poop": Cohen's *d* = 4.52 (Balcetis & Dunning, 2009).
- "Eating pretzels makes you thirstier than drinking water does": Cohen's d = 4.69 (Balcetis & Dunning, 2009).
- Children tend to state that "boys tend to wear skirts more often than girls tend to wear skirts" (Streck & Kessels, 2024, unpublished poster presentation).

Although, as a quick aside, I have questions about even these effects, and am slowly working to replicate them and other some maximal positive control studies like this (see also [Hilgard, 2021](https://doi.org/10.1016/j.jesp.2020.104082)).

### Where you should probably not see Cohen's *d* > 4 or 5

Conversely, there are contexts where we can say that it is relatively unlikely that we should observe very large Cohen's *d* values, such as Cohen's *d* = 8.0. One example would be RCTs on psychotherapy, given that we have lots and lots of information about effect sizes in that area (e.g., [Cuijpers et al., 2024](https://doi.org/10.1002/wps.21203)). Perhaps especially in clients who did not respond to prior treatments because, who may be more treatment resistant (although, for an excellent statistical critique of this common clinical assumption see [Senn, 2004](https://doi.org/10.1136/bmj.329.7472.966)). Perhaps especially at one-year follow up, given that demonstrating sustained improvement is always challenging.  

And yet, we can find such a effect in [Gloster et al.'s (2020)](https://doi.org/10.1016/j.cpr.2019.101810) meta-analysis of psychotherapy in for previous treatment non-res ponders. In that article, for unclear reasons, the authors censor Cohen's *d* values above 1, so their magnitude is not fully apparent from the forest plot. To make this clearer, I (successfully) reproduced the forest plot for efficacy at follow-up they presented in Figure 5.

<br>

![](gloster_fig_5_fu_recreated.png)

<br>

Whew. This is either one of the most effective psychotherapy interventions that has ever been created, or something is amiss. The ability to spot this and think "hmm that doesn't look right" is a skill I think we should be training.

Equally, the meta-analysis for efficacy at the post-treatment time-point (their Figure 2) also contains some implausible or even impossible effect sizes:

<br>

![](gloster_fig_2_posttreatment_recreated.png)

<br>

On the one hand, I do believe there are contexts in which scientists should be able to quickly and efficiently point out "that's not true" without endless hand-wringing (see my other post [here](https://mmmdata.io/posts/2025/07/critique-does-not-require-solution/)). 

On the other hand, when trying to convince readers of the utility of looking into the plausibility of the magnitude of effect sizes, it's helpful to bring receipts that these effect sizes are indeed erroneous or untrustworthy. It's therefore important to note that these very large effect sizes cannot be correctly reproduced from the results reported in the original articles. 

In the case of Isasi et al. (2010), Gloster et al. (2020) appear to have made the "Standard Error error" here of confusing Standard Deviation and Standard Error, which inflates effect size. See various examples, commentary and study of this by [Maassen et al., 2020](https://doi.org/10.1371/journal.pone.0233107); tweets by [Charlton, 2022](https://x.com/AaronCharlton/status/1478927020528750594), statistical notes by [Altman & Bland, 2005](https://doi.org/10.1136/bmj.331.7521.903), and others. In the case of Moore and Blackwell (1997), it's unclear how Gloster et al. (2020) reached Cohen'd *d* = 1.65 as the original article reports *d* = -0.08. You can read more about the specifics of these issues in Gloster et al. (2020) in [this pubpeer comment](https://pubpeer.com/publications/B894E24B78C656FA21941142971CDE) or [this preprint (Hussey, 2025)](https://osf.io/preprints/psyarxiv/rbydj). 

