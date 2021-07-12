---
title: Hello, World!
author: admin
date: '2020-05-11'
slug: hello-world
categories:
  - web
  - career
tags:
  - web
subtitle: ''
summary: ''
authors: []
lastmod: '2020-05-11T13:17:21+01:00'
featured: yes
image:
  caption: ''
  focal_point: ''
  preview_only: no
projects: []
---

"Hello, World!" the traditional output of many a first computer programme. This was supposed to be my first blog entry and yet it's much easier to write about the installation process, so it is really my second!

I've built this website to serve a couple of purposes:  
  * Document my Data Science journey
	* Share my projects & ideas
	* Career musings as I try and forge a path that integrates my clinical experience to date with my developing interests in the Data Science world
	* Refresh my web development skills and practice writing in Markdown

..and perhaps a bit of **shameless self-promotion** too!

This decision was motivated by two unknowing individuals:

[Dr Danny Wong](https://dannyjnwong.github.io/) an Anaesthetist & Data Science Researcher who was one of my original inspirations to explore Data Science. What surprised me was when I stumbled across his blog whilst googling solutions for [Replacing values in a column with dplyr using logical statements](https://dannyjnwong.github.io/Replacing-values-in-a-column-with-dplyr-using-logical-statements/) [^1]. I realised that a blog could be a method of not only sharing one's work, but also documenting the learning *process*.

[Ben Kinnard](https://www.linkedin.com/in/benjaminkinnard/) an old school friend who gave up a successful career in Wealth Management to re-train as a Software Developer and posted ["Why blog in 2020?"](https://holfolioben.com/misc/2020/01/01/why-blog-in-2020.html). A lot of this sounded familiar, particularly *"trying too hard to sound impressive"* as a barrier to trying at all. Again there was the concept of a blog as a personal journal.

So here we are! Wish me luck!  
  
  
  

#### Footnotes
[^1] In the end I used a different solution to replace character strings for exponents with their corresponding order of magnitude. 
`data <- data %>% mutate(PROPDMGEXP = case_when(PROPDMGEXP == "K" ~ 1E3, PROPDMGEXP == "M" ~ 1E6))`
This was for the final assignment of the Reproducible Research course from Johns Hopkins and my [solution can be found on RPubs](https://rpubs.com/tomlincr/JHU-Storm-Assignment).
