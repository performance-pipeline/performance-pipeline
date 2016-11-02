---
layout: page
title: The Performance Pipeline
permalink: /
---

Performance is a critical cornerstone of a successful application running in a production environment, just like quality and security. In order to make performance testing a first class citizen, that you must consider it during every phase of your application lifecycle. Of course you need to look for different types of issues at the various stages of your application lifecycle, as you would with quality testing, for example. Thinking about performance during every stage of your application lifecycle is core to the performance pipeline concept.


Let’s first look quickly at how we have changed our view on QA testing over the years. Not so long ago, quality testing was seen as an overhead that was be contained only if time permitted at the end of your application lifecycle. QA is now a first class citizen that you wouldn’t dream of omitting at every stage of our application lifecycle. For example, writing development code without unit tests is largely accepted as a terrible practice. Many don’t consider a user story to be complete without some level of quality testing first. Good QA throughout your application lifecycle is considered key to the application’s success in production. Ensuring quality throughout the application lifecycle means adding unit tests during development, automated regression tests during CI, integration and system testing, all the way up to our smoke tests which you run in production.


So, what about performance? How can you fit performance in our application lifecycle? When you think of traditional performance testing, you probably think about long running, load and stress tests in a production-like environment towards the end of your application lifecycle. But we can do better than this, by bringing our testing efforts forward and earlier on in the application lifecycle. At the earlier phases, bugs are easier, cheaper and much more convenient to fix. It has been shown that developers are the people who will ultimately fix performance bugs wherever they’re found in a release, so it makes sense to have them fix as many of these issues while they’re being introduced to the codebase or better still, before!


The performance pipeline focuses on performance at every stage of our application lifecycle. However, you need to be smart about what can be achieved at each stage. For example, you don’t want to chase down milliseconds during our development phase, as our production environment will likely be considerably different. Let’s explore what you should think about and test at every stage of our application lifecycle.

