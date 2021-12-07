---
layout: page
title: ROCF
description: Analyze cognitive impairment
img: assets/img/rey.jpg
importance: 1
category: data analysis
---

Our system uses a smartpen to automatically digitize sketches from paper. A participant draws a Rey-Osterrieth Complex Figure as they would draw on any piece of paper. The test figures produce fuzzy sketches since several lines are segmented. Participants can also draw the shape in any order they wish, combining any shapes. The sketches will be turned into undirected graph, and 18 details are recognized with automated system.

## Intro

The Rey-Osterrieth Complex Figure Test (ROCF) - neuropsychological test that evaluates several cognitive functions including visuospatial abilities, memory, attention, planning, working memory and executive functions. The shape is specifically designed to be abstract so that participants cannot associate it with any common object or concept. A clinician then grades all three sketches on whether 18 separate sub-shapes exist and, if they do, how neatly they were drawn. Our creation of an automated ROCF that can grade itself on the existing grading scheme. 

## Graph Creation

Step by step construction pipeline: 

1. Corner detection by resampling to a uniform interspace with Pythagorean theorem
2. Corner-finding algorithm from Wolin to identify any “corner” from drawn strokes
3. Create undirected graph
4. Vertex Contraction vertices that fall below a predetermined distance threshold.

## Grading

To test our recognizer’s performance, the system graded `141 digitized Rey-Osterrieth tests` from participants, and we compare how closely our system’s grades correlate with those of an expert grader. For healthy participants taking this test, our expert graders attributed sloppiness as a lack of effort rather than genuine memory loss if the patient has no hand motor issues. By employing graph crawling, classical vertex search, and optimization algorithms we are able to identify key sub-shapes of geometric shapes.

###  Grading Tools

`F1-Score` of our recognition algorithm for each detail, and the comparison between our system’s total grade and the expert graders’ total grade. Spearman's Rank correlation coefficient is a technique which can be used to summarise the strength and direction (negative or positive) of a relationship between two variables.


## Paper

The project repository is confidential. However, if you are interested in learning more, I posted the unpublished manuscript under my [research work](/research/).
