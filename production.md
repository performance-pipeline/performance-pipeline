---
layout: page
title: Production
permalink: /production/
---

![performance-pipeline-image]({{ site.baseurl }}/images/performance-pipeline-production.png "The Performance Pipeline - Production Phase")

Now the application is in production and this where the rubber meets the road. Even a well-designed and coded application will be subject to an entirely different set of factors that can and will affect performance. Not only is the application now experiencing real user load and pushing and pulling data from backend systems, it has to compete for example, with other applications, VoIP traffic, users viewing YouTube videos for network bandwidth and computing resources. In most cases, poor performance will be reported by end users in the enterprise or in the case of e-commerce, customers abandoning shopping carts.  
Frequently, enterprise business units will require the IT organization to provide commitments for the availability and performance or quality of service (QoS) of the application through Service Level Agreements (SLAs). To ensure that SLA requirements are met, IT will utilize various solutions to analyze, measure and then provide reports, usually on a monthly basis. Production focused solutions like application performance management (APM) and flow analysis provide in-depth data on the underlying causes that affect application QoS, but they only reveal that an issue exists. Unfortunately, they do not detail how to resolve the problems within the application that are exacerbated by contention for network bandwidth, as an example.

On the other hand, a poorly performing application that appeared to be fine during integration and QA testing (when performance was not addressed early on) will now reveal its flaws in a production environment. Too many SQL calls for a single request or other inefficiencies within the application will only surface when subjected to a true production situation. Testing tools, such as profilers could catch the effect of performance related issues, but they will not pinpoint the specific code that is the root cause.

_**Take aways**_
- _**Use APMs** to measure and whether you are meeting the SLAs and expectations set out in the requirements analysis phase._
- _Remember APMs can **only find problems**, rather than provide you with details or help to debug them._