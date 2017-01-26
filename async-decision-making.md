# Asynchronous decision making in open source teams

_Asynchronous decision making_ is a key enabler of our geographically and culturally distributed open source teams. In this post I'll explain the ingredients that make it work at the ASF.

I became active in the ASF in 2001 [via Gianugo Rabellino](https://lists.apache.org/thread.html/c9180946d53733876c99dffba598017a736c9c31efac55a069f8efee@1006518708@%3Cfop-dev.xmlgraphics.apache.org%3E) - he was the one who started the discussions with Apache Fop about me donating the jfor XLS-FO to RTF converter that I had developed earlier. It was already too late to uninvent RTF which is a terrible format, but I digress. I am currently a member of the [Board of Directors](https://www.apache.org/foundation/board/) of the ASF and have been doing a lot of thinking (and [presentations](https://pinboard.in/u:bdelacretaz/t:pressbook/)) about  what makes the ASF tick in terms of collaboration and Shared Neurons.

If synchronous decision-making meetings were required in ASF projects, even using remote channels like IRC or videoconference, we would move forward at a snail-like pace, as just finding a time where all stakeholders are available is almost impossible in an environment that has no managers and no central schedule.

Meetings are also very expensive when you are working on a _maker's schedule_, as described by Paul Graham [1]. Frequent meetings ruin the productivity of craftsmen, and there's lots of craftmanship in our industry, especially when you're building leading edge stuff.

So, what's needed to enable people to make collective decisions asynchronously, without requiring meetings?

The first thing you need is a _central asynchronous communications channel_. Which technology you use for that doesn't really matter, but it has to allow everybody to get the same information, and provide a usable way of having _threaded discussions_, where you can branch off on a topic while ignoring other topics being discussed on the same channel. This can be as simple as a whiteboard if people often visit the same place, or as elaborate as web-based forums, accessible from any mobile device so you can bother^H^H^H^H^H reach people everywhere. At the ASF we use plain mailing lists for that, very successfully when people use them with the right discipline (see the appendix below). Archiving this channel is very useful, to allow newcomers to get a feel for how things work as well as documenting the reasoning that led to each decision and avoid having to repeat things over and over.

The second required tool is _a way to build consensus_, where you avoid deadlocks and make sure decisions go forward. Unanimity in decisions is ideal of course, but the second best is _consensus_, defined as _widespread agreement among people who have decision power_. Requiring unanimity or allowing vetoes in decisions can block progress, so at the ASF vetoes only apply to a very limited set of decisions types, as defined by our voting rules [4]. In companies, decision power can be based on hierarchy to break deadlocks. That has to happen sometimes, but abusing it can cause employees to lose their autonomy and purpose, which kills your team in the long term.

To keep track of each decision, a _case management system_ is ideal. You could work without that, depending on your team's size and the number of decisions that you take, but it's very convenient to be able to discuss the details of a given decision and keep associated information in a single place. You don't need complex software for that, at the ASF we use fairly simple _issue trackers_. Those are Web-based systems where each case is handled on a single page, with a history of comments and actions. Some non-urgent or very hard decisions can take a long time to reach closure, and it's very useful to keep their history in a single place, if only to avoid having to explain them again to new members of the team. In a low tech environment you could just use a single sheet of paper to briefly document each decision with the key points that led to it, and keep those in binders or physical files.

A nice side effect of using case management software is that each decision gets a simple unique identifier, like FOO-123 for the 123th ticket of the FOO project. This removes any ambiguity as to which issue one's discussing, by mentioning those identifiers in conversations.

So, in summary, the following should allow your group to make decisions asynchronously, without requiring meeting and with a written trace of everything that happens:
* An archived asynchronous communications channel, where everybody can get the same information and threaded discussions can take place.
* A way of building consensus, including fair rules for breaking deadlocks.
* If possible, a case management system to keep track of each decision's details, in a much cleaner way than the often messy discussions that happen on the asynchronous channel.

## Semi-asynchronous decision making at the ASF
I've been a member of the ASF's Board of Directors for a few terms now and I'm still impressed by how efficient our monthly phone conferences are. The meeting regularly lasts only 60 to 90 minutes, during which we approve around 50 projet reports, vote on a few resolutions and often address a few discussion items.

Besides a few simple things like good phone discipline and a side channel for less important comments (and jokes), the main reason this meeting is so efficient is that _almost everything is decided in advance_. 

Board members are expected to read the project reports before the meeting, and a dead simple case management system (described below) helps discuss issues in advance, and find out which reports require a more extensive discussion.

Assuming the majority of board members have read the reports in advance, and flagged them as ok or requiring discussion, we don't need any housekeeping time during the meeting. Everybody shows up with a clear view of where difficult discussions might arise, so they have time to prepare for that, including asking others for clarification before the meeting so we can resolve any outstanding issues without delay.

The case management system that we use for this is extremely simple, but in terms of enabling asynchronous (or rather semi-asynchronous) decision making it fullfills its role. Our meeting agenda consists of a _single text file in our source control system_, with a simple structure that provides for a small discussion space for each report that we have to approve and each resolution that we need to vote on.

The agenda file structure looks roughly like this:

    Call to order
    Roll call
    Officer reports
    Project reports, headers and discussion space
    Board Resolutions with discussion space
    Appendix: Full Project reports and other supporting material
   
And a project report header and discussion space is as simple as this:

    E. Apache Blazinator Project [Bob Blazer / Bertrand]

      See Attachment E

      [ Blazinator.
        approved: bd, mm, dd, db, jc, ldv
        comments:
		  bd:  Not sure why LEGAL-123 blocks their release
		  ldv: They are waiting for the committer to supply
		       an updated iCLA as the received one was 
			   incomplete.
		  bd:  Ok, thanks, approving the report then.
        ]
		
This simple block of structured text builds a very simple "case management system" for the case of approving the Blazinator report. 

The "approved" line indicates which board members have approved the report, on a single line so that simple text-based tools can validate and count the approvals.

The "comments" section allows stakeholders to comment on the report (which is found in an appendix later in the text file), and reply to each other's comments to hopefully reach closure before the meeting. If this happens, approving this report takes almost no time in the meeting, the chairman can just list the project names ("case identifiers" according to the above terminology) of such pre-approved reports, asking if anybody's opposed to approving them.

Combined with the ASF board's mailing list, this builds a very simple and very efficient system for semi-asynchronous decision making. Most decisions are taken before the meeting, and the participants can spend their time where it actually adds value as opposed to exchanging boring status information during the meeting.

## Try it yourself!
Many ASF and other Open Source projects release world-changing software while having no or very few meetings, demonstrating that these techniques work. 

If you're bogged down with inefficient or useless meetings, I suggest that you try applying these principles to a meaningful subset of your decision making activities. People will need to hone their skills to work efficiently in this way, but the rewards can be huge for distributed teams.

## Appendix: Mailing lists at the ASF
At the ASF we use mailing lists as our central asynchronous communications channel, based on our _if it didn't happen on the dev mailing list, it didn't happen_ rule [2]. Mailing lists might be seen as tools of the past when you compare them with the latest shiny tools, but they remain a ubiquitous way of communicating in loosely coupled remote groups, especially when used with a strong discipline of _Precise Quoting_ [3] and paying attention to meaningful subject lines. Unfortunately I hear some "modern" email clients make a mess of that quoting - just stay away from them.

## References
* [1] http://www.paulgraham.com/makersschedule.html - Paul Graham, _Maker's Schedule, Manager's Schedule_, July 2009
* [2] https://community.apache.org/apache-way/apache-project-maturity-model.html - The Apache Project Maturity Model, ASF community development team, 2015.
* [3] http://s.apache.org/gianugo_quoting_2002 - Gianugo Rabellino "[OT/Rant] Quoting", message to the cocoon-dev mailing list, January 2002
* [4] http://www.apache.org/foundation/voting.html - ASF voting rules, created in 1999 probably, or even earlier among the Apache Group.
