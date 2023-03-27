---
layout: page
title: Discussion - DevOps
permalink: /lecture-notes/17-devops
parent: Calendar
nav_order: 10
---
# Discussion: DevOps (Canopy & Evolutionary study of configuration in cloud)
These notes roughly capture the (mostly unedited) comments from the class:
## Agenda:
1. Administrative reminders
	1. Reflection paper feedback and grades posted, reminder of [course grading policy](https://neu-se.github.io/CS4910-7580-Spring-2023/policies/#grading): 3 checks -> A, check+ doesn't impact grade
	2. Project status update due Tuesday, 11am
	3. Weeks 13 and 14 readings updated as discussed on Tuesday
2. Follow-up and lingering questions from Tuesday's DevOps lecture
3. Poll (https://PollEv.com/jbell)
4. Discussion: Canopy
5. Discussion: An Evolutionary Study of Configuration Design and Implementation in Cloud Systems


## Discussion: Canopy
* What is the problem that they are solving? What is the world that this system lives in?
	* What caused a crash? When you add 10 features at once, it is important to be able to precisely debug things
* What is hard about this, and makes it not just Log4J? (Or any other logging framework)
	* Performance debugging is hard - unobservable (make it observable)
	* Hard to correlate log statements, particularly across distributed system
	* What is the right level of granularity to use for logging: downsides are that too much takes too much space, too hard to understand
	* Logging is increasing attack surface
	* LOTS of concurrent debuggers, all trying to measure different things
* What is the methodology for doing this debugging?
	* Determine what it is potentially causing a problem, and then determine where to insert some tracing probes, and then insert them
* What is the design space?
	* Want to decouple: "How to determine what to log" from "what is the problem that we need to troubleshoot?"
	* Look to create a system for decision support for testing hypotheses 
	* If we do not know where to put logging statements (based on the problem that occurs), where do they go?
		* Propose putting them in core blocks/areas - the model is really "log everything"
			* Provide an API 
* What are the downsides of "log everything"'
	* Hard to maintain performance -- 1.16GB/sec
	* Capture a "Trace"
		* For a request: when the request enters system, assign an ID, for every component that processes that request, store log entries, along with the ID
		* Directed acyclic graph with dependencies
		* "Trace is sharded across backend processing pipeline by TraceID"
			* Can have a pool of 100 servers, assign a traceID to each server
			* After trace is captured, flushed to processor
			* SCUBA database stores the underlying log files  
	* Hard to analyze/gain insights
		* Start by isolating to analyze in specific components
		* Start by reducing the dataset ("feature extraction lambdas")
	* How to use as a developer debugging?
		* Examine data with extracted features, or create new feature extractors
* Design requirements that they fit within:
	* Don't know in advance what we need to log or ask about
	* Don't want to have to maintain a data format
		* Not worth it in terms of space: but also in terms of coordination
	* Have to deal with a lot of different execution models
		* Server vs browser vs iPhone
			* Many requests on one server vs single thread of JS in browser vs device limitations
			* Constraints wrt bandwidth, power etc 
* Evaluation
	* Canopy is a better tool than X?
	* Canopy doesn't make my site too slow?
	* Canopy is useful? Do developers like it?
		* Reliance on case studies
		* It seems like it works
		* How could you even do a user study?
		* Is it still in use? How has it evolved?
		* A lot of information is better than 0 information
		* What other questions would you ask to study the interface?
			* If you were pitching Facebook: "Let's make the interface for performance debugging better" what is that study?
				* Find places where we found bugs before, do an A/B trial with the new and old interface to see ability to find the bug
				* Fix the hypotheses: tell the engineer "here is the hypotheses you are trying to test" and see how long it takes and with what accuracy the human can test that
				* Baseline: Compare aggregate traces to the raw ones?
	* Does Canopy scale to Facebook?
		* Yes
		* "We tolerate more latency the further the latency is from us"
			* OK to be worse on phone browser than on server
			* "It is worth it" if it solves bigger problems

## Discussion: An evolutionary study of configuration design and implementation in cloud systems
### What are the big-picture questions that this study aims to answer?
* What is the current state of practice in the interface for configuring systems?
* What are the objects that they study?
	* 4 open-source applications
		* The configuration interface
		* The usage of those configuration values within the application
		* The documentation of those configuration options
		* OK with it being all Apache?
			* They *are* widely used
* What is the overall story for significance?
	* Configuration design is something that should be considered a first-class software engineering problem
		* We should automatically check configurations after reading them in
		* Alarm-bell paper: "Facebook and google both had 15% of their failures come from misconfigurations!" But: developers of configurable software are not checking this carefully
* Methodology: How to find changes to these projects that impact configuration values
	* Keyword search for issues (and do manual examination)
	* Search the content of diffs for configuration-related keywords
	* Look for changes to program regions that use configurations
	* Might miss some "deep" aspects in the code that 

Not a question in this article:
* How do configuration files used in deployed systems evolve over time? 
	* Maybe could then improve the software as a result
	* Undocumented parameters are a horrible idea
	* What causes people to stray from the defaults?
* Is it important to study configurability?
	* Yes, because it goes to usability
	* But what systems?
	* What are actual configurations that induce failures?
* What is the relationship of configurability between open source and proprietary software?
	* What does the SQLite dev team think of this kind of configurability study?
* What for next time?
	* IaC over configuration?