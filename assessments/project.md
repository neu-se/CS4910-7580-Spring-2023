---
layout: assignment
title: Implementation Project
parent: Assessments
nav_order: 5
description: Description of Course Project
due_date: "Tuesday April 18 2023, 11:00am EDT"
---

The project will involve a hands-on application of the techniques and tools that we discuss in class, and can be completed either individually or in a group of at most three. Topics for the project will be discussed in the first six weeks of class, and your specific project topic will be finalized soon after. Both research-oriented projects (which implement and evaluate some new idea) and engineering-oriented projects (which make contributions to tools that developers may already use) are welcomed. All projects must involve the implementation of some software artifact (e.g. building a new system, extending an existing one, or developing scripting to automate the evaluation of some system). 


## Sample project ideas
* Mining GitHub or other open source ecosystems to answer a software engineering research question
* Conducting an evaluation of existing software engineering tools or frameworks in a new context (compared to existing evaluations)
* Implementing new features for open source software engineering tools, for example: extensions to mutation testing tools, fuzzers, plugins for continuous integration platforms, etc.
* Creating continuous integration workflows for automated performance testing of the [covey.town](https://github.com/neu-se/covey.town) platform
* Applying continuous integration and automated testing to an existing research project

We will add to this list throughout the first few weeks of the semester, and students are welcomed to propose project ideas that aren't from this list. Course projects that build on or extend students' projects from outside of the course are welcomed.

You will have five primary deliverables for the project: 1) [a preliminary proposal outlining your project]({{site.baseurl}}/asessments/project-proposal), 2) [a revised proposal]({{site.baseurl}}{% link assessments/revised-project-proposal.md %}), 3) a [mid-semester status update]]({{site.baseurl}}{% link assessments/project-status-update.md %}), 4) a final report describing your project experience, and 5) the actual software artifact that you created in your project.


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

## Project Poster Presentation
Create a poster that summarizes your project, including the introduction/motivation, the results, and challenges. We have no specific formatting requirements for the poster, but encourage you to use the space primarily for figures/images/tables rather than for blocks of text.

To encourage interactivity, posters will be presented in two ways:
1. Asynchronously, via Discord: We will share all posters on Discord before class on the 18th. Students can review and comment on posters before they are presented.
2. During class time on the 18th and 20th, each group will provide a ~5-7 minute presentation of their poster (we will present the posters on the screen) and answer questions. 

We would like to collect posters and highlight them on the course website, allowing future students to get a sense for the kinds of projects that students have undertaken in the past. When we have done this in other classes, students have also later remarked that it was helpful for their project to be highlighted on the class website, as it provided a reputable URL that could be shared with potential employers or collaborators to simultaneously present the student's work and contextualize it within the course. Please include a statement when you upload your poster as to whether you consent to the poster being shared publicly or not. 

## Final Project Submission
Create a zip file with your entire implementation artifact. Create a PDF with your report, and a separate PDF with your poster. Submit all three on Canvas by April 18 at 11:00am (use the assignment labeled "Implementation Project" for the implementation itself, "Report" for the report and "Poster" for the poster). No late submissions will be accepted. 

## Grading Rubric
Your project will be graded on the scale of (Unacceptable, Check-, Check, Check+). The criteria for each grade are described below:

To receive the grade of **Check**, the project must satisfy all of these criteria:
* The project proposal is submitted on time. The proposal is roughly one page long and includes a good-faith effort to address each of the 5 points outlined above.
* The project status update is submitted on time. The status update is roughly 2-4 paragraphs long and includes a good-faith effort to address each of the 5 points outlined above.
* The project includes a response to any feedback provided on the proposal: for any changes requested by the instructor, either those changes were accepted, or there is a discussion in the report of why those changes did not make sense.
* The project report is between 3-10 pages long, contains at least the three sections outlined above, and captures your efforts on implementing your project
* The project report and implementation are submitted on time
* The project poster is submitted on time and summarizes the introduction/motivation to the project, the results, and any signfiicant challenges encountered
* EITHER:
	* 1) the project implementation successfully achieves the goals outlined, OR:
	* 2) the "Project Challenges" section of the report describes in detail the challenges that you faced that prevented you from achieving some goal(s), and the steps that you took to try to overcome those challenges. The record of steps that you took to overcome those challenges is sufficiently detailed to demonstrate that you put a good-faith effort into getting it to work. The project status update supports this narrative.
	
To receive the grade of **Check-**: the project must satisfy all of these criteria:
* The project proposal is submitted on time. The proposal is roughly one page long and includes a good-faith effort to address each of the 5 points outlined above.
* The project status update is submitted on time. The status update is roughly 2-4 paragraphs long and includes a good-faith effort to address each of the 5 points outlined above.
* The project report is between 3-10 pages long, contains at least the three sections outlined above, with a good-faith effort to respond to the prompts.
* The project report, implementation and/or poster are submitted on time
* The project implementation may not achieve all of the goals outlined, the project challenges section may not include a detailed discussion of the challenges encountered and good-faith attempts to overcome those challenges.


Submissions that do not meet the criteria for "Check-" will receive the grade of "Unacceptable." Submissions that exceed the qualities outlined for "Check" may receive the grade of "Check+". As per the course policies, note that a grade of "Check" is sufficient to receive an A in the class.
