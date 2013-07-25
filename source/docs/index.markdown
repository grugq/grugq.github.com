---
layout: page
title: "Docs"
date: 2013-04-01 04:39
comments: false
sharing: true
footer: true
---
The paper's I've written over the years.

- **[Cheating the ELF: Subversive Dynamic Linking](subversiveld.pdf)**
	A paper explaining the ELF format and how to abuse the dynamic linker
	to access library code.

- **[Armouring the ELF: binary encryption on UNIX platforms](phrack-58-05.txt)**
	My first article for Phrack. Describes some techniques for encrypting
	binaries on Linux. This was an important issue at the time as hacker 
	groups were trying to stem the leak of private exploits. There was 
	also the problem of exploit code being discovered in the wild and the 
	bugs dying. This was an attempt to lock down access to the exploits, 
	as well as the information (i.e. the vulnerability) contained within
	the exploit. My implementation used the subversive linking technique
	from the previous paper.

- **[The Art of Defiling: Defeating forensics analysis on Unix file systesm](phrack-59-06.txt)**
	The ur-text of anti-forensics. Few people seem to have understood what
	was actually in here. After the publication of this article I was 
	forced to resign from @stake. The techniques in here are still valid
	against some modern forensics tools. The core take aways though should
	be the basic strategies of anti-forensics. 
	
- **[Bypassing 3rd party Windows buffer overflow protections](phrack-62-05.txt)**
	This paper explores a large number of ways to bypass HIPS systems that 
	are bolted onto an operating system, rather than baked in. Mostly 
	techniques for skipping the hooks which transfer execution into the 
	HIPS logic. This article was written by myself and Eugene, with the
	NT syscall shellcode provided by jamie butler. We'd all done similar
	research, so decided to collaborate on a paper. At the time, Eugene
	and I both worked for HIPS companies so we decided to publish
	anonymously to avoid any problems.

- **[FIST FIST FIST Its all in the wrist](phrack-62-08.txt)**
	This was my final anti-forensics paper. I don't believe there has been
	anything which advances the core theory of anti-forensics beyond this
	paper. I now know that I was developing counterintelligence theory from
	first principles. Slow going. This paper deals primarily with in memory
	execution techniques for Linux. It covers some important anti-forensic
	principles as well, in particular minimizing the operational fingerprint.

- **[Userland Exec](ul_exec.txt)**
	A quick little paper for a quick little project. At the time someone
	had posted an implementation of userland exec to bugtraq which simply
	copied a binary into the stack and jumped to the entry point. Mark Dowd
	asked me how this would be done "properly", and in the process of 
	explaining it to him, I decided it would be easier to just write a PoC. 
	So, that weekend I banged out a PoC of ul_exec() and wrote up a paper
	on how it worked. It was a useful technique for anti-forensic tools as
	well as it enabled pulling a program out of an encrypted data store and
	executing it without creating a clear text version on disk. 
