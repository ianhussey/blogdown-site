---
layout: single
title: "GitHub version control software for psychologists"
sitemap: true
date: 2015-10-16
---

Perhaps it's just my own learning curve, but it feels like internet resources are making it easier and easier to conduct and communicate research. [LimeSurvey](http://www.limesurvey.org) does away with the need for paper questionnaires, [PsychoPy](http://www.psychopy.org) allows me to write training and testing procedures in a matter of hours, [Google docs](http://docs.google.com) allows me to write  collaboratively, [Zotero](http://www.zotero.org) references the manuscripts for me, [Recite](http://reciteworks.com/) checks them for errors, [ResearchGate](https://www.researchgate.net/profile/Ian_Hussey) takes care of distribution, and [Dropbox](https://www.dropbox.com) covers my ass incase anything goes wrong.

Nonetheless, there were two gaping holes left in my workflow:

# 1 Version control

As shameful as it is to admit, whenever I am coding a new task in PsychoPy I have an endless number of zip files lying around my hard drive. Files are often interdependent, so in order to 'crystalize' a given version I find myself zipping folders multiple times a day. To all real programmers out there: I'm sorry.  

# 2 Code distribution and citation

At least in psychology, there is still a huge disjoint between the procedures we report and the implementations of these procedures that we actually use. For example, I might report in a given manuscript that I used "an IAT" (a procedure), but it's often less clear which program or versions (i.e., implementations) I actually used to effect this. Importantly, we unfortunately cannot assume that the description of a procedure and its implementations are identical, or that all implementations are created equal. The only way to make this process transparent (and therefore replicable) is to make all research materials available. In the past, I've relied on distributing compiled programs (e.g., the IRAP.exe file), but there is an obvious need to distribute source code itself too. 

Of course, the solution to both of the above is version control software - the "track changes" of programming. I've known about the most popular and accessible one, [GitHub](http://github.io), for quite a while, but have only just got on the bandwagon. Of course, version control goes well beyond track changes: not only does it keep track of what has been changed and allow those changes to be undone, but it also allows for different versions of a project to be created, worked on, and then later reintegrated into the main project. Because the repositories in which projects are held can be made public, this also allows for both distribution and collaboration without requiring communication. 

There are many [great guides](https://guides.github.com/activities/hello-world/) on getting started with GitHub.

It's also worth noting that Brian Nosek's [Open Science Framework](https://osf.io) allows for GitHub integration, thereby allowing you to make all research materials available in one place. For the moment, I plan on making many of my coding projects (e.g., testing tasks, training tasks, plotting scripts) available on my [public GitHub](https://github.com/ianhussey). This website is also hosted on my GitHub ([thanks to this guide](http://jmcglone.com/guides/github-pages/)), in order to provide a simple way to access projects that are ready for wider use.