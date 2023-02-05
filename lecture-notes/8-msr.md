---
layout: page
title: Discussion - MSR
permalink: /lecture-notes/8-msr
parent: Calendar
nav_order: 6
---

# Discussion: Mining Software Repositories
These notes roughly capture the (mostly unedited) comments from the class:


## General discussion
#### When is a study "exploratory" vs "definitive?"
* Even if you say "exploratory" people still jump to conclusions
* Depends on the context, maybe
* Transparency in data/results/study can help future work to confirm/refute/clarify

## Discussion: "The Promises and Perils of Mining GitHub"
#### What is wrong with using GitHub for personal projects, wrt perils?
* Heavily dependent on what you are trying to study - "well-engineered" vs... personal
	* Not "wrong" to use GH for personal projects, but maybe bad to assume that they are well-engineered. In fact: having a dataset of these "less engineered" projects could be useful for some applications
	* "Contaminates data" - across categories
* The purpose of GitHub is not to provide a database for mining :)
* There are a variety of ways to "sanitize" the data: Committers, commit frequency, recency, presence of forks/pull-requests/issues

Perils of linking issues with code: Biased samples based on population, bugs in bug trackers aren't all bugs, commercial projects != open source projects, large sample size "might" help

GHTorrent - an interesting resource

#### Study design
* 1,000 GH users get an open-ended survey, 240 responses
	* relatively small, biased to those who had published their emails
	* would bigger survey result in different conclusions?
	* reach saturation?
* Qualitative analysis of metadata
* Manual analysis for 434 projects

#### The perils
1. Repository != project
	* Forks
	* What about those 11k commits in forks not merged into upstream?
2. Activity is measured in commits
	* Most projects have very few commits
3. Most projects inactive
	* What is "active" - commit in past 6? months
	* Should we measure activity in terms of users? (How to measure usage, how to correct for popularity)
		* Note that "inactive" != "dead" - maybe important to distinguish "used" and "active" and "alive"
	* Most active 2.5% of projects account for remaining 97.5% of projects
4. Large portion of repos not for software development
	* used just for storage. Configuration files, resumes, datasets, etc.
	* not "well engineered projects" but something else
	* Static websites
	* "Assets" other kinds of blobs, etc.
	* Books ("books as code")
5. 2/3 repos personal
	* 90/240 respondents said they use GH mostly for personal projects and not with intention to communicate
	* Maybe connected to the response rate/bias here - who posts email/responds/has social projects?
	* Followed-up based on quantitative analysis of how many commiters there are
		* There are personal projects that have multiple fly-by committers
		* There are significant community projects who primarily have single committers
7. PRs are valuable, but not used everywhere
8. PRs can be reworked and lose discussion
9. Most PRs appear non-merged even though merged
	* Could this be a UI problem, now fixed?
	* Can lead to inaccurate data for studies that look at what drives "success" in merges
	* Bot PRs
10. Many active projects don't use GitHub exclusively 
	* Mirrors
	* Hard to expect everything in one place

#### The promises
* PRs are valuable source of data
* Linking developers, PRs, issues and commits

Things that are absent:
* Mining the CODE itself
* Repository templates - where does this fit?
	* Forks that you cannot tell are forks

## Discussion: "A Large-Scale Comparison of Python Code in Jupyter Notebooks and Scripts."
* Motivation/intro
	* Jet brains research
* What are interesting questions to ask of large-scale notebook datasets?
	* Is code in notebooks different? (Procedural vs exploratory)
	* Is the code written for different reasons?
	* How many users have both (we can link committers!)
	* How often are notebooks used collaboratively vs individually?
	* What are the most popular languages that are used for notebooks?
	* Are notebooks "actively developed" in the same way of non-notebooks
	* Who is using these tools, and why? (Students, domain scientists,...)
	* Is the style of the code different depending on the context?
	* Why migrate to and away from notebooks?
	* Examine which libraries are used in the notebooks, cluster usage, popularity, etc
* Methodology
	* Metrics
		* Structural metrics
			* Number of built-in functions, user-defined functions (definitions? usages?), API functions
			* Cyclomatic complexity - proxy measure for understandability. (Maybe some confounding things)
			* Number of imported functions
			* Cell coupling
				* How many variables are referenced between cells
			* Extended comment LOC
				* Comments + markdown lines
		* Stylistic metrics
			* Linters
			* Only ran linters on 100k files
			* How slow was this to run? Why was that the case?
	* Datasets
		* All jupyter notebooks in Nov 2020 (9.7m) excluding in fork repos
			* Took 1 month
			* 1.7m projects
			* Only python notebooks: 8.3m
			* Filtered to only those with "permissive" license: 847,000
				* "Copyleft" - if you change the code and distribute the compiled code you must give away your changes to source
				* "Permissive" - do whatever you want
			* Sampling?
				* They included all that met these criteria?
		* Compare notebooks to non-notebooks:
			* 10k most-starred projects on GH with permissive licenses
			* Sampling?
				* Treated every single file separately, didn't weight per-repo
				* What KINDS of projects are these?
	* Results
		* "Has no effect" linting rule is not helpful, it occurs widely
		* "Uses the same variable name" repeated IS something where there might be a helpful intervention
		* Jupyter notebooks "are more error-prone"
			* Were the non-notebook files listed normally?
			* Also has to do with the use cases 
		* Function usage and complexity?
			* Far fewer functions in notebooks than scripts
			* More usage of functions/APIs in notebooks than scripts
			* Implications?
				* Different programming models wrt structure
		* Notebooks were longer
			* Notebooks might "drag" on and on [let's look at evolution!]
			* Diff'ing notebooks :'(
		* Are there raw numbers?
			* Invalid statistical tests

