---
title: "Trialling the CLAToolkit - Dashboards and Adventures with IFN614"
description: "Trialling the CLAToolkit"
categories:
  - Blog
tags: [connected learning analytics, dashboards, CLAtoolkit, SNA, Content Analysis, user trial]
author: kirsty
---

So... its been a while. Sorry, but these last few months have been pretty busy. We have been madly rolling out functionality, finding out what people think about it, and then trying new things and upgrades. We have also been running a first trial with a real actual unit run at QUT
<a href="http://2015.informationprograms.info/">IFN614: Information Programs</a>  which is run by an academic in my School <a href="http://higheredukate.com/who-is-kate/">Kate Davis</a>. Kate is one of your classic Teach in the Wild types. She has a long history of using innovative Wordpress set-ups for her classes that blow your standard LMS out of the water. Normally Kate spends a couple of weeks at the beginning of semester posting announcements in Blackboard (QUT's standard LMS) saying that the class is not there, and that they should follow a link to her actual teaching site. Check out the difference in the two setups when it comes to IFN614:

####  Blackboard:
![IFN614, Blackboard Site]({{site.baseurl}}/assets/images/IFN614-blackboard.jpg){: .align-center}

#### Versus WordPress:

![IFN614, Wordpress Site]({{site.baseurl}}/assets/images/IFN614-wordpress.jpg){: .align-center}

Of particular interest to us, Kate has strong participation requirements for this unit, students need to post on blogs in the wordpress site, and participate in regular Twitter chats using hashtags specified at the beginning of semester. These chats go nuts. I have watched a couple and they get an insane amount of action. A couple of weeks ago Kate was telling me that she normally has three different screens focussed on different parts of the chat, and she still misses most of what is going on. Historically, Kate has had to manually trawl through twitter to work out how well her students participated in the unit... you can imagine how easy that is. This makes her a fantastic candidate for our project.. hopefully it is really going to help her out down the track.

So. We gave Kate's students the option to sign up for a trial of the CLA toolkit. Data was collected from the designated hashtags used in the class as well as from the Wordpress forums. The class has 34 students, and about a third signed up (twelve students were in the system the last time I checked). The class has pretty much finished now (they are all madly finishing off assignments etc.) so we pretty much have our full data set now. Lets use it go explore some of the reports that are available in the CLA toolkit.

First, lets check out the Activity Dashboard for the unit.

![IFN614, Activity]({{site.baseurl}}/assets/images/IFN614-Activity.jpg){: .align-center}

When do you think the twitter chats were? ;) Note that by the end of the semester these things were getting about 300 tweets just from the signed up cohort! (Although Kate herself was normally responsible for around 80 of them.. talk about <a href="https://coi.athabascau.ca/coi-model/description-teaching-presence/">teacher presence</a>!) Note also that the chats got more active as the class progressed and the class started finding their feet. See down the bottom there is a little slider? That lets people zoom down into more specific points in time. They can then filter some of the other reports off of this restricted period (at the moment this works with SNA and a wordcloud but this functionality should roll out to all the widgets over summer). The Activity report also lets the instructor drop down into the student dashboard, which I am a bit worried is too boring at the moment... In our ethics application we said that we would only show students data about their own behaviour in the system. This means that, for example, the SNA shown to the students is only about <i>their</i> tweets to someone else. Check out my student dashboard SNA for our PROJ-TEAM unit (which is collecting data from the #clatoolkit, #xAPI and #learninganalytics hashtags).

![Student dashboard for project team]({{site.baseurl}}/assets/images/PROJ-TEAM-Student.jpg){: .align-center}

That shot also shows you another feature - students can select specific links and then see what interactions led to those links in another report below... here we see some of the places where I have mentioned @aneesha in a tweet. But back to the point... Here is the equivalent instructor facing report for PROJ-TEAM

![SNA for the project team]({{site.baseurl}}/assets/images/PROJ-TEAM-SNA.jpg){: .align-center}

Its a lot more interesting hey? We are currently trying to work out what a nice balance is between privacy and information.. I think at the moment we might be leaning a bit too much towards privacy. Might have to go back and get a variation to the ethics application once we work out a good balance. Now, just as an aside.. If you explore that shot you can also see that a couple of the project team have not signed up yet.. You should totally pay them out if you work out who they are ;) So.. anyway this instructor facing SNA report also lets you do the click on a link and explore specific interactions, which is really useful for working out how different members of a cohort are interacting with one another. And if we think back to the Activity report then we should recall that we can look at the interactions that occurred over a specific more limited period of time - another feature that I have been using quite a bit.

One more set of reports are currently available, geared towards Content Analysis. These give sentiment analysis, a word cloud and a Topic Model based on <a href="http://nlp.stanford.edu/events/illvi2014/papers/sievert-illvi2014.pdf">LDAvis</a>

![Project team content dashboard]({{site.baseurl}}/assets/images/PROJ-TEAM-Content.jpg){: .align-center}

This report is going to see a lot of development over the next few months - fun times ahead! :)

Anywho.. back to IFN614..
Here is a zoomed out representation of the Social Network Analysis of the class that Kate can see at the moment.

![IFN614, SNA]({{site.baseurl}}/assets/images/IFN614-SNA.jpg){: .align-center}

Cool huh? Its a pretty connected class.
