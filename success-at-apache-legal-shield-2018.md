Success at Apache: the Apache Legal Shield - a pragmatic view
========

Section 12.1 of the Apache Bylaws [1] describes the legal protection that the Apache Software Foundation provides to our directors, officers and members. 

I'm not a lawyer by far, however, and that language is a bit hard to parse into a pragmatic set of recommendations, so I thought I'd try to clarify what this means for our contributors.

If you go into detail there's certainly more to it than my pragmatic and simplified view below, but I think the two items below are the absolute basics that every PMC member should understand in order to benefit from the legal shield that the Foundation provides.

Acts of the Foundation
------
The first thing is to make sure our software releases are "Acts of the Foundation" as opposed to something that people do in their own name. This is natural if we follow our release policy [2], which defines a simple release approval process which makes the project's PMC [3] responsible for the release, as opposed to our individual contributors and release managers. 

This means that if the released software is ever involved in legal action and someone has to testify or produce information as part of a subpoena, it's the Foundation which is in charge of that and not our individual contributors. These things happen from time to time, not very often but they can represent a lot of work and aggravation that none of us are looking for. The Oracle subpoena to Apache [4] is just one example of that.

The goal of our release process is to make it very clear what an Apache Release is, and that anyone using our software in other ways, by getting it directly from our code repositories for example, does so at their own risk.

Developer Builds
-----
This leads to the second thing that I'd like to mention in this pragmatic and simplified summary of our legal shield: developer builds, which happen much more often than releases, often daily, and that people can easily download and use.

To avoid any confusion, it is important to clearly label these things as being meant for development and testing only, and to draw a clear line between them and official Apache Releases. Those builds should only be advertised in places where developers who are part of our communities (as opposed to the general public) can see them, and with suitable disclaimers.

In our world of continuous deployment and automated builds, the lines between what's a release and what's just tagged code that works for someone are often blurred. That's totally fine from a technical point of view, and often desirable when one wants to move fast, but we shouldn't forget about the possible legal implications ot distributing software, and make sure we take advantage of the well-designed Apache Legal Shield that the Foundation provides to us.

[1] https://www.apache.org/foundation/bylaws

[2] http://www.apache.org/legal/release-policy.html

[3] https://www.apache.org/foundation/how-it-works.html

[4] http://www.groklaw.net/articlebasic.php?story=20110509221136468
