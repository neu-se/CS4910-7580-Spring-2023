---
layout: page
title: Calendar
description: Listing of course modules and topics.
---

# Calendar

Generally, we will discuss one research paper each class meeting. Please be sure to read the assigned paper before class. Where possible, I've directly linked to PDFs. However, some papers link to the ACM or IEEE library - you can sign in to those services using your Northeastern login (select "Sign in with institutional credentials" and then select Northeastern).

 {% for module in site.modules %}
 {{ module }}
 {% endfor %}
