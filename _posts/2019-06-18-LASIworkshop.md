---
title: "Building LA ecosystems"
description: "Resource, links etc. for my LASI workshop"
tags: [data interoperability, xAPI, Caliper, data portability, lifelong learning]
toc: true
toc_label: "Data Portability"
author: kirsty
categories:
  - Blog
---

Welcome! This blog post has resources and links for the workshop I am giving for [LASI19](https://solaresearch.org/events/lasi/lasi19/) on *Building Learning Analytics Ecosystems*. Follow the links alongside to find the relevant activity.

## My Slides

[Download them]({{site.baseurl}}/assets/slides/BuildingLAEcosystems.pptx) if you want to have a look! (Don't skip ahead though! Grrrr.) Or you can have a look  at them embedded below.

<iframe src = "{{site.baseurl}}/assets/slides/BuildingLAEcosystems.pdf" width='100%' height='500' type='application/pdf' allowfullscreen></iframe>

##  Activity: Build a LRP

NB: Make sure you ask Kirsty to give you login information for the LRS so that you can go and have a look at the data resulting from this exercise! (She is not sharing it here as we are goign to use one of her private LRSs!)

This exercise is going to give you a taster in what it takes to build a LRP (Learning Record Provider). I also expect that it will introduce you all to the issues associated with achieving data interoperability across multiple LRPs... but more on that later  ;) We are building off of the great starter resources provided by [Anthony Altieri](https://learningsolutionsmag.com/articles/2322/getting-started-with-xapi-four-lines-of-code) and [Bryan Jones](https://elearningart.com/blog/xapi/), but  with a slight twist... you should work out  your own statements! Feel free to look at those tutorials if you are having troubles, but you should work to define a statement that best describes the specific action being performed by the learner you are tracking.

Basically, here are the four steps you must take to send an xAPI statement to a LRS:

1. Define a variable that holds the URL address of the learning record store (LRS) and the username and password to authenticate
1. Tell the browser to use that variable for the LRS
1. Create a variable and define the xAPI statement
1. Send the statement

Below you will see some more detailed instructions about how to do this... pair up with someone you don't know and work with them through this activity!

### Follow these steps

1. Download [this file]({{site.baseurl}}/assets/LRPexercise.zip) and open up `LRP.html` in your favourite text editor
1. You will need to fill in a few fields:   
    - LRS endpoint: https://lasi-workshop.lrs.io/xapi/
    - Username: participant
    - Password: password
    - the learner's unique id (an email will work here, but feel free to add extra information to this field... look up the stuff you can add [here](https://github.com/adlnet/xAPI-Spec/blob/master/xAPI-Data.md#actor))
    - the verb (and maybe an activity... look at the xAPI specification linked to above for info!)
    - an object
1. You need to go and get some files from ADL to support sending statements!  
    - Go to [https://github.com/adlnet/xAPIWrapper](https://github.com/adlnet/xAPIWrapper)
    - Go to `dist` folder, copy the `xapiwrapper.min.js` file and paste it into the folder you have your `LRP.html` file in
    - Go to `lib` folder, copy the `cryptojs_v3.1.2.js` file and paste it into the same folder
1. Open up the edited file in your web browser. Try clicking the button - does it work?
1. Log into the LRS and explore the data in it... are your statements there? Here are some things that might help  you troubleshoot if your statements are not showing up:  
  - are your statements legal? Check the spec, or... see the next step
  - check the log entries... you might find some error messages pertaining to your LRP (where are these in this LRS? Can you find them?)
  - have you got your `xapiwrapper.min.js` and `cryptojs_v3.1.2.js` files in the right place? NB. you need to have a wrapper file for your `LRP.html` file to work!
  - if you are still having troubles then the `LRP-example.html` file should work... (if you have the wrappers etc. in the same folder)
1. Go and have a look at the other statements in the LRS! What analytics and reporting does it provide? Are they any good?
1. Can you extend your LRP to provide more information? What about a `context` element? Maybe you can add a second button or other thing to the page... how would you define a statement for that object?
1. Try  sending your statements to a *different* LRS! Some of the other free ones are [Yet](https://www.yetanalytics.com/free-sandbox-account), [watershed](https://www.watershedlrs.com/product/pricing/essentials-learning-record-store  
) and [SCORMCloud](https://rusticisoftware.com/products/scorm-cloud/)... or you could try creating your own [Veracity](https://lrs.io/) one and sending statements there ;)


## Pick a challenge

In the afternoon we will focus upon further exploration of key avenues that you find interesting.

- You need to form into groups of at least 4 who all want to work on one of these challenges (or a combination of them).
- You should work together using the resources associated with each challenge to come up with an artefact.
- Each group will have to present its findings at the end of the day!

### Challenge 1: best practice xAPI profiles

{: .notice--info}
Can you build a profile that will provide data the LA community can actually use?

**Resources that might help:**
- [xAPI profile starter template](https://www.imsglobal.org/sites/default/files/caliper/v1p1/caliper-spec-v1p1/caliper-spec-v1p1.html)
- [xAPI Profile specification](https://github.com/adlnet/xapi-profiles)
- [all published xAPI profiles](http://xapi.vocab.pub/) (Its not many!)
- [Caliper pages](https://www.imsglobal.org/activity/caliper)
- [Caliper specification](https://www.imsglobal.org/sites/default/files/caliper/v1p1/caliper-spec-v1p1/caliper-spec-v1p1.html) and [Metric profiles](https://www.imsglobal.org/caliper-11-metric-profiles)

### Challenge 2: design an extension to the LA-API schema

{: .notice--info}
Can you extend the LA-API schema design to facilitate more LA?

**Resources that might help:**
- [LA-API page]({{site.baseurl}}/tools/LA-API/)
- [GraphQL specification](https://graphql.github.io/graphql-spec/) and [documentation](https://graphql.org/)
- Ask me to share some example data via our GraphiQL site!

### Challenge 3: extend the LA-API

{: .notice--info}
Can you fork the LA-API/mongo-extract and extend them to add new functionality

**Resources that might help:**
- [LA-API page]({{site.baseurl}}/tools/LA-API/)
- [GraphQL specification](https://graphql.github.io/graphql-spec/) and [documentation](https://graphql.org/)
- Ask me to share some example data via our GraphiQL site!

### Challenge 4: design a dashboard

{: .notice--info}
Can you leverage data interop to build dashboards that self populate using all relevant data?

**Resources that might help:**
- [LA-API page]({{site.baseurl}}/tools/LA-API/)
- [GraphQL specification](https://graphql.github.io/graphql-spec/) and [documentation](https://graphql.org/)
- Ask me to share some example data via our GraphiQL site!

### Challenge 5: explore the ethics of data interoperability

{: .notice--info}
What might go wrong if data flows across institutional boundaries?

De Hert, P., Papakonstantinou, V., Malgieri, G., Beslay, L., & Sanchez, I. (2018). [The right to data portability in the GDPR: Towards user-centric interoperability of digital services](https://www.sciencedirect.com/science/article/pii/S0267364917303333). Computer Law & Security Review, 34(2), 193-203.
