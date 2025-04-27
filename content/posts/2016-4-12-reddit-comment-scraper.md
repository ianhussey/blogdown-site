---
layout: single
title: "Reddit comment scraper"
sitemap: true
date: 2016-08-16
---

Experimental-clinical psychologists have finally started to capitalise on naturalistic internet data sources for research. For example, recent papers using data from the social news aggregator [Reddit](http://www.reddit.com) (e.g., [Hipp et al., 2015](http://psycnet.apa.org/?&fa=main.doiLanding&doi=10.1037/a0039998)), and the social networking site [Tumblr](http://www.tumblr.com) (e.g., [Cavazos-Rehg et al., 2016](http://econtent.hogrefe.com/doi/abs/10.1027/0227-5910/a000409)).

The AskReddit subreddit is a particularly useful source. Here, hundreds or thousands of people provide answers to single questions. In many cases these data may be difficult to come by through other means. For example, Hipp et al. (2015) "scraped" data from a thread asking rapists what their motivations were and whether they regretted it or not.

Luckily, Reddit provides access to their data freely through their [API](https://www.reddit.com/dev/api/), and several libraries have been written to make accessing data via the API extremely easy. 

I've used [PRAW](https://github.com/praw-dev/praw), an API wrapper written in Python, to write a script that allows researchers to easily emulate Hipp et al.'s data acquisition methodology. It scrapes all comments from a given thread and saves the object as a Python pickle, and then selects only the first-level comments and saves the contents of the comment as a `.csv` file. You can then feed this into your qualitative or quantitative analysis of choice. For example, a [sentiment analysis](https://en.wikipedia.org/wiki/Sentiment_analysis) via [TidyText](https://github.com/juliasilge/tidytext) in R.   

Download the [current release](https://github.com/ianhussey/RedditCommentScraper/releases/) or check out the [project page](https://github.com/ianhussey/RedditCommentScraper/) if you'd like to see the most recent code or contribute to the project.  