---
layout: page
title: Home
nav_exclude: true
seo:
  type: Course
  name: CS 4973/7580, Advanced Software Engineering
---

# {{ site.tagline }}
{: .mb-2 }
CS 4973/7580, Spring 2023, Tues 11:45-1:25pm/Thurs 2:50-4:30pm, Richards Hall 325
{: .fs-6 .fw-300 }

{% if site.announcements %}
{{ site.announcements.last }}
[Announcements](announcements.md){: .btn .btn-outline .fs-3 }
{% endif %}

## Instructor
{% assign instructors = site.staffers | where: 'role', 'Instructor' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}

{% assign teaching_assistants = site.staffers | where: 'role', 'Teaching Assistant' %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% if num_teaching_assistants != 0 %}
## Teaching Assistants

{% for staffer in teaching_assistants %}
{{ staffer }}
{% endfor %}
{% endif %}

## Overview
Building, delivering and maintaining successful software products requires more than being good at programming. Software engineering encompasses the tools and processes that we use to design, construct and maintain programs over time. Software engineering has been said to consider the "multi person development of multi version programs." Development processes that work well for a single developer do not scale to large or even medium-sized teams. Similarly, development processes that work well for quickly delivering a one-off program to a client cause chaos when applied to a codebase that needs to be maintained and updated over months and years. 
This class will explore recent research in software engineering, focusing particularly on automated approaches that help developers create higher quality software, faster.

The primary objective for this course is for students to learn about cutting edge processes and techniques for engineering software. Topics will include: testing, agile processes, continuous integration, open source ecosystems, end-user programming, and security. We will study research papers that apply a variety of methods for studying software engineering, including studies of open source software and also observational studies and interviews of developers. The course delivery will be a mixture of lectures and discussions of research articles.  

## Pre-requisites
Students are expected to have experience engineering software beyond the scope of programming assignments in courses. Examples might include software written for research projects, for personal projects, or for a product. There is no requirement to be able to program in any particular language, but working knowledge of Java, C, TypeScript, Ruby, Python or R will be useful for the implementaiton project.

## Intended Audience
This course is intended for undergraduate and graduate students who would like to prepare for research in software engineering and other adjacent fields of computer science (for example: security and systems). This course is also designed to be highly applicable to students who are *not* interested in pursuing a career in research, but who would like to become more productive software engineers in industry. 

