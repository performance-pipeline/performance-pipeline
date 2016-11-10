---
layout: page
title: Test
permalink: /test/
---
<a href="https://github.com/performance-pipeline/performance-pipeline.github.io"><img style="position: absolute; top: 0; left: 0; border: 0;" src="https://camo.githubusercontent.com/121cd7cbdc3e4855075ea8b558508b91ac463ac2/68747470733a2f2f73332e616d617a6f6e6177732e636f6d2f6769746875622f726962626f6e732f666f726b6d655f6c6566745f677265656e5f3030373230302e706e67" alt="Fork me on GitHub" data-canonical-src="https://s3.amazonaws.com/github/ribbons/forkme_left_green_007200.png"></a>

![performance-pipeline-image]({{ site.baseurl }}/images/performance-pipeline-test.png "The Performance Pipeline - Test Phase")

As we get closer to production our testing will get more involved. The three main areas of testing is automated test suites during CI, traditional performance load/stress testing in system test and production-like testing during staging. Let’s look at each of these to understand how we can performance test at each stage.

### Continuous Integration testing.

There are a couple of approaches in which you can include performance at this stage:
- Use your existing tests suites
  - It’s common to have amassed a large number of functional tests which run on each build during CI. Reuse these tests by monitoring the key interactions. These can include the database or back end interactions (both quantity and duration) as well as duration of test times.

- Track your build regressions
  - Finding quality regressions is easy. When your functionality works, your tests pass. When a bug is introduced, your tests immediately turn red and your build fails. Consider the same consequences when you hit a performance regression. When there are significant differences between the performance behaviours of two recent builds, investigate the changes between two builds, understand the code differences and determine if such a performance increase is warranted, based on the new behaviour.

### System Testing & Staging

During staging, more robust performance testing can be performed as you’re now in a cloned production environment, or as close as you can be. You will want to start generating some synthesized load on your application as the resulting metrics will be closer to real-world results. First, you should establish baselines which you will then set as your target. There are a number of different ways to synthesize load on your applications to test application response time, system response time, load bearing capacities and sustained runtime behavior.

**Load Testing**

Load testing helps you establish your benchmark. Configure a predetermined amount of load that should be expected with the “normal” amount of traffic. Stable runtime conditions should be reached here, so be well-informed and realistic in determining what the baseline standard will be. 

**Stress Testing**

Stress testing follows closely behind load testing. Run a higher than expected load against the system to identify how much the system can take before it fails. You’ll want to make sure there is a considerable margin here, but less obviously, the goal isn’t necessarily to reach a scalability nirvana as errors are expected. More importantly, identify the failure point to increase the predictability of your releases and establish a point of reference for when a higher amount of traffic is expected, such as during special campaigns. 

**Spike Testing**

Spike testing lets you see the system’s response to a sharp increase in traffic. This is a good chance to see how quickly a node can spin up in your high availability cluster, or how quickly your failover cluster responds. You can test to make sure your application recovers from periods of heavy load and to see how long your application is affected after a short burst in traffic.

**Soak Testing**

Soak testing helps you measure the endurance of your application under load over a significant period of time. This helps to reveal issues like memory leaks and backed up queues. The goal is to make sure the throughput and response times do not decline.

To pair with the synthetic workloads, now is a good time to examine metrics that span a wider scope outside of your application, such as, heap, garbage collector activity, CPU hotspots and threads. Monitor your application to not only reveal holes in the ecosystem or application that need optimizing; when thinking in a performance-centric manner, you’ll use these metrics to track and prevent any form of performance degradation, even if minor. Keep in mind that a few extra milliseconds in response times can have a business impact.

### Staging

There are many aspects to ensuring that your staging environment is equivalent to your production environment, including mirroring hardware and software. Consider replaying production load on your staging environments, if you find that synthesized load is not providing you with reliable results. Also, try to make your data as production like as you can make it, if you cannot mirror your production data exactly.

_**Take aways**_
- _Use your **existing automated test suites** to measure regressions across builds during Continuous Integration environments._
- _When testing load and stress tests, always **take baselines** that you can **measure** against and use for **comparison**. Use varieties of load, stress, spike and soak testing to find different issues._
- _Consider **replaying production traffic** in your staging environment for a closer real life representation of production than just synthesized load._

Next Stage: [Production]({{ site.baseurl }}/production)