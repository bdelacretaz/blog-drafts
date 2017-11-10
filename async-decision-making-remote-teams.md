# Asynchronous decision making in remote teams

By Bertrand Delacretaz, November 2017 - @bdelacretaz, grep.codeconsult.ch

_Asynchronous decision making_ is a key enabler of geographically and culturally distributed open source teams. This post is about the key principles and tools that make it possible.

Synchronous decision-making meetings can be _extremely_ expensive for people who work on a Maker's Schedule (Graham, 2009) and are often impractical with remote teams anyway. There's no lack of jokes and parody videos about how phone or video meetings often derail into inefficient time wasters that people do their best to avoid.

The asynchronous decision making principles used in large Open Source projects, like at the Apache Software Foundation (ASF) where I'm most active, are a very efficient way to move forward while requiring a minimum of meetings. Many Open Source projects have just a handful of meetings a year, if ever, yet consistently produce high quality software. 

There must be something to learn from the way they operate.

The first thing you need to enable asynchronous decision making is a _central asynchronous communications channel_. Which technology you use for that doesn't really matter but it has to allow everybody to get the same information and provide a usable way of having _threaded discussions_, where you can branch off on a topic while ignoring other topics being discussed on the same channel. Such a channel is best used in a similar way to marine radio channels, where a broadcast channel is used sparingly to get the attention of the right people, which then branch off to a sub-channel to have a more detailed discussion.

Mailing lists are still used as this central channel in many Open Source projects, although the new generations of software developers might consider them as an old and clunky tool. Mailing lists require a lot of discipline to efficiently cope with the high traffic of a busy project, particularly in terms of efficient quoting, sticking to one topic per thread and making sure subject lines are relevant (Delacretaz, 2017).

When used properly and coupled with an indexed archive, mailing lists are still the most ubiquitous tool for loosely coupled groups. Corporate teams might benefit from more modern collaboration tools which are nicer to use and have stronger multimedia features, but whatever the tools the key is to create a channel where people can efficiently communicate as a large group on a wide variety of topics, asynchronously. A busy channel is often preferable to multiple channels (Mazzocchi, 2006) as a way to create a consistent and engaged community.

The second tool is _a mechanism for building consensus_, where you avoid deadlocks and make sure decisions go forward. Unanimity in decisions is ideal of course, but the second best is _consensus_, defined as _widespread agreement among people who have decision power_. Requiring unanimity or allowing vetoes in decisions can block progress, so at the ASF vetoes only apply to a very limited set of decisions types, as defined by our voting rules (ASF, 1999). Building consensus usually happens on the project's central channel as described above, but for complex topics it often makes sense to use a case management system, as described below. This allows for focusing the central channel on informal discussions and brainstorming, and moving to the more structured context of the case management system when a discussion evolves into a decision.

The third tool is a _case management system_ which helps keeps track of each decision in a more precise way. Depending on your team's size and the number of decisions that you take you can work without it, but it's very convenient to be able to discuss the details of a given decision and keep associated information in a single and relatively isolated place. You don't necessarily need complex software for that, at the ASF we use fairly simple _issue trackers_, Web-based systems originally created for software support and bug management. With such tools, each case is is handled on a single Web page, with a history of comments and actions with works very well for keeping track of decisions and of the path that leads to them. Some non-urgent or complex decisions can take a long time to reach closure, and it's very useful to have their history in a single place. This means new team members can get up to speed in a mostly self-service way by looking at which decisions have been made or are outstanding, who's involved in them, etc.

A useful side effect of using case management software is that each decision gets a simple unique identifier, like FOO-123 for the 123th ticket of the FOO project. This allows for removing any ambiguity as to which issue one's discussing, by mentioning those identifiers in conversations.

In summary, the following tools should allow your group to make decisions asynchronously, without requiring meetings and with a written trace of everything that happens:

* An archived asynchronous communications channel, where everybody can get the same information, threaded discussions can take place, and people can catch up with specific ongoing discussions at any time.
* A way of building consensus, including fair rules for breaking deadlocks.
* A case management system to keep track of each decision's details and of the decisions "story".

If you do have meetings, these techniques are still very useful as a way to make them much more efficient by preparing them and getting closure on as many things as possible in advance.

The ASF's Board of Directors applies these principles to allow its nine members to make a few dozen decisions at each of our monthly phone meetings, which last less than two hours. Those meetings are very efficient as we spend time carefully preparing them, using a very simple bespoke case management system to build consensus in advance wherever possible, identify which topics need more discussion and prioritize them in advance.

Interestingly, the Swiss Federal Council's weekly meeting runs in a similar way, using lots of upfront preparation along with a set of color-coded lists for their agenda to indicate which items can be rapidly approved and which need more discussion. This allows those seven very busy people to make about 2'500 decisions over about 50 weekly sessions of a few hours each, which is sounds more efficient to me than many traditional meetings.

The asynchronous decision making techniques used by Open Source projects (and governments as we just learned) can help remote teams by streamlining and better defining their decision process. You don't need complex tools for that, but using them efficiently requires discipline and a willingness to experiment initially, until your team reaches its asynchronous decision making "cruising speed". 

I believe the benefits of this approach make the investment in time and tools a very valuable one and leads to happier team members, which is a key component of success!

## References
* (Graham, 2009) : Paul Graham, _Maker's Schedule, Manager's Schedule_, July 2009 - http://www.paulgraham.com/makersschedule.html - 
* (Mazzocchi, 2006): Stefano’s Mazzocchi’s Busy List Pattern, blog post by Bertrand Delacretaz presenting Stefano Mazzocchi's ideas - https://grep.codeconsult.ch/2011/12/ - 
* (ASF, 1999): ASF voting rules - http://www.apache.org/foundation/voting.html
* (Swiss Federal Council, 2017) : Federal Council meeting - how the meeting runs -  https://www.admin.ch/gov/en/start/federal-council/tasks/decision-making/federal-council-meeting.html
* (Delacretaz, 2017) : Large Mailing Lists Survival Guide - https://grep.codeconsult.ch/2017/11/10/large-mailing-lists-survival-guide/

