---
layout: page
title: Development
permalink: /development/
---
<a href="https://github.com/performance-pipeline/performance-pipeline.github.io"><img style="position: absolute; top: 0; left: 0; border: 0;" src="https://camo.githubusercontent.com/121cd7cbdc3e4855075ea8b558508b91ac463ac2/68747470733a2f2f73332e616d617a6f6e6177732e636f6d2f6769746875622f726962626f6e732f666f726b6d655f6c6566745f677265656e5f3030373230302e706e67" alt="Fork me on GitHub" data-canonical-src="https://s3.amazonaws.com/github/ribbons/forkme_left_green_007200.png"></a>

![performance-pipeline-image]({{ site.baseurl }}/images/performance-pipeline-development.png "The Performance Pipeline - Development Phase")

The development phase is the first time you get to quantifiably test code that could make it into production. The important question is, what should you be testing and what shouldn’t you be testing in this phase? It’s important to appreciate that the test environment that you run in development will have major differences from a production deployment. If you’re not strategic with what and how you test, you could find yourselves wasting time by testing without accurate data. For instance, performing tests such as stress or load testing too early may result in false bottlenecks existing in an area of your application that simply doesn’t appear in production. Let’s look at the types of issues that you can test for during development:

**Inefficient Application Code**

You should know where you’re spending most of your time within application requests. Note that there’s no need to dig too deep at this stage as you’ll be working from development specific data. You wouldn’t paint a wall before it’s plastered, but you would do everything you can to make sure it’s flat before you plaster. Look for where you’re spending most of your relative time at this stage. If one method is taking 500% more time than the others, investigate it to see if there are ways to understand why, and fix if possible. Common code smells like poor use of APIs, resource contention or invoking unnecessary code etc tend to be easier to fix earlier and are most noticeable during development.

**Inefficient Database Access**

Database access is a prime suspect for poorly performing code. Often IO queries are simply too slow. Sometimes application code can be creating more queries than is necessary. The queries may all individually be reasonably, but looking at the bigger picture, your data fetching strategy could be too lazy or eager than what the user experience should demand. It’s prudent to understand how much time you’re spending in the database, but again be wary of the development to production differences in your configuration and data. It’s far nicer to fix database access issues in simpler development scenarios, rather than finding them due to load or stress testing further down the line.

**Concurrency Bugs**

When making decisions as simple as which collection to use to store data, it’s important to understand how concurrency will affect your choices. How is the class you’re writing going to be accessed by users? Make sure if there’s even a chance that your class could have concurrency concerns, which is likely, write defensive code with concurrency in mind. 

**Oversized Session Data**

Session Data can easily grow out of control, without much of an impact to the single user in your development environment. However, when your application is scaled, large sessions can cause severe issues if you’re in a production environment with limited resources. If your production environment is more capable, you’ll just be left with a clumsier, slower application if you tend to  manipulate the session data. 

**Code Reviews**

A cheap place to be retrospective on your code is during code reviews. It’s not unusual for developers to focus more on the functional aspects of code during a code review. However it’s very important that the aspects mentioned above are thought about during a code review as well to help prevent performance bugs slipping into the next phase, making them more expensive to fix.

_**Take aways**_
- _**Databases and inefficient code** are the most likely areas for performance issues._
  - _Check your IO queries are fast and few._
- _Understand where your application is spending its time._
- _Think about **performance in code reviews**. Consider the performance implications of code changes._

Next Stage: [Test]({{ site.baseurl }}/test)