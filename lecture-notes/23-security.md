---
layout: page
title: Discussion - Security
permalink: /lecture-notes/23-security
parent: Calendar
nav_order: 14
---
# Discussion: Why Secret Detection Tools are Not Enough & Course Postmortem
* Secret detection in code repositories
	* What is this?
		* Detect passwords that are put into code
		* Examples of password needed: To connect to external APIs, databases, etc
	* How do we detect secrets?
		* Need to look back in history to find everything (if this happens to you, check: ohshitgit.com)
	* Why do the authors say this is important?
		* The keys are put as plain-text - anybody who gets access to this repository in the future will get access to this secret
	* What do you think about this being important?
		* A better fix is to have secrets that are short-lived, and hence, their disclosure is not *horrible*
		* Developers are not sufficiently focused on security - we need defense in depth
			* "If this gets discovered it's not a big deal" - This judgement should not be left to the masses. Great exploits are usually a chain of smaller exploits, and care should be taken in providing footholds
		* What about a key management system, e.g. Hashicorp vault
			* Complicated
			* Adds friction
			* Many different tools, need tool-knowledge, not just conceptual knowlddge
			* Oh wait, you also have to decide how to configure it (who gets what keys? the social/organizational problems…)
		* Experiences with secret detection tools
			* APIs that are proactively crawling GitHub looking for their keys
			* GitHub’s GitGuardian scanning
			* From the old days: the $14,000 mistake of sharing an AWS key
			* The scope of this problem is huge - auditing is not easy (especially finding all of them).
	* What are the objectives to this study?
		* How often do devs bypass warnings?
		* What is density of checked-in secrets by-file?
		* What is the distribution among developers that are checking in secrets?
		* Why do developers ignore the warnings?
		* Goal: Motivate developers to NOT ignore the warnings
		* Goal: Make tools better to generate less false positives
		* “We have a budget of 10 warnings a day”… Lacework
	* What is the methodology?
		* Conduct a study in XTech
		* How could/should this study be designed to ensure trasnferability?
			* Still have humans in the loop… 
			* Survey + qualitative findings described in context can transfer (must have sufficient context described)
	* Results + implications?
		* How often do devs bypass warnings?
			* 51.4%
				* These are “potential” secrets, some may be false positives!
				* What about results of actual outcomes: the investigations
			* What does “bypass” mean here?
				* Continue uploading to VCS regardless of warning
				* “One time bypass”
				* “Permanent bypass”
		* Why do developers ignore the warnings?
			* Believe that there is no significant damage
				* Not a production credential
					* They will forget to remove it, maybe it becomes a production credential one day
					* Could allow an attacker lateral movement in an organization 
				* No significant data exposed
					* Whose decision is this to make?
			* It wasn’t me, I am just a refactorer
				* Maybe this one is the least bad :)
				* Maybe you should have a policy that is: if you come across it, you have to fix it.
			* There is a difficult-to-quantify risk here: someone higher up than the dev needs to make the call to determine whether resources should be allocated to fixing this or not?
		* Why can’t secrets be promptly removed?
			* Cost + training
			* Cost -> Requires organizational buy-in to this as a priority
		* What are solutions?
			* Train developers on alternatives to hard-coded secrets
			* Organizational support for this problem
			* Include this paper in software engineering security lectures
			* MAKE A LINTER THAT SHOWS A RED SQUIGGLE IN VSCODE THE MOMENT THAT YOU DO THIS
		* Impact/value of the survey?
			* Provides clear qualitative results about the problems faced by the deployment of secret development tools
	* Is this a good methodology to take to evaluate all of our software engineering tools?
		* Put tools in front of developers, have them use it, collect survey results as to “is this helpful”
			* Helps to elicit ways to improve interface/integration with developer workflows
		* For earlier-stage experimentation, also perform observational studies
		* Evaluation of the tool needs to also consider the entire context of the problem - not limited to the tool or the developers - in this context, we should also measure things like security outcomes

# Course Postmortem

## Top papers and bottom papers poll in PollEv
Sometimes the papers that we were the most critical of led to the best discussions. Update poll next time to clarify top means "more time on this" and bottom means "less time on this, or not at all"

## Other topics to cover
* Ethics
  * Discuss case studies - powerful examples to motivate further discussion
  * Value sensitive design?
  * Find papers/studies that involve cultures that are typically not studied in research literature
* ML/AI - MLops, SE for AI, AI for SE, LLMs, etc
  * Background ethics discussion
  * GitHub Copilot + generally LLMs of code
  * Testing + AI
	* Testing LLMs
	* Using LLMs for testing
* DevOps overall
	* What happens when you start deploying the product?
	* SLA, uptime guarantees
	* Disaster recovery
    * More infrastructure as code
* Reproducibility + maintainability in experimental software
* Including discussions of social justice, equity and diversity throughout the class, not just in a single meeting

## Class format/participation etc
* Lukewarm on the idea of having a weekly deliverable
* Students sign up to present papers
	* A particularly good approach for focusing on a specific research interest
* Reflection paper?
	* Provide more precise specification, especially about the degree to which each paper needs to be covered
	* Drop the requirement for papers from the class (still strong suggestion on topics) - but can still use a paper from the class
	* Add a paper swap/peer review
* "Advanced Software Engineering II"?
