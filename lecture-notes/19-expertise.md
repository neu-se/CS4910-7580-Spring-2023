---
layout: page
title: Discussion - Expertise
permalink: /lecture-notes/19-expertise
parent: Calendar
nav_order: 12
---
# Discussion: What makes a great software engineer & Programming Strategies
These notes roughly capture the (mostly unedited) comments from the class:

## What makes a great software engineer?
### Why is this a question that we should ask?
* It could be actionable: if we know what makes a software engineer great, we could create training and processes to develop those
	* And when you notice in yourself, you could focus on that
	* (And focus hiring activities - especially in lower level positions where we are hiring based on potential)
	* Need to do a *broad* survey to capture not just technical attributes
	* Helps to recognize the limitations of software engineers, and understand what a reasonable ask is
	* Helps to inspire future technologies or tools to manage that development
	* Important to distinguish "software engineer" vs "programmer"
* What is the difference between "what is a good software engineer" and "what is a good business worker?"
	* See the programming strategies paper: much of the knowledge may be tacit
	* Technical skills are not needed in all jobs, but what is needed in this job is the ability to collaborate between those with technical skills and the non-technical/domain skills 
	* It is easier to get outdated in the SE domain (or to simply have the "wrong" technical skills)
	* Connecting the value to the business/user to the technical work/code is hard
* Is a great SE at Microsoft a great SE at Apple (...or Chewy or Wayfair), or elsewhere?
	* Well, maybe... but the easiest way to determine this is to look at table 2 and determine whether it is adequate for the job or not
	* Different companies have different objectives, goals and aims. For small companies, especially startups engineers might need to handle a broader set of tasks. Also a big difference if the software is B2B vs B2C - different
	* Is this different based on level - startup prefers senior level engineer vs entry-level?
	* If the answer to this is no: then does that mean that one of those companies is doing it "wrong"?
		* Especially at the high level of figure 1: The emphasis on non-technical skills should generalize
		* No, it means that they are just hiring *programmers* and not software engineers
* What DOES make a great software engineer?
	* Personal characteristics - are these all intrinsic? Are any?
		* Ultimately, down to training - could be transferred through education, or through - but perhaps with greater time/resources/effort
		* Some of these are "hard lessons"
		* Some are very tied to the condition that you are in: adaptability (also passion)
		* Passion is king? Intrinsic rewards > extrinsic rewards
		* Constant drive for improvement: how do you teach this?
		* There are conflicts between attributes: someone who always wants to improve might not be a great team player (depends on the team)
		* How to implement training for this, based on different individuals' personalities/strengths
	* Team qualities
		* Should we consider people who are not software engineers to understand what makes a great software engineer?
		* Potentially great software engineers might be introverts, and not sharing enough to create team success
		* How does WFH/remote work intersect with these qualities and day-to-day activities that could benefit these qualities (but are missed)?
			* "What makes a great remote software engineer?"
		* How to recognize tacit knowledge, both to non-software engineers, but perhaps more importantly, within a team?
		* How to recognize things that can be tested (trial and error) vs must get right the first time (and have communication overhead up-front)
	* Decision making
		* Most general and applicable to other fields of business, but least emphasized in CS education and hiring
		* A lot of this is learned through *experience* and is specific to the context/team
		* Can definitely teach at least some of these skills: "What kind of animal would you be?" (More serious things here)
		* Explicit education on leadership and collaboration. Here are the learning objectives:
			* A good leader is one who can take a vacation on short notice, because their team can function in their absence
				* Counterpoint: if you want to be promoted, then maybe you need to prove that in your absence, you are missed :)
			* A good collaborator is an effective communicator, who can explain what they did to different audiences
			* A good leader creates artifacts (e.g. documentation) to enable others to succeed in the leader's tasks. Successful documentation is documentation that can be reused
			* A good leader is able to hire and supervise contributors smarter than them
			* A good leader is knowledgable AND is knowledgable about their team in order to effectively transfer tacit (and other) knowledge to them
			* A good leader has integrity
		* How to teach all of this?
			* Communication - either first-hand experience, or learned experience
* Aspects of the product
	* Things that we do teach?
	* Things that we don't do a great job teaching?
		* Evolving/long-term, how to structure software to be efficiently delivered over time

## An exploratory study of sharing strategic programming knowledge
* How does one great software engineer transfer (especially tacit) expertise to others?
* What do we think about figure 1 strategies?
	* KNOW WHO YOUR AUDIENCE IS
	* Need to understand the shared context - so that we can understand what tacit knowledge is known by the reader/user
*  Why do we have this tacit knowledge problem in software engineering?
	* Evolution - write a book, and it's obsolete
	* Maybe it's not tacit, we are just not putting in the effort to explain it
	* Software engineering is a field that allows for trial and error in ways not possible in other fields. A trainee might "succeed" on an assignment but not learn that tacit knowledge
* "If you really understand it then you can teach it to someone" - pedagogical content knowledge
* Why Roboto?
	* Shared grammar and expectations 
	* Could an LLM execute the strategy?
* Discussion
	* Would study participants have invented something else if not using roboto?
	* This is overdue.
	* What about cross-referencing strategies, so that there are "details on demand"
	* Maybe debugging is not the right application for this - it could apply more broadly
		* Or maybe it is :)
		* High level strategy: Hypothesis-driven debugging
		* Low level strategy: Create approaches to generate hypotheses
	* Relationship to expert systems?
	* We want this for cooking, and more english-y things
	* We also want to have some NLP techniques to seed the pot of strategies
	* What makes a great programming strategy author?
		* Pedagogical content knowledge, plus...?
		* We need ChatGPT + programming strategies