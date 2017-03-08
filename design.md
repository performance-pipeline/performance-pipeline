---
layout: page
title: 
permalink: /design/
---
<a href="https://github.com/performance-pipeline/performance-pipeline.github.io"><img style="position: absolute; top: 0; left: 0; border: 0;" src="https://camo.githubusercontent.com/121cd7cbdc3e4855075ea8b558508b91ac463ac2/68747470733a2f2f73332e616d617a6f6e6177732e636f6d2f6769746875622f726962626f6e732f666f726b6d655f6c6566745f677265656e5f3030373230302e706e67" alt="Fork me on GitHub" data-canonical-src="https://s3.amazonaws.com/github/ribbons/forkme_left_green_007200.png"></a>

![performance-pipeline-image]({{ site.baseurl }}/images/performance-pipeline-design.png "The Performance Pipeline - Design Phase")

Your design decisions should be made based on your requirements analysis. That is to say that the system you design needs to be capable of satisfying the requirements that has been previously set out. There will of course be additional constraints and requirements added to the system as it is designed, although these will be more granular. Performance is part of the customer experience that is designed. Here are some areas that will require thought and consideration:


- Prototyping your application can give you confidence that your design can meet the expectations outlined in the requirements analysis phase.
- Make sure your services aren’t so small that you’re constantly bouncing from service to service, you’ll start to find that your service communication latency dominates your request times. 
- Non-conversational requests reduces round trip invocations, and minimizes call latency. Try to batch requests into a single call to increase your work to latency ratio.
- Design your code with concurrency in mind. If you need to use a resource, acquire and release them like you pay for them by the millisecond! This will reduce resource contention across threads.
- Make use of pooled resources. Pooling lessens performance overheads as pooled resources don’t go through startup and teardown every time they’re needed.
- Write code in the right place. If you need to validate input in a form, do it in the browser, rather than the backend, where possible. By using caching, for certain data, you can return information back to the user quickly at the same time as reducing load on the back end.
- Reduce back end interactions. It’s invariably inevitable that you’ll need to get or update information in a database. You can design our database to reduce the time and number of requests you send to the back end. This can be done by designing in the right fetching strategies for instance.
- Make sure you hold your external dependencies accountable. If you use third party dependencies you have requirements on SLAs so that they match your SLAs and fit in with your requirements.

_**Take aways**_
- _**Ensure the architecture you design isn’t affecting your performance**. Prototyping can go a long way to making sure your design can meet your expectations. Your performance requirement constraints should go some way to helping you choose your desired architecture._
- _**Database interaction is expensive**. Make sure you only go there when you need to, and batch requests where possible._

Next Stage: [Development]({{ site.baseurl }}/development)