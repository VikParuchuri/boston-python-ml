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


```
## Error: there is no package called 'ggplot2'
```


## What is edX?

* edX (edx.org) is an educational non-profit created by founding partners Harvard and MIT in May of 2012.  
* Several other universities have since joined the effort.
* Two major components:
  * edX platform learning management system (LMS)
  * edX studio content management system (CMS)
  * Together, enable authoring and delivery of courses at extremely large scale.
* Have hosted 30+ courses in subject areas from physics to justice, with a larger number upcoming.
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

## How it looks

* ![open response](assets/img/open_ended_response.png)

--- .class #id

## What is AI assessment, anyways?

* AI assessment is the edX term for a more generic process: machine-learning based text classification and scoring.
* We can start with any "training set" of text and associated scores.
  * ie Reddit posts and scores, essays and scores, books and the names of the authors who wrote them.
* The goal is to "train" a model that can map future input text to a score/category without being told what it is (prediction)

--- .class #id

## Training set example

Let's say that I wanted to give a survey after the talks today and ask the following question:

Why do you want to learn about machine learning?

The responses might look like this:


```
## 1 I like solving interesting problems.
## 2 What is machine learning?
## 3 I'm not sure.
```


Let's say that the survey also asks people to rate the talks on a scale of 0 to 2.

We would now have text and associated scores:

![plot of chunk unnamed-chunk-3](figure/unnamed-chunk-3.png) 


--- .class #id

## First steps

* Computers can't directly understand text like humans can.
  * Humans automatically break down sentences into units of meaning.
* In this case, we have to explicitly show the computer how to do this.
* Process is called tokenization.









