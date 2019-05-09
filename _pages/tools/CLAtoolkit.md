---
title: "The Connected Learning Analytics (CLA) toolkit"
permalink: /tools/CLAtoolkit/
---

The CLA toolkit is designed to interface with a variety of social media sources using the APIs that they make available to extract data about a student’s participation in defined learning activities. It makes use  of the [Experience API (xAPI)](https://www.adlnet.gov/research/performance-tracking-analysis/experience-api/) data standard to store information in an interoperable format that can be used in later analysis (see our pages on [data portability]({{site.baseurl}}/dataPortability/) for more information about that).

![The CLA toolkit]({{site.baseurl}}/assets/images/CLAToolkit.png)

The CLA toolkit gives students access to the data that they generate. They  can decide which social media accounts to link using this tool, which only collects data for specified activities in those  accounts. This  both preserves student privacy (as students can opt in and out of any data collection), and enables student control over what subset of their social media data is collected by an institution. The CLA toolkit enables students to explore the data that they generate in social media environments and as a consequence, promotes awareness of, and improves data literacy.  

The development of this tool was supported by the Australian Government's Office for Learning and Teaching (OLT), under a Research and Innovation grant (Enabling connected learning via open source analytics in the wild: learning analytics beyond the LMS).

###  Code base - CLA toolkit V2

Version 2 of the codebase for this tool was implemented in TypeScript, using a mongo database and GraphQL to interface with various social media APIs. This architecture is highly modular and flexible, making ongoing extensions to the codebase far easier. It is essentially a helper tool, which enables data collection via the creation of "classes" using various social media, and the processing of student sign up and authentication to those classes for the social media that they choose to link to that class.

Currently  this tool supports the collection of data for students who sign  up to data collection from:
- twitter (tweets with specified hashtags)
- slack (messages from specified channels)
- trello (activity on a linked board)
- GitHub (contributions to a specified repo)

Check out the codebase [here](https://github.com/uts-cic/CLAtoolkitv2)

Analytics and reports are provided by the [LA-API]({{site.baseurl}}/tools/LA-API/), which is now being developed as a separate set of projects.


###  Code base - CLA toolkit V1

Version 1 one of the CLA toolkit was developed in 2015, using python with a django framework, and highcharts for dashboards. You can read about how we used it in trials with students in [this]({{site.baseurl}}/assets/papers/Published-3607-12964-2-PB.pdf) paper.


This version of the codebase became increasingly difficult to maintain. It ended up with a tightly coupled architecture, with LA being stored during data capture. This meant that functionality was often broken as data structures evolved to cater for new data imports from different social media providers.

Much of this codebase is depreciated and/or no longer functional. If you are interested in the codebase for historical purposes then you can check it out here:

- The [Connected Learning Analytics Toolkit V1](https://github.com/kirstykitto/CLAtoolkit)
- The [Connected Learning Recipe](https://github.com/kirstykitto/CLRecipe)
