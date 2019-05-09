---
title: "Data Portability"
permalink: /dataPortability/
toc: true
toc_label: "Data Portability"
sidebar:
  - image: /assets/images/dataPortability.png
    image_alt: "Data portability icon"
---


What is data portability? It is the idea that people should not have their data stored in "silos" or "walled gardens" that are incompatible with one another and so subject them to vendor lock-in.

This is not just a "nice to have"...  it is becoming legally enshrined for some jurisdictions (see e.g.  [Article 20 of the GDPR](https://gdpr-info.eu/art-20-gdpr/), which states that:

{: .notice--info}
*The data subject shall have the right to receive the personal data concerning him or her, which he or she has provided to a controller, in a structured, commonly used and machine-readable format and have the right to transmit those data to another controller without hindrance from the controller to which the personal data have been provided*

However, good arguments have been made that data portability is too weak (see e.g. [GDPR: data portability is a false promise](https://medium.com/mydata/gdpr-data-portability-is-a-false-promise-af460d35a629)) to enable user control  of *their* personal data. How then should we approach this complex concept in the field of education? This page is devoted to exploring these issues...



## Lifelong learning

Wherever you stand on data ownership... right now the education sector is a very long way from being able to provide data portability in any form. Why is that a problem?

Because learning happens across a lifetime, and in multiple places and spaces. People connect both face to face and online to grow and develop, they learn from their peers, apply skills learned in one setting to new contexts, and source content and information from both formal and informal settings. As they gain confidence, those same individuals start to mentor, teach, and instruct other people in their personal learning network ([PLN](http://www.linkinglearning.com.au/plns-theory-and-practice/)). Sometimes they decide to return to formal learning opportunities, sometimes not. This process of learning continues throughout a person's career, not just during a finite period of formal education at the start of their life.

That means that if fields like [Learning Analytics (LA)](https://solaresearch.org/) are going to deliver on core goals like [personalised learning](https://er.educause.edu/articles/2016/3/personalized-learning-what-it-really-is-and-why-it-really-matters) then they should really be working to use data from across a person's life, instead of just [concentrating on their current performance](https://mfeldstein.com/we-have-personalization-backwards/). However, this opens up a whole range of technical, ethical and legal issues! This page is mainly concerned with the technical problems of porting data between our educational silos.

## Data standards

The traditional way to achieve data portability requires common technical standards to facilitate the transfer from one data controller to another, thus promoting data interoperability. In the modern era of education, we have two key data standards that have emerged which would assist with this...

### Experience API (xAPI)

  [xAPI](https://www.adlnet.gov/research/performance-tracking-analysis/experience-api/) provides a platform-neutral method to collect data about events occurring in any learning experience. It was released in 2013 as the outcome of an [Advanced Distributed Learning  (ADL)](https://www.adlnet.gov/) project that aimed to: improve interoperability between elearning systems that collect and exchange student learning data; and overcome the limitations of SCORM. Statements are very flexibly defined in xAPI as actor, verb, object triplets, with a syntax defined in an open source [technical specification](https://github.com/adlnet/xAPI-Spec) maintained by the xAPI community. xAPI Learning Record Providers (LRPs) send xAPI statements to a Learning Record Store (LRS), for later analysis or reporting.

  *Find out more:*
  The xAPI community is broad and kind of spread all over the place. Here are some  places you can start finding  out more about how to implement  it.
  - The [xAPI technical specification](https://github.com/adlnet/xAPI-Spec) gives details about the base syntax that must be satisfied by xAPI compliant LRPs.
  - The [xAPI Profile specification](https://github.com/adlnet/xapi-profiles) extends the base syntax,
  - Don't know how to generate statements in your tools yet?  Check out these tutorials on building LRPs by [Anthony Altieri](http://www.learningsolutionsmag.com/articles/2322/getting-started-with-xapi-four-lines-of-code), and [Mel Milloway](https://www.linkedin.com/pulse/follow-along-3-getting-started-xapi-tutorials-melissa-milloway-msit/), and [eLearning art](https://elearningart.com/blog/xapi/).
  - A number of LRS providers host free demo services that you can use to store xAPI statements, such as: [Veracity](https://lrs.io/), [Yet](https://www.yetanalytics.com/free-sandbox-account), [SCORMCloud](https://rusticisoftware.com/products/scorm-cloud/)...
  - The IEEE released a guide on [xAPI for technical implementers](https://docs.google.com/document/d/1do3WKfzsFKjXK6hlLOv-yiXJ0gdY1tYWULABWnDTIjQ/edit?usp=sharing)
  - And you could try joining the [xAPI and Analytics slack channel](https://join.slack.com/t/xapi-la/shared_invite/enQtMzMyMjM3NjQ0Njc4LTRlODc3MTkyMTJhYmI4NTc0OThhNjU0MTNjYjc3NTBmYjRmNDVjMjFkZjMyZWUxZGNkNDY2YzE1MzgwN2IxNDk)

### IMS Caliper

In 2015 [IMS](https://www.imsglobal.org/) publicly released [Caliper](https://www.imsglobal.org/activity/caliper) as an alternative educational data standard. Similar to xAPI, the [Caliper specification](https://www.imsglobal.org/sites/default/files/caliper/v1p1/caliper-spec-v1p1/caliper-spec-v1p1.html) creates triples about an actor, performing an action, on an object. This makes Caliper very similar to xAPI, but it has much stricter semantics: to be certified as Caliper compliant a data provider must both become a member of the consortium, and then implement at least one *metric profile*, which then specifies how activity should be tracked, and for which actions, objects, and actors.

This results  in complete alignment on the data models implemented by any vendor implementing Caliper. However, the data model itself is very tightly aligned with traditional learning ecosystems, and does not readily extend to learning ‘in the wild’.

### Two tutorials on xAPI and Caliper

Want an intro to all this? Here are the slides from a workshop that the BeyondLMS project lead (Kirsty Kitto) gave at the learning analytics track of [eLearning Korea](http://www.elearningkorea.org/en/business/business3?pgcode=15) during 2018. It introduces the two standards (but with a core focus on xAPI), along with their advantages and disadvantages for achieving data portability over a lifetime.


<iframe src = "{{site.baseurl}}/assets/slides/Kitto-xAPI.pdf" width='100%' height='500' allowfullscreen type='application/pdf'></iframe>

If  you want to find out more about Caliper,  then the talk at the same event by Markus Gylling is a good place to go!

<iframe src = "{{site.baseurl}}/assets/slides/LASI_Markus_Gylling_mgy-seoul-sep2018.pdf" width='100%' height='500' allowfullscreen type='application/pdf'></iframe>


## The problem with standards

While we have been very involved in educational data standards (and in particular xAPI) for  the BeyondLMS project, there have been [ongoing challenges](https://er.educause.edu/articles/2017/7/the-promise-of-learning-data-interoperability) in getting people to follow them when building learning ecosystems. If you work in a large education provider (like a university) then you will probably find yourself dealing with tools that emit data conforming to both... or neither. People just don't tend to follow standards when they build their tools, often because it involves considerably more effort. But  even when they do, we often find that the resulting data is not interoperable anyway.

We are developing the [Learning Analytics API (LA-API)]({{site.baseurl}}/tools/LA-API/) as a solution to this problem. It implements a form of *pragmatic data interoperability*, using NLP and GraphQL to flexibly map between data from different formats. Go check out the [more detailed pages]({{site.baseurl}}/tools/LA-API/) to find out more.
