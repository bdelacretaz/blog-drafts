# Asynchronous decision making in open source teams and governments

I have made parallels [between my country and the Apache Software Foundation](http://grep.codeconsult.ch/2009/03/30/the-asf-is-the-switzerland-of-open-source/) (ASF) before. That was tongue-in-cheek but it turns out there are more valid parallels.

Thinking about how efficient decision making can be in distributed open source teams, as compared to the traditional enterprise style, I realized that my (Swiss) government actually works a lot like the ASF's board of directors, when it comes to decision making.

## Asynchronous decision making
_Asynchronous decision making_ is a key enabler of our geographically and culturally distributed open source teams. 

If synchronous decision-making meetings were required, even using remote channels like IRC or videoconference, we would move forward at a snail-like pace, as just finding a time where all stakeholders are available is impossible in an environment with no managers and no schedule.

Also, meetings are very expensive when you are working on a _maker's schedule_, as Paul Graham puts it [1]. Frequent meetings ruin the productivity of craftsmen, and there's lots of craftmanship in our industry, especially when you're building leading edge stuff. And you have to do that in today's world.

So, what's needed to enable people to make collective decisions asynchronously, without requiring meetings?

The first thing you need is an _central asynchronous communications channel_. Which technology you use for that doesn't really matter, but it has to allow everybody to get the same information, and provide a usable way of having _threaded discussions_, where you can branch off on a topic while other topics are being discussed on the same channel. This can be as simple as a whiteboard if people often visit the same place, or as elaborate as web-based forums accessible from any mobile device so you can bother^H^H^H^H^H reach people everywhere. At the ASF we use plain mailing lists for that, very successfully when people use them with the right discipline (see the appendix below). Archiving this channel is very useful, to allow newcomers to get a feel for how things work as well as documenting the reasoning that led to each decision and avoid having to repeat things over and over.

The second required tool is _a way to build consensus_, where you avoid deadlocks and make sure decisions go forward. Unanimity in decisions is ideal of course, but the second best is _consensus_, defined as _widespread agreement among people who have decision power_. Requiring unanimity or allowing vetoes in decisions can block progress, so at the ASF this only happens for a very limited set of decisions, as defined in our voting rules [4]. In companies, decision power can be based on hierarchy to break deadlocks, and has to sometimes, but abusing that can cause employees to lose their autonomy and purpose, which kills you in the long term.

To keep precise information on each decision, a _case management system_ is ideal. You can work without that depending on your team's size and the number of decisions that you take, but it's very convenient to be able to discuss the details of a given decision and keep associated information in a single place. You don't need complex software for that, at the ASF we use fairly simple _issue trackers_ for that. Those are Web-based systems where each case is handled on a single page, with a history of comments and actions. Some non-urgent of very hard decisions can take a long time to reach closure, and it's very useful to keep their history in a single place, if only to avoid having to explain them again to new members of the team. In a low tech environment you could just use a single sheet of paper to briefly document each decision with the key points that led to it, and keep those in binders or physical files.

A nice side effect of using case management software is that each decision gets a simple unique identifier, like FOO-123 for the 123th ticket of the FOO project. This removes any ambiguity as to which issue one's discussing, by mentioning those identifiers in conversations.

So, in summary, the following should allow your group to make decisions asynchronously, without requiring meeting and with a written trace of everything that happens:
* An archived asynchronous communications channel, where everybody can get the same information and informal discussions can take place.
* A way of building consensus, including fair rules for breaking deadlocks.
* Ideally, a case management system to keep track of each decision's details, in a much cleaner way than the often messy discussions that happen in email.

## Semi-asynchronous decision making at the ASF
TODO: anonymized examples from the board meeting

## The Swiss Federal Council works in the same way
TODO: colored lists, collaboration system that leads to them

## Appendix: Mailing lists at the ASF
At the ASF we use mailing lists as our central asynchronous communications channel, based on our _if it didn't happen on the dev mailing list, it didn't happen_ rule [2]. Mailing lists might be seen as tools of the past when you compare them with the latest shiny tools, but they remain a ubiquitous way of communicating in remote groups, especially when using with a strong discipline of _meaninfgul inline quoting_ [3]. Unfortunately I hear some "modern" email clients make a mess of that - just stay away from them.

## References
* [1] http://www.paulgraham.com/makersschedule.html - Paul Graham, _Maker's Schedule, Manager's Schedule_, July 2009
* [2] https://community.apache.org/apache-way/apache-project-maturity-model.html - The Apache Project Maturity Model, ASF community development team, 2015.
* [3] http://s.apache.org/gianugo_quoting_2002 - Gianugo Rabellino "[OT/Rant] Quoting", message to the cocoon-dev mailing list, January 2002
* [4] http://www.apache.org/foundation/voting.html - ASF voting rules, created in 1999 probably, or even earlier among the Apache Group.