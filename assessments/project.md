---
layout: assignment
title: Implementation Project
parent: Assessments
nav_order: 2
description: Description of Course Project
due_date: "Thursday April 20, 11:59pm ET"
---

# Implementation Project
The project will involve a hands-on application of the techniques and tools that we discuss in class, and can be completed either individually or in a group of at most three. Topics for the project will be discussed in the first six weeks of class, and your specific project topic will be finalized soon after. Both research-oriented projects (which implement and evaluate some new idea) and engineering-oriented projects (which make contributions to tools that developers may already use) are welcomed. All projects must involve the implementation of some software artifact (e.g. building a new system, extending an existing one, or developing scripting to automate the evaluation of some system). 


## Sample project ideas
* AFL++ describes numerous engineering improvements to AFL that make a significant improvement to AFL. There are a number of fuzzers written in other languages, targeting code in Java (e.g. [JQF](https://github.com/rohanpadhye/JQF) and [Jazzer](https://github.com/CodeIntelligenceTesting/jazzer)) in Python (e.g. [Atheris](https://github.com/google/atheris), plus surely many more). Implement one of the features of AFL++ for one of those fuzzers, and evaluate the performance improvement on the fuzzer
* Exploring mutation testing with flaky tests
* Combining fuzzing with test harness generation
* Build a fuzzing harness for Java web apps

We will add to this list throughout the first few weeks of the semester, and students are welcomed to propose project ideas that aren't from this list. Course projects that build on or extend students' projects from outside of the course are welcomed.

You will have four primary deliverables for the project: 1) a proposal outlining your project, 2) a mid-semester status update, 3) a final report describing your project experience, and 4) the actual software artifact that you created in your project.

## The Project Proposal
The project proposal should explain, at a high level, the project that you have in mind. The proposal should address the following points:
1. Describe the goals of your project: are you seeking to develop new functionality for an existing application, develop a greenfield application, or evaluate some existing system?
2. What will be the concrete deliverables that you create?
3. If there will be an evaluation aspect, what metrics will you capture? 
4. What technologies will you use?
5. What are the major risks that you see in the project that you are proposing? Do you have contingency plans in case some key aspect of the project doesn't work out?

The proposal should be roughly one page long, although if you find it useful to include figures, or additional text, that is OK, too.

The project proposal is due on February 16th at 11:59pm, submitted via Canvas.

A good-faith, on-time attempt to answer the questions above is necessary to receive a "check" on the project overall (see overall project grading rubric below).

### Proposal re-submission
If your project proposal is submitted on time, but is not sufficiently detailed that I can judge whether your project is feasible or not, I will provide you with detailed feedback, and ask you to re-submit the project proposal. If you then re-submit the proposal, this will not have any negative impact on your grade.

## The Project Status Update
The project status update should reflect on the progress that you have made thus far and outline the work that remains to be done on your project. 
The status update should address the following points:

1. What have you accomplished? Include a link to the code that you have written so far.
2. What challenges have you encountered?
3. Are there any difficulties that are currently preventing you from making progress?
4. What tasks do you still need to complete?
5. Do you believe that your original proposal is still feasible? If no, what modifications to your original proposal would make it more feasible.

The project status update should be roughly 2-4 paragraphs long.

The project status update is due on March 16th at 11:59pm, submitted via Canvas.

A good-faith, on-time attempt to answer the questions above is necessary to receive a "check" on the project overall (see overall project grading rubric below).

## The Project Report
In addition to producing a code artifact (e.g. your project implementation), you will also write up a final project report that describes your experience implementing and evaluating your project. The maximum length of the project report is ten pages, not including figures and/or references. As they say, "a picture is worth a thousand words" --- we expect that there will be at least some figures in every project report (e.g. architectural diagrams, screenshots, evaluation results, etc.). Please consider ten pages as an absolute upper-bound on length: shorter may be better than longer, and a 3-5 page report that contains everything that we need to know is fine.

The final report should contain the following sections (feel free to add additional sections; the sections below are required):

### Introduction
Describe the project that you proposed (assuming that the reader of this report hasn't read your project proposal). It is fine to copy and paste text from the project proposal here, if that text still applies. However, if you have made changes to your project topic based on feedback on the proposal, or based on experiences working on the project, be sure to describe here what you *actually* did, and not just what you originally planned to do.

### Project Results
Considering the overall project goals that you proposed, present the results or findings of your project, describing in detail what you learned from doing the project. Describe the technologies that you used, and how you used them. In this section, focus on goals that you successfully achieved, or that failing, concepts and technologies that you learned. If your project builds upon existing code, frameworks, scripts, tools, etc. built by you or someone else, be sure to clearly differentiate the work that you implemented for this project in this course, as opposed to work you or others may have done previously.

### Project Challenges
While it is possible that you successfully implemented your entire project without any challenges, it's quite likely that you ran into a variety of challenges along the way. In some cases, you may have even discovered that the overall goals that you set out to achieve are simply not attainable (or at least, not attainable in the time frame allocated). That is absolutely fine, and for better or worse, is the price of working on research problems: if we knew the answer to these problems already, they wouldn't be research!

In this section, you should describe in detail challenges that you encountered, and what you did to try to work around them. If you ran into implementation-level challenges (e.g. difficulties with particular technologies, unescapable segfaults, etc) describe your hypothesis for *why* you might have run into this challenge, and any steps that you have taken to try to test that hypothesis/debug the situation. This section provides an opportunity for a project that has no working implementation at all to still receive a grade of "check" - if you could never get the project to work, but can describe various steps that you took to debug your project, you are still creating an artifact that demonstrates your understanding of advanced software engineering processes.

## Final Project Submission
Create a zip file with your entire implementation, and create a PDF with your report. Submit both on Canvas by April 13th at 11:59pm. No late submissions will be accepted. 

## Grading Rubric
Your project will be graded on the scale of (Unacceptable, Check-, Check, Check+). The criteria for each grade are described below:

To receive the grade of **Check**, the project must satisfy all of these criteria:
* The project proposal is submitted on time. The proposal is roughly one page long and includes a good-faith effort to address each of the 5 points outlined above.
* The project status update is submitted on time. The status update is roughly 2-4 paragraphs long and includes a good-faith effort to address each of the 5 points outlined above.
* The project includes a response to any feedback provided on the proposal: for any changes requested by the instructor, either those changes were accepted, or there is a discussion in the report of why those changes did not make sense.
* The project report is between 3-10 pages long, contains at least the three sections outlined above, and captures your efforts on implementing your project
* The project report and implementation are submitted on time
* EITHER:
	* 1) the project implementation successfully achieves the goals outlined, OR:
	* 2) the "Project Challenges" section of the report describes in detail the challenges that you faced that prevented you from achieving some goal(s), and the steps that you took to try to overcome those challenges. The record of steps that you took to overcome those challenges is sufficiently detailed to demonstrate that you put a good-faith effort into getting it to work. The project status update supports this narrative.
	
To receive the grade of **Check-**: the project must satisfy all of these criteria:
* The project proposal is submitted on time. The proposal is roughly one page long and includes a good-faith effort to address each of the 5 points outlined above.
* The project status update is submitted on time. The status update is roughly 2-4 paragraphs long and includes a good-faith effort to address each of the 5 points outlined above.
* The project report is between 3-10 pages long, contains at least the three sections outlined above, with a good-faith effort to respond to the prompts.
* The project report and implementation are submitted on time
* The project implementation may not achieve all of the goals outlined, the project challenges section may not include a detailed discussion of the challenges encountered and good-faith attempts to overcome those challenges.


Submissions that do not meet the criteria for "Check-" will receive the grade of "Unacceptable." Submissions that exceed the qualities outlined for "Check" may receive the grade of "Check+". As per the course policies, note that a grade of "Check" is sufficient to receive an A in the class.
