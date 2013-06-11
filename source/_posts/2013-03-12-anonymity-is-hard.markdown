---
layout: post
title: "anonymity is hard"
date: 2013-03-12 21:05
comments: true
categories: OPSEC
---

Anonymity in the real world is very hard
----------------------------------------

In late 2011 Hezbollah rolled up a CIA spy ring in Lebanon. This provides an
interesting lesson in CIA tradecraft and real world counterintelligence. Close
examination of the techniques used to track down the agents will reveal some
serious problems with many systems designed to provide security for
anti-government groups.

This post is partially in a response to [Matt Green's](http://blog.cryptographyengineering.com/2013/03/here-come-encryption-apps.html) 
post about encryption apps. The secrecy provided by encryption applications,
primarily privacy of communication content, is not sufficient to protect against 
even minimal monitoring. Any anti-government activity in a modern environment, e.g.
one involving mobile phones and the internet, needs to include anonymity first and
foremost.


The Sources
-----------

[This article](http://www.guardian.co.uk/world/feedarticle/9958834) provides
some of the details about the tradecraft of the spy network, and how it
failed. The focus is on how the agents were contacted by their handlers and
how this was used to uncover the whole network. [Another site](http://www.ufppc.org/us-a-world-news-mainmenu-35/10702-news-three-us-spy-rings-broken-in-lebanon-a-iran.html) 
provides a large collection of related articles which fills in some additional
details.


The Tradecraft (Probably, maybe)
--------------------------------

**NOTE:** This information is based on newspaper articles, so it is of limited
accuracy. However, it seems like reasonable tradecraft practices that even
amateurs would devise and is thus presented for analysis here.

- **Dedicated mobile phone**
	The agents had a mobile phone used specifically for communication with
	their handler. This phone was kept in a static location waiting for
	contact, and possibly spent a lot of time switched off.

- **Pre-arranged meeting place**
	The agents had a meeting location (allegedly at a Pizza Hut) where
	they met their handlers. This location was (allegedly) reused for
	multiple agents and multiple meetings. 

- **Signalling code word**
	Contact by the handler to the agent was via a code word (allegedly: "PIZZA!"),
	which was meaningless by itself but also contextually anomalous.


Well, thats one way to do it
----------------------------

The adversary, Hezbollah, used access to the telephone company logs (they have those),
and searched for atypical mobile phone usage patterns:

- phones that only receive a few calls / messages over long periods of time
- mobile phones that are never mobile
- weird / unusual messages (PIZZA!!)

That is, they were looking for phones that were kept at home, turned on
occasionally, and only received calls/sms infrequently. The exact usage pattern
one would expect for a mobile that is used exclusively for a handler to contact
an agent.

This data gave Hezbollah a general location (down to the apartment complex) of
where the agents were located. Next, the adversary correlated the location
data with the home addresses of members who had access to secret information.
They conducted surveillance on those members and discovered they were using a
Pizza Hut to meet with their handlers. 

**Speculation**
Finally, the adversary was able to continually monitor the meeting location
and detect other members of the spy network meeting with their handlers. The
CIA is known for over using the same locations for meetings [1].

[1] [The C.I. Desk](http://www.amazon.com/The-C-I-Desk-Counterintelligence-Cubicle/dp/1608447391)


Computer says No
----------------

The problems with these tradecraft practises are pretty obvious from a
counterintelligence analysis. They are anomalous (atypical mobile phone use)
and they are rigidly predictable (reusing the same meeting location).

For encryption applications used by anti-government forces this provides a
clear blueprint for action - look normal. Even basic monitoring of traffic
will reveal anomalous activity which can be used to identify who needs to be
watched more closely.


Conclusion
----------

Hiding anomalous activity is hard, but vitally important. The problem with
many security systems based purely on secrecy is that their usage is itself
anomalous. It singles out and attracts attention to the users. If the
adversary doesn't know who those users are initially, they can cross correlate
real world data with the suspicious activity and narrow their focus to real
people. Those people can, and will, end up dead.
