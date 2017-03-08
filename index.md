---
layout: page
title:
permalink: /
---
<a href="https://github.com/performance-pipeline/performance-pipeline.github.io"><img style="position: absolute; top: 0; left: 0; border: 0;" src="https://camo.githubusercontent.com/121cd7cbdc3e4855075ea8b558508b91ac463ac2/68747470733a2f2f73332e616d617a6f6e6177732e636f6d2f6769746875622f726962626f6e732f666f726b6d655f6c6566745f677265656e5f3030373230302e706e67" alt="Fork me on GitHub" data-canonical-src="https://s3.amazonaws.com/github/ribbons/forkme_left_green_007200.png"></a>

![performance-pipeline-logo]({{ site.baseurl }}/images/performance-pipeline-logo-color.png "The Performance Pipeline")

## Introduction

Improving the performance of your application is an investment. If you tolerate poor application performance, you’re accepting loss of revenue and upset or lost users to competitors and more. To make performance a priority, you need to give it the necessary attention during every release. We already know testing is cheaper and easier to perform when it’s done early. If not found early on, performance issues would be more complex and time consuming to diagnose and fix.

In practice, Quality Assurance (QA) testing is more proficient at the *testing early* mindset. Different QA tools and processes are used to find different types of issues at each stage of the application lifecycle. This ensures that the end product is properly tested and more likely to have fewer QA issues. The equivalent process for performance, is the **Performance Pipeline**, a strategy that focuses on performance at every stage of your application lifecycle.

## The Performance Pipeline

When you think of traditional performance testing, many will think about long running, load and stress tests in a production-like environment that is only run towards the end of your application lifecycle. However, there are many other types of performance tests that can be run at every stage of the application lifecycle, rather than just at the later stages. By testing in earlier phases, bugs are easier, cheaper and much more convenient to fix, using simpler use cases.

![performance-pipeline-image]({{ site.baseurl }}/images/performance-pipeline.png "The Performance Pipeline")

The performance pipeline focuses on performance at every stage of our application lifecycle. However, you need to be smart about what can be achieved at each stage. For example, chasing milliseconds during development isn’t effective, as our production environment will be considerably different. Let’s explore what you should think about and test at every stage of the application lifecycle.

## The Pipeline Phases

The five phases of the performance pipeline are as follows: Requirements Analysis, Design, Development, Test, and Production. You should be focused on the performance of your application at every one of these phases.

## [Requirements Analysis]({{ site.baseurl }}/requirements-analysis/)

Non-functional requirements, including performance requirements must be added to your project at the same time as your functional requirements. During this first stage you should state clear demands that you expect from your finished project. These demands must be considered in all subsequent phases of the pipeline. There’s no such thing as a project or functional requirement not having a performance requirement. Make sure your performance requirements are measurable, and precise, by avoiding such language such as “all” and “every”. Try to be explicit with your requirements. [More...]({{ site.baseurl }}/requirements-analysis/)

## [Design]({{ site.baseurl }}/design/)

Don’t use architectures and designs that prevent you achieving your performance requirements. Prototyping can give you confidence that your design meets your expectations. Database interactions are expensive. Make sure you only go there when you need to, and batch requests where possible. If you intend to use third party endpoints, make sure they can guarantee the requirements you have. [More...]({{ site.baseurl }}/design/)

## [Development]({{ site.baseurl }}/development/)

Databases and inefficient code are the most likely areas for performance issues.  Be aware of how many interactions with the database your code is making, how long they’re taking, whether you’re getting too much or not enough data etc. Understand where your code is spending most of its time in the request and whether that’s reasonable at this stage. Consider the performance implications of code changes during your code reviews and consider them as important as functional errors. [More...]({{ site.baseurl }}/development/)

## [Test]({{ site.baseurl }}/test/)

The test phase ranges from Continuous Integration activities through to staging. Use your existing automated test suites to measure regressions across builds during Continuous Integration environments. When running load and stress tests, always take baselines that you can measure against and use for comparison. Use varieties of load, stress, spike and soak testing to find different issues. Consider replaying production traffic in your staging environment for a closer real life representation of production traffic. [More...]({{ site.baseurl }}/test/)

## [Production]({{ site.baseurl }}/production/)

In this phase, you need to live up to your Service Level Agreements (SLAs) and meet the expectations set in the requirements analysis phase. To ensure your requirements are met, utilize various solutions to analyze, measure and provide reports, on a monthly basis. Production focused solutions like Application Performance Management (APM) and flow analysis, provide in-depth data on the underlying causes that affect application Quality of Service (QoS), but they only reveal that an issue exists. [More...]({{ site.baseurl }}/production/)
