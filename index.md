---
title       : Text scoring and classification using edX EASE and Discern
subtitle    : 
author      : Vik Paruchuri
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
---

## What is edX?

* edX (edx.org) is an educational non-profit created by founding partners Harvard and MIT in May of 2012.  
* Several other universities have since joined the effort.
* Two major components:
  * edX platform learning management system (LMS)
  * edX Studio content management system (CMS)
  * Together, enable authoring and delivery of courses at extremely large scale.
* Have hosted 30 courses in subject areas from physics to justice, with an equal number upcoming.
* Recenly passed the 1 million student mark.

--- .class #id 

## Assessments on the edX platform

* When edX launched, assessments were restricted to "closed-choice" response.
* ![multiple choice](assets/img/multiple_choice_problem.png)
* ![string response](assets/img/string_response.png)

--- .class #id

## How do we support humanities courses?

* Difficult to support humanities courses without allowing students to enter free-text responses.
  * Richer assessments allow for varied instructional and learning styles.
* Short answer responses also useful for STEM courses offered by edX.

--- .class #id

## Potential strategies

* Peer assessment (students grade each other)
* Self assessment (students grade themselves)
* Instructor assessment (instructor grades everyone)
* AI Assessment (computer algorithm is trained and then grades students)
* Scoring students based on participation and quality of discussions.

--- .class #id

## Overall Implementation

* Through edx-ora (https://github.com/edx/edx-ora), implemented a combination of peer assessment, self assessment, instructor assessment, and AI assessment.
* edx-ora is currently being used to grade student free-text responses on the edX platform.
* Currently in alpha, and development is ongoing.
* Although the focus of this talk is AI assessment, highly encourage looking at edX-ora if you are interested.

--- .class #id

## AI Assessment

* 






