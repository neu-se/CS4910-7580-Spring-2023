---
layout: calendar
title: Calendar
instructor: Prof Bell
location: Richards Hall 325
dates: Tues 11:45am-1:25pm, Thurs 2:50pm-4:30pm
description: Listing of course modules and topics.
weeks:
    '1':
        topic: Software Process
        Tue:
            date: 2023/01/10
            name: SW Process and Course Overview
        Thu:
            date: 2023/01/12
            name: Process Discussion
            required:
                - "[Software Aspects of Strategic Defense Systems](https://doi.org/10.1145/214956.214961). David Parnas. CACM 1985"
    '2':
        topic: Modularity and Design
        Tue:
            date: 2023/01/17
            name: "Overview: Modularity, Design and Patterns"
            # readings: [GabrielPatterns]
            required:
                - "[Patterns of Software: Tales from the Software Community](https://www.dreamsongs.com/Files/PatternsOfSoftware.pdf). Richard Gabriel, 1996. Read 'Reuse Versus Compression' (p3-7) and 'The Quality Without a Name' (p33-43)"
        Thu:
            date: 2023/01/19
            name: "Discussion: Modularity and Design"
            required:
                - "TBD"
    '3':
        topic: Mining Software Repositories
        Tue:
            date: 2023/01/24
            name: 'Overview: MSR, metrics'
        Thu:
            date: 2023/01/26
            name: 'Discussion: Mining Software Repositories'
            required:
                - "[The Promises and Perils of Mining GitHub](https://doi.org/10.1145/2597073.2597074). Kalliamvakou et al. MSR 2014"
                - "[A Large-Scale Comparison of Python Code in Jupyter Notebooks and Scripts](https://doi.org/10.1145/3524842.3528447). Grotov et al. MSR 2022"
    '4':
        topic: 'Open Source'
        Tue:
            date: 2023/01/31
            name: 'Overview: Open Source History and Models'
        Thu:
            date: 2023/02/02
            name: 'Discussion: Open Source'
            required:
                - "[How Has Forking Changed in the Last 20 Years? A Study of Hard Forks on GitHub](https://doi.org/10.1145/3377812.3390911). Zhou, Vasilescu and Kästner. ICSE 2020"
                - "[How to Not Get Rich: An Empirical Study of Donations in Open Source](https://doi.org/10.1145/3377811.3380410). Overney et al. ICSE 2020"
    '5':
        topic: 'Testing: Overview and Oracles'
        Tue:
            date: 2023/02/07
            name: 'Overview: Tests and Oracles'
        Thu:
            date: 2023/02/09
            name: 'Discussion: Test Oracles'
            required:
                - "[Are Mutants a Valid Substitute for Real Faults in Software Testing?](https://doi.org/10.1145/2635868.2635929). Just et al. FSE 2014"
                - "[Dynamically Discovering Likely Program Invariants to Support Program Evolution](https://doi.org/10.1145/302405.302467). Ernst, Griswold and Notkin. ICSE 1999"
    '6':
        topic: 'Testing: Inputs'
        Tue:
            date: 2023/02/14
            name: 'Overview: Input Generation Techniques'
            # readings: [Miller90Empirical]
            required:
                - "[An Empirical Study of the Reliability of UNIX Utilities](https://doi.org/10.1145/96267.96279).  Miller, Fredriksen and So. CACM 1990"
        Thu:
            date: 2023/02/16
            name: Project Proposal Brainstorming
    '7':
        topic: 'Testing: Inputs'
        Tue:
            date: 2023/02/21
            name: 'Discussion: Fuzzing'
            required:
                - "[Automated Testing of Graphics Shader Compilers](https://doi.org/10.1145/3133917). Donaldson et al. OOPSLA 2017"
            optional: [Bohme16CoverageBased,Pacheco07Randoop]
        Thu:
            date: 2023/02/23
            name: 'Project Proposal Presentations'
            deliverable:
                name: 'Preliminary Project Proposal'
    '8':
        topic: 'CI and Test Suite Maintenance'
        Tue:
            name: 'Overview: CI and cloud resources'
            date: 2023/02/28
            deliverable:
                name: 'Final Project Proposal'
        Thu:
            date: 2023/03/02
            name: 'Discussion: CI, more process'
            # readings: [Hilton17Tradeoffs,Memon17Taming]
            required:
                - "[Trade-Offs in Continuous Integration: Assurance, Security, and Flexibility](https://doi.org/10.1145/3106237.3106270). Hilton et al. FSE 2017"
                - "[Taming Google-Scale Continuous Testing](https://doi.org/10.1109/ICSE-SEIP.2017.16). Memon et al. ICSE 2017"
    '9':
        topic: Spring Break
    '10':
        topic: Paper Presentations
        Tue:
            date: 2023/03/14
            name: Students present their reflection papers
            deliverable:
                name: 'Reflection Paper'
                page: '/assessments/paper/'
        Thu:
            date: 2023/03/16
            name: Students present their reflection papers
    '11':
        topic: Devops
        Tue:
            date: 2023/03/21
            name: 'Overview: Deployment and Operations'
        Thu:
            date: 2023/03/23
            name: 'Discussion: DevOps'
            # readings: [Kaldor17Canopy]
            required:
                - "[Canopy: An End-to-End Performance Tracing And Analysis System](https://doi.org/10.1145/3132747.3132749). Kaldor et al. OSDI 2017"
                - TBD
    '12':
        topic: Expertise and Knowledge Sharing
        Tue:
            name: 'Overview: Collaboration in SE'
            date: 2023/03/28
        Thu:
            date: 2023/03/30
            name: "Discussion: Being Great and Helping Others"
            required:
                - "[What Makes a Great Software Engineer?](https://dl.acm.org/doi/10.5555/2818754.2818839) Li, Ko and Zhu. ICSE 2015"
                - "[An Exploratory Study of Sharing Strategic Programming Knowledge](https://doi.org/10.1145/3491102.3502070). Arab et al. CHI 2022"
            # readings: [Li15WhatMakes,Arab22Exploratory]

    '13':
        topic: Security
        Tue:
            date: 2023/04/04
            name: 'Overview: Security and SE, Malicious Components'
            # readings: [Sejfia22Practical]
            required:
                - "[Practical Automated Detection of Malicious Npm Packages](https://doi.org/10.1145/3510003.3510104). Sejfia and Schäfer. ICSE 2022"
        Thu:
            date: 2023/04/06
            name: "Discussion: Supply Chain Security"
            # readings: [Zahan22WeakLinks,Rahman22WhySecret]
            required:
                - "[What Are Weak Links in the Npm Supply Chain?](https://doi.org/10.1145/3510457.3513044). Zahan et al. ICSE 2022"
                - "[Why secret detection tools are not enough: It’s not just about false positives - An industrial case study](https://link.springer.com/article/10.1007/s10664-021-10109-y). Rahman et al. Empirical Software Engineering, 2022"
    '14':
        topic: SE in Domains
        Tue:
            date: 2023/04/11
            name: "Discussion: SE and Data Science"
            # readings: [Chattopadhyay20Notebooks,Wang21Assessing]
            required:
                - "[Assessing and Restoring Reproducibility of Jupyter Notebooks](https://doi.org/10.1145/3324884.3416585). Wang et al. ASE 2021"
                - "[What’s Wrong with Computational Notebooks? Pain Points, Needs, and Design Opportunities](https://doi.org/10.1145/3313831.3376729). Chattopadhyay et al. CHI 2020"

        Thu:
            date: 2023/04/13
            name: "Discussion: SE and Robotics"
            # readings: [Hermans2015Detecting]
            required:
                - "TBD"
    '15':
        topic: Project Presentations
        Tue:
            date: 2023/04/18
            name: "Students present their projects"
        Thu:
            date: 2023/04/20
            name: "Students present their projects"

---

Class meetings marked as "overview" will be lecture-focused, providing background material to help contextualize the topic. "Discussion" meetings will be highly interactive discussions centered on the required readings.


Please be sure to read the assigned paper before class. 
Most papers link into the ACM or IEEE library - you can sign in to those services using your Northeastern login (select "Sign in with institutional credentials" and then select Northeastern). Note that for the ACM library, you can create an ACM account and then link it to your Northeastern ID ("My Profile" -> "Institutional Affiliations") so that you can stay logged in and not need to go through Duo every time that you would like to read a paper.
