---
layout: calendar
title: Calendar
nav_order: 2
instructor: Prof Bell
location: Richards Hall 325
dates: Tues 11:45am-1:25pm, Thurs 2:50pm-4:30pm
description: Listing of course modules and topics.
weeks:
    '1':
        topic: Software Process
        Tue:
            date: 2023/01/10
            name: SW Process and Course Overview. 
            file: 1-overview
        Thu:
            date: 2023/01/12
            name: Process Discussion
            page: /lecture-notes/2-sdi
            required:
                - "[Software Aspects of Strategic Defense Systems](https://doi.org/10.1145/214956.214961). David Parnas. CACM 1985"
    '2':
        topic: Modularity and Design
        Tue:
            date: 2023/01/17
            name: "Overview: Modularity, Design and Patterns"
            # readings: [GabrielPatterns]
            page: /lecture-notes/3-design
            file: 3-design
            required:
                - "[Patterns of Software: Tales from the Software Community](https://www.dreamsongs.com/Files/PatternsOfSoftware.pdf). Richard Gabriel, 1996. Read 'Reuse Versus Compression' (p3-7) and 'The Quality Without a Name' (p33-43)"
        Thu:
            date: 2023/01/19
            name: "Discussion: Modularity and Design"
            page: /lecture-notes/4-aop-rp
            required:
                - "[Aspect-Oriented Programming](https://link.springer.com/chapter/10.1007/BFb0053381). Kiczales et al. ECOOP 1997"
                - "[An empirical study on program comprehension with reactive programming](https://dl.acm.org/doi/abs/10.1145/2635868.2635895). Salvaneschi et al. FSE 2014"
    '3':
        topic: 'Open Source'
        Tue:
            date: 2023/01/24
            name: 'Overview: Open Source History and Models'
            file: 5-open-source
        Thu:
            date: 2023/01/26
            name: 'Discussion: Open Source'
            page: /lecture-notes/6-oss
            required:
                - "[How Has Forking Changed in the Last 20 Years? A Study of Hard Forks on GitHub](https://dl.acm.org/doi/10.1145/3377811.3380412). Zhou, Vasilescu and Kästner. ICSE 2020"
                - "[How to Not Get Rich: An Empirical Study of Donations in Open Source](https://doi.org/10.1145/3377811.3380410). Overney et al. ICSE 2020"
    '4':
        topic: Mining Software Repositories
        Tue:
            date: 2023/01/31
            name: 'Overview: MSR, metrics'
            file: 7-msr
        Thu:
            date: 2023/02/02
            name: 'Discussion: Mining Software Repositories'
            page: /lecture-notes/8-msr
            required:
                - "[The Promises and Perils of Mining GitHub](https://doi.org/10.1145/2597073.2597074). Kalliamvakou et al. MSR 2014"
                - "[A Large-Scale Comparison of Python Code in Jupyter Notebooks and Scripts](https://doi.org/10.1145/3524842.3528447). Grotov et al. MSR 2022"
    '5':
        topic: 'Testing: Overview and Oracles'
        Tue:
            date: 2023/02/07
            name: 'Overview: Tests and Oracles'
            file: 9-tests-oracles
            deliverable:
                name: 'Reflection Paper Proposal'
                page: '/assessments/paper-proposal/'

        Thu:
            date: 2023/02/09
            name: 'Discussion: Test Oracles'
            page: '/lecture-notes/10-mutation-daikon'
            required:
                - "[Are Mutants a Valid Substitute for Real Faults in Software Testing?](https://doi.org/10.1145/2635868.2635929). Just et al. FSE 2014"
                - "[Dynamically Discovering Likely Program Invariants to Support Program Evolution](https://doi.org/10.1145/302405.302467). Ernst, Griswold and Notkin. ICSE 1999"
    '6':
        topic: 'Testing: Inputs'
        Tue:
            date: 2023/02/14
            name: 'Overview: Input Generation Techniques'
            file: 11-tests-inputs
            # readings: [Miller90Empirical]
            required:
                - "[An Empirical Study of the Reliability of UNIX Utilities](https://doi.org/10.1145/96267.96279).  Miller, Fredriksen and So. CACM 1990"
                - "[How SQLite is Tested](https://www.sqlite.org/testing.html). If you are interested in how SQLite is made, optionally check out: SQLite [amalgamation](https://www.sqlite.org/amalgamation.html), [license](https://github.com/sqlite/sqlite/blob/master/LICENSE.md)"
        Thu:
            date: 2023/02/16
            name: Project Proposal Brainstorming
    '7':
        topic: 'Testing: Inputs'
        Tue:
            date: 2023/02/21
            name: 'Discussion: Fuzzing'
            page: '/lecture-notes/12-glfuzz'
            required:
                - "[Automated Testing of Graphics Shader Compilers](https://doi.org/10.1145/3133917). Donaldson et al. OOPSLA 2017"
            optional: [Bohme16CoverageBased,Pacheco07Randoop]
        Thu:
            date: 2023/02/23
            name: 'Project Proposal Discussions'
            deliverable:
                name: 'Preliminary Project Proposal'
                page: '/assessments/project-proposal'
    '8':
        topic: 'CI and Test Suite Maintenance'
        Tue:
            name: 'Overview: CI and cloud resources'
            date: 2023/02/28
            file: 13-ci
        Thu:
            date: 2023/03/02
            name: 'Discussion: CI, more process'
            deliverable:
                name: 'Final Project Proposal'
                page: '/assessments/revised-project-proposal'
            page: '/lecture-notes/14-ci'
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
            note: '[Paper presentation order](https://northeastern.instructure.com/courses/136828/pages/paper-presentation-order)'
        Thu:
            date: 2023/03/16
            name: Students present their reflection papers
            note: '[Paper presentation order](https://northeastern.instructure.com/courses/136828/pages/paper-presentation-order)'
    '11':
        topic: Devops
        Tue:
            date: 2023/03/21
            name: 'Overview: Deployment and Operations'
            file: 15-cd
            required:
                - "[The $440 Million Software Error at Knight Capital](https://www.henricodolfing.com/2019/06/project-failure-case-study-knight-capital.html)"
                - "[Do The Simple Thing First: The Engineering Behind Instagram](https://www.fastcompany.com/3047642/do-the-simple-thing-first-the-engineering-behind-instagram)"
        Thu:
            date: 2023/03/23
            name: 'Discussion: DevOps'
            page: 17-devops
            # readings: [Kaldor17Canopy]
            required:
                - "[Canopy: An End-to-End Performance Tracing And Analysis System](https://doi.org/10.1145/3132747.3132749). Kaldor et al. OSDI 2017"
                - "[An Evolutionary Study of Configuration Design and Implementation in Cloud Systems](https://dl.acm.org/doi/10.1109/ICSE43902.2021.00029). Zhang et al. ICSE 2021"
    '12':
        topic: Expertise and Knowledge Sharing
        Tue:
            name: 'Overview: Collaboration in SE'
            date: 2023/03/28
            file: 18-knowledge
            deliverable:
                name: Project Status Update
                page: /assessments/project-status-update/
        Thu:
            date: 2023/03/30
            name: "Discussion: Being Great and Helping Others"
            required:
                - "[What Makes a Great Software Engineer?](https://dl.acm.org/doi/10.5555/2818754.2818839) Li, Ko and Zhu. ICSE 2015"
                - "[An Exploratory Study of Sharing Strategic Programming Knowledge](https://doi.org/10.1145/3491102.3502070). Arab et al. CHI 2022"
            # readings: [Li15WhatMakes,Arab22Exploratory]

    '13':
        topic: More Human Factors
        Tue:
            date: 2023/04/04
            name: "Discussion: SE and Data Science"
            # readings: [Chattopadhyay20Notebooks,Wang21Assessing]
            required:
                - "[What’s Wrong with Computational Notebooks? Pain Points, Needs, and Design Opportunities](https://doi.org/10.1145/3313831.3376729). Chattopadhyay et al. CHI 2020"
                - "[Managing Messes in Computational Notebooks](https://dl.acm.org/doi/10.1145/3290605.3300500). Head et al. CHI 2019"

        Thu:
            date: 2023/04/06
            name: "Discussion: Barriers to Diversity in SE"
            required:
                - "[Open source barriers to entry, revisited: A sociotechnical perspective](https://dl.acm.org/doi/10.1145/3180155.3180241). Mendez et al. ICSE 2018"
                - "[\"STILL AROUND\": Experiences and Survival Strategies of Veteran Women Software Developers](https://empirical-software.engineering/assets/pdf/icse23-still-around.pdf). Breukelen et al. ICSE 2023"
    '14':
        topic: Security
        Tue:
            date: 2023/04/11
            name: 'Overview: Security and SE, Malicious Components'
            # readings: [Sejfia22Practical]
            required:
                - "[Practical Automated Detection of Malicious Npm Packages](https://doi.org/10.1145/3510003.3510104). Sejfia and Schäfer. ICSE 2022"
        Thu:
            date: 2023/04/13
            name: "Discussion: Supply Chain Security"
            # readings: [Zahan22WeakLinks,Rahman22WhySecret]
            required:
                - "[What Are Weak Links in the Npm Supply Chain?](https://doi.org/10.1145/3510457.3513044). Zahan et al. ICSE 2022"
                - "[Why secret detection tools are not enough: It’s not just about false positives - An industrial case study](https://link.springer.com/article/10.1007/s10664-021-10109-y). Rahman et al. Empirical Software Engineering, 2022"
    '15':
        topic: Project Presentations
        Tue:
            date: 2023/04/18
            name: "Students present their projects"
            deliverable:
                name: Project Report
                page: /assessments/project/
        Thu:
            date: 2023/04/20
            name: "Students present their projects"

---

Class meetings marked as "overview" will be lecture-focused, providing background material to help contextualize the topic. "Discussion" meetings will be highly interactive discussions centered on the required readings.


Please be sure to read the assigned paper before class. 
Most papers link into the ACM or IEEE library - you can sign in to those services using your Northeastern login (select "Sign in with institutional credentials" and then select Northeastern). Note that for the ACM library, you can create an ACM account and then link it to your Northeastern ID ("My Profile" -> "Institutional Affiliations") so that you can stay logged in and not need to go through Duo every time that you would like to read a paper.
