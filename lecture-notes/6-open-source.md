---
layout: page
title: Discussion - OSS
permalink: /lecture-notes/6-oss
parent: Calendar
nav_order: 6
---

# Discussion: Open Source
These notes roughly capture the (mostly unedited) comments from the class:

1. Review course requirements:
	1. *Individual* Reflection Paper (proposal with reading list: Feb 7, ~2500 word final document: Mar 14, Mar 14 & 16 presentations)
	2. *Group* Project (Feb 23 preliminary proposal, Mar 2 final proposal, Mar 28 status update, Apr 18 report, Apr 18 & 20 presentations) 
	3. In-class participation (attendance, completing polls, participating). 
2. Review course grading:
	1. Each of the above 3 aspects gets an overall grade: Check-, Check, Check+
	2. Paper and project each have extremely detailed rubrics
	3. Participation: Can miss up to two weeks with no penalty
	4. Earn at least check on all 3: A
	5. Earn at least check on 2: B
	6. Earn at least check on 1: C
	7. +/- are discretionary
	8. All grades manually computed at end of semester, do not rely on Canvas averages
3. Poll and high-level discussion: OSS
	1. Poll will ask for evaluation on two dimensions: https://pollev.com/jbell
		1. Significance: Do you think that there is a practical impact of this study? (We will discuss those impacts)
		2. Soundness: Do you think that the methods are appropriate, and that the results support the conclusions that are drawn?
	2. Forking paper:
		1. Significance
			1. Interviews on collaboration interesting and can have relevance
			3. Avoiding hard forks is interesting, but not the main focus of the article
			4. Good contribution for learning about forking, history, implications, etc. 
			5. There has been a significant increase in forking (good), increase in OSS, collaboration (good), increase in hard forks (?)
		2. Soundness
			1. How to interpret response rate? What conclusions to draw?
			2. Heuristics-based classifiers for detecting social forks vs hard forks, hard to tell exactly what the heuristics optimize for, whether it is even possible to make a clear classification
	3. Open source donations
		1. Significance
			1. Selection of platforms (can't make claims beyond what they studied)
			2. Interesting conclusion that there is not a significant correlation between level of activity and donations
			3. What is the right question to ask here?
				1. Over what time period to consider activity?
		2. Soundness
			1. Are there strong confounds: projects only ask for money once they are already in a relatively mature phase?
			2. Using only public artifacts vs interviews/survey
			3. RQ5: How was the money spent?
			4. Compares across domains
			5. Volume of donations, value of donations, amount activity really varies by project AND by domain
4. Broader OSS discussion/community issues
	1. What are the expectations of community members
		1. Contributors
			1. Contributions to be accepted?
		2. Users
			1. Bug-free?
5. Forking
	1. There is a spectrum between hard forks  and social forks
	2. “We started as a social fork, then it became a hard fork”
	3. “Significant increase in forks” - but short-lived
		1. How to make forks sustainable?
	4. What are our own experiences about making a fork?
		1. Merging back upstream?
		2. Intentional not to merge upstream: a feature just for us
		3. “Successful PR” - make the fork, then merge upstream
		4. “I just had to make a fork of the class project”
	5. What are the motivations for project maintainers to NOT merging in a PR?
		1. Supply chain attacks
		2. Maintenance burden
		3. Vanity [or maybe something is intentionally snapshotted]
		4. It is not a feature that we want
		5. Licensing conflicts
	6. What are the motivations for project maintainers TO merge them in?
		1. Diversity the volunteer pool, bring in new talent
		2. Free bug fixes
		3. What about a “disruptive innovation?”
			1. Creativity, community contribution
			2. Build on top of existing projects to make something new/bigger
		4. Forks can increase the utilization of the overall project
			1. That fork might have its own pool of users, contributors, etc. WebRTC
	7. Methodology:
		1. Is there a more objective way to determine hard forks, OR: is it OK, OR: should we change the question to be easier to answer?
			1. Maybe this should be a non-discrete (Not hard/social)?
				1. Based on a metric based on the flow of changes in both directions
			2. Maybe the study is interesting without the “hard fork” part?
				1. (“We found that the stigma around hard forks is mostly gone”)
	8. Results:
		1. “Hard forks are not likely to be avoidable”
		2. Community fragmentation is problematic… could we measure that directly?
			1. Forks, new projects, projects that just don’t happen
		3. What about community/governance models?
			1. It is organic.
			2. What is GitHub’s role in governance? (Nudging)
			3. BDFL vs hierarchy
6. Donations:
	1. Did the decision of the authors of the donations to not interview developers cause them to miss out on significant information?
		1. This is a difficult topic to discuss and get answers on
		2. This is a possible topic to get valid/good answers on, but it is _hard_ and time consuming to do right
	2. Other soundness complaints:
		1. Bitcoin
		2. Projects supported by a foundation?
		3. Other support mechanisms (paid version vs free version)
	3. Other significance complaints:
		1. We really want to compare self-run donations vs other funding sources
		2. “How are they spending the money” - this is a philanthropy-rooted question, maybe turn to that research
		3. What is the level of funding that is needed to sustain a project?
			1. Bringing funding in to a project may have unexpected outcomes (again, look to philanthropy research)
	4. Methodology
		1. Is this “look at open source projects” and then follow-up with interviews a good methodology overall?
			1. Good, but hard to draw general conclusions
			2. Can be very limiting based on the selection of data sources.
				1. OK with just using GitHub?
				2. OK with just using OpenCollective?
			3. There are non-open-source collaboratively funded projects that are excluded from such a study (e.g. games)