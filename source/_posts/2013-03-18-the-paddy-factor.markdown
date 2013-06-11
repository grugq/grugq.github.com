---
layout: post
title: "the paddy factor"
date: 2013-03-18 09:51
comments: true
categories: [OPSEC, link analysis, CI]
---


The **Paddy Factor** was a disparaging term used by the British security
forces to refer to poor OPSEC practices by the Provisional IRA (PIRA)
in the early 1970s. Much of this terrible counter intelligence posture was due
to a limited number of easily avoidable activities that combined to compromise
many Provos:

- **Self incrimination**
	- PIRA members would congregate in pubs and sing IRA songs.
	- They would boast about their IRA operations while drunk in pubs.
	- They would reply with a nod and a wink to friendly inquiries about their
	  activities, making it easy for informants to identify them.
	- They would march in pro-IRA rallies.


	**Problem:** The adversary was able to easily identify (some) PIRA
	members. Once the adversary identifies members of an organisation,
	they will investigate and monitor them to uncover other members. 

- **Contamination**
	PIRA members would associate with each other when not on operations.
	In intel parlance this is called "pre-operational contact", and it is
	to be avoided. The reason is that any surveillance on one member will
	reveal the other members of the group. This is a form of *contamination*.
	
In short, some (many?) members of the Provisional IRA made their affiliation
publically known by bragging about their operations in public places. This
made them known to the adversary (the British security forces), who were then
able to monitor those known PIRA members. Later, at political events such as
rallies, these known PIRA members would hang out and chat with their unknown
underground brethren. This made the underground members known to the adversary,
with the obvious negative consequences.


Link Analysis and You
---------------------

Knowing only a single node in a network, e.g. one member of an organisation,
and monitoring which other nodes it contacts with gives insight into
membership of the graph. The police, for example, use a variety of monitoring
techniques to build up *phone trees* which map out organisational relationships.

This form of analysis, mapping associations between nodes in a network (e.g.
membership in an organisation) is called link analysis. It can be used against
communication end points (e.g. mobile phones, email addresses), which are then
associated with individuals. For example, link analysis of mobile phone numbers
and contact address books of drug dealers is used to determine hierarchical
information about their distribution networks. Link analysis is a very powerful
method of understanding relationships and being able to link "chatter" between
nodes as activity related to an organisation.


How to unlink
-------------

One solution to making link analysis harder and less useful is to create
unique nodes for each connection. Done successfuly, this creates link graph is
only 2 nodes and 1 edge. In practise, this means that every connection between
peers should be unique to that connection, i.e. create a new jabber identity for
each associate you have. Do not share these jabber IDs between different *friends*.
The rule is simple: 1 friend, 1 jabber ID. 

These node to node links should be changed regularly as well. The old nodes
must never contact the new nodes. That will contaminate them, create a link
that associates them together. New clean break each time.


Conclusion
----------

It is possible to defeat link analysis, but it takes discipline and is hard to 
do successfully. Every single communications end point must be unique and 
dedicated to only one other end point. These end points must never contaminate
each other by interacting or mentioning other end points. This will inhibit
creating a *phone tree*, or link analysis chart of organisation membership. 

**Warning:** unlinking will not prevent traffic flow analysis, fingerprinting, 
or many other techniques from linking comms end points. But it is square one.
