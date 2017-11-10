# Asynchronous decision making in remote teams

By Bertrand Delacretaz, November 2017 - @bdelacretaz, grep.codeconsult.ch - all rights reserved

_Asynchronous decision making_ is a key enabler of geographically and culturally distributed software teams, which need to make dozens of small or large decisions every week as a group to be successful.

This post is about the key principles and tools that make it possible.

Synchronous decision-making meetings can be _extremely_ expensive for people who work on a Maker's Schedule (Graham, 2009) and are often impractical with remote teams anyway. There's no lack of jokes and parody videos about how phone or video meetings often derail into inefficient time wasters that people do their best to avoid.

The asynchronous decision making principles used in large Open Source projects, like at the Apache Software Foundation (ASF) where I'm most active, are a very efficient way to move forward while requiring a minimum of meetings. Many Open Source projects have just a handful of meetings a year, if ever, yet consistently produce high quality software. 

There must be something to learn from the way they operate.

The first thing you need to enable asynchronous decision making is a _central asynchronous communications channel_. Which technology you use for that doesn't really matter but it has to allow everybody to get the same information and enable _threaded discussions_, where you can branch off on a topic while ignoring other topics being discussed on the same channel. Marine radio comes to mind as an analogy, where a broadcast channel is used very sparingly to get the attention of the right people, which then branch off to a sub-channel to have more detailed discussions.

Mailing lists are still used as this central channel in many Open Source projects, although the new generations of software developers might consider them as an old and clunky tool. Mailing lists require a lot of discipline to efficiently cope with the high traffic of a busy project, particularly in terms of meaningful quoting, sticking to one topic per thread and making sure subject lines are relevant (Delacretaz, 2017).

When used properly and coupled with an indexed archive, mailing lists are still the most ubiquitous tool to create such a channel. Corporate teams might benefit from more modern collaboration tools which are nicer to use and have stronger multimedia features, but whatever the tools the key is to create a channel where people can efficiently communicate as a large group on a wide variety of topics, asynchronously. A busy channel is often preferable to multiple channels (Mazzocchi, 2006) as a way to create a consistent and engaged community.

The second tool is _a mechanism for building consensus_, where you avoid deadlocks and make sure decisions go forward. Unanimity in decisions is ideal of course, but the second best is _consensus_, defined as _widespread agreement among people who have decision power_. Requiring unanimity or allowing vetoes in decisions can block progress, so at the ASF vetoes only apply to a very limited set of decisions types. The ASF's voting rules (ASF, 1999) are a well established and often copied way of building consensus in loosely coupled teams which in the case of the ASF, have no boss. They define a simple set of voting rules which can be used when consensus doesn't emerge naturally. 

Building consensus usually happens on the project's central channel as described above, but for complex topics it often makes sense to use a case management system, as described below. This allows for focusing the central channel on informal discussions and brainstorming, and moving to the more structured context of the case management system when a discussion evolves into a decision.

The third tool is this _case management system_ which helps keeps track of each decision in a more precise way. Depending on your team's size and the number of decisions that you make you can work without it, but it's very convenient to be able to discuss the details of a given decision and keep associated information in a single and relatively isolated place. You don't necessarily need complex software for that, at the ASF we use fairly simple _issue trackers_, Web-based systems originally created for software support and bug management. With such tools, each case is is handled on a single Web page, with a history of comments and actions with works very well for keeping track of decisions and of the path that leads to them. Some non-urgent or complex decisions can take a long time to reach closure, and it's very useful to have their history in a single place. This means new team members (or those who return from absence) can get up to speed mostly by themselves, by looking at which decisions have been made recently or are outstanding, who's involved in them and by discovering the story behind each decision.

One success story about this is the ASF's Board of Directors, which applies these principles to allow its nine members to make a few dozen decisions at each of our monthly phone meetings, which last less than two hours. We spend time carefully preparing those meetings by making most of our decisions asynchronously in advance, allowing us to focus the meeting on the complex or uncertain ones and spending very little time on the cases where we got full or partial consensus in advance.

Another interesting example outside of the software world is the Swiss Federal Council's weekly meeting (Swiss Federal Council, 2017), which runs in a similar way. Teams carefully prepare the meeting by building consensus in advance using techniques similar to the ones described here. The meeting agenda consists of a set of color-coded lists, with colors that indicate which items can be rapidly approved, which ones need a bit more discussion and which ones are expected to be complex . This allows those seven very busy people to make more than 2'500 yearly decisions over about 50 weekly sessions of a few hours each, which sounds quite efficient to me.

Based on my experience with these tools and techniques in various contexts, I believe the benefits of this approach make the investment in time and tools a very valuable one. It also leads to happier team members, which is a key component of success!

## References
* (Graham, 2009) : Paul Graham, _Maker's Schedule, Manager's Schedule_, July 2009 - http://www.paulgraham.com/makersschedule.html - 
* (Mazzocchi, 2006): Stefano’s Mazzocchi’s Busy List Pattern, blog post by Bertrand Delacretaz presenting Stefano Mazzocchi's ideas - https://grep.codeconsult.ch/2011/12/ - 
* (ASF, 1999): ASF voting rules - http://www.apache.org/foundation/voting.html
* (Swiss Federal Council, 2017) : Federal Council meeting - how the meeting runs -  https://www.admin.ch/gov/en/start/federal-council/tasks/decision-making/federal-council-meeting.html
* (Delacretaz, 2017) : Large Mailing Lists Survival Guide - https://grep.codeconsult.ch/2017/11/10/large-mailing-lists-survival-guide/

