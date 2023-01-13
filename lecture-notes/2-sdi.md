---
layout: page
title: Discussion - SDI
permalink: /lecture-notes/2-sdi
parent: Calendar
nav_order: 1
---

# Discussion: Software Aspects of Strategic Defense Systems

These notes roughly capture the (mostly unedited) comments from the class:

1. Hot Takes/First Impressions: What did you think of these essays, overall?
	1. Requirements: “Do everything perfectly”
	2. Important/interesting to discuss education of programmers
	3. Is this actually a problem of programming languages?
	4. Most (or all?) of the problems discussed exist not only for the SDI, but in other contexts too
	5. How to reason about what a reasonable/good investment is?
		1. Applied research
			1. Make the missile hit the exact target
		2. Fundamental research
			1. Make software more reliable
			2. What we needed then: concurrency, fault tolerant systems
	6. Wow, we sure had much different hardware at the time, and the difference between a high and a low level programming language…
	7. The hard requirements (never miss a target) are pretty insane
		1. Not. Ever. Possible.
	8. We have had actual documented cases of missile detection systems providing false positives that would have resulted in nuclear war had not a human intervened
2. Essays on software process
	1. Why software is unreliable
		1. Continuous vs discrete states. If continuous states, can’t test all states in advance
		2. It depends on what you want to prove and in which circumstances
		3. How do we understand software - decompose it into modules?
			1. Is it possible for modules to break down, and lead to unreliable software?
				1. Specifying WHICH module to use can be a challenge
				2. By construction, different modules must be built by different teams
				3. Concurrency/multi-processing
				4. Different modules built by different teams may be unreliable in themselves, especially if they are entirely disconnected in their development structure
		4. Software engineers are not trained sufficiently
			1. Insufficient understanding of when different methods are applicable, and under what circumstances they can be expected to generalize/continue to perform
			2. “Think like a computer” is not an appropriate teaching method
				1. Programming by trial-and-error (but this requires tests)
			3. Not good enough tooling support
			4. Higher level languages might help “think like a computer” by raising the abstraction level
			5. Rigorous training in requirements writing and decomposition - understanding in particular implicit requirements for behaviors that should NOT occur
			6. How much of this problem is related to EXPERIENCE that can’t be trained/shared, versus training?
				1. Prototyping/iterative decomposition
				2. Patterns/architecture?
	2. Why SDI will be untrustworthy
		1. “Untrustworthy” - this means not 100% perfect performance - should that just be “nuff said”?
		2. This is realistically a systems problem, not just including the post-launch phase (intelligence gathering, pre-launch capabilities, other countermeasures)
		3. Example: How to develop fire control software? What are the inputs? What are the algorithms to use? How to test this?
			1. Start with the given inputs: we have some ballistic missile that is on some trajectory
			2.  AI has gotten _so_ much further
		4. Many of the assumptions are grounded on the current state of hardware/software at the day
	3. Why conventional SW development does not produce reliable programs
3. Essays on “emerging approaches”
	1. The limits of SE methods
		1. Waterfall process
			1. At a system-level, the entire system must be correct “the first time”
			2. Requirements/interfaces between modules must be carefully gathered, designed, analyzed (Rely on experience building previous things to do this)
		2. Structured programming
		3. Formally specified interfaces
			1. What is an example of a difficult design decision that could be easily overlooked? 
				1. Constraints of execution time, space requirements for modules must be specified ahead
				2. Disconnect between project managers/engineers - particularly in terms of what is actually possible with current technology
				3. Anything related to assumptions of the countermeasures of the enemy, all of which must be based on (uncertain) intelligence (plus the fact that there might be gas in that enemy software)
				4. Implicit assumptions, e.g. on iteration over a hash table 
			2. Is a solution to this grounded in software, in humans, or in both?
				1. Some things can be solved in software. Especially discussion of multi-processing, baking these kinds of solutions into languages (e.g. Rust, async actors)
				2. Some things need to be solved in human processes.
					1. Software can be used to help mediate communication.
					2. How to organize high-level design vs low-level design?
					3. How to structure teams?
				3. Maybe most/all things are socio-technical, and depending on the problem, might be more of one side than the other
				4. Maybe we need to break bad habits?
		4. Cooperative multiprocessing using locks/signals
		5. The Software Cost Reduction project 
			1. What was learned from this 8+ year effort?
				1. Need complete black-box requirements upfront
				2. MODULES, and also why to use modules
				3. Precise documentation using formal methods (compare to “functionality over documentation”)
			2. “Every new concept requires at least 2 generations of engineers to become the standard”
	2. AI and the SDI
		1. AI has gotten pretty far compared to what it was
		2. “People speak of AI as if it were some magic body of new ideas”
		3. We have found out that many things that we thought were hard (chess) are “easy” others (recognizing blocks) hard 
	3. Can automatic programming solve the SDI problem?
		1. Even if we have ChatGPT to generate code, still need to generate prompt
		2. Helps programmer with the “simple” things, and as this is continued to be used, you eventually might generate more reliable code
		3. GitHub CoPilot is a big “wow” but not the end of the story
		4. Programs need to be _read_ by humans also: are these automatic techniques making things that are not maintainable
		5. What kind of explainability/traceability do we get from this?
		6. What about new programming languages?
			1. Garbage collectors?
			2. Programming by specification
			3. Type systems
			4. Would a higher level language lead to more reliable programs? Pros and cons...
				1. As more things are abstracted away, developer may become less aware of what is actually happening under the hood
				2. How to conceptualize “real-time” - millisecond latency is OK 
				3. Performance is harder to reason about
				4. The low-level mechanisms implemented by the high-level language *should* be correct
				5. Higher-level problems may be easier to reason about in maintenace
				6. Can actually spend time focusing on what it is that you need to do, rather than how to implement the low-level parts of it
			5. How do programming environments improve reliability?
				1. What is a programming environment in this context? (Other than Unix™)
					1. Operating system, editors
				2. What programming environments make software more reliable/faster to build?
					1. IDEs + language servers - include linting/test/analysis results directly inside of an integrated environment. Refactoring.
					2. Simulation of physical devices in virtual environments 
					3. Version control + collaboration tools
					4. Continuous integration
	4. Can program verification make the SDI software reliable?
		1. What was missing at the time? Languages, solvers, proofs assistants 
		2. What are the properties that you are going to verify?