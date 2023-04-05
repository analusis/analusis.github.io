---
title: About me
subtitle: Learning data analytics
description: This page describes internet-safe information about me and the beginning of my journey into data analytics.
featured_image: /images/about.jpg
---

## Who

I'm a full-time paramedic with an interest in data analytics. It is my mission to learn how to collect, analyze, and share data to improve the world around me.

## Where

I am located in the Dallas-Fort Worth area of Texas.

## When

My journey started in September 2022 with the <a href="https://www.coursera.org/google-certificates/data-analytics-certificate" target="_blank">Coursera Google Data Analytics Course</a>.

I completed the course in April 2023 with the following case studies:

| Case Study               | Summary | Technology               |
|--------------------------|---------|--------------------------|
| <a href="{{ '/project/gda-casestudy1' | relative_url }}">Cyclistic</a> | Analyze rider data from the last 12 months to identify trends in usage between member and casual riders. | Excel, R Studio, Tableau |
| <a href="{{ '/project/gda-casestudy2' | relative_url }}">Wellness</a>  |  | |

{% assign currentDate = site.time | date: '%s' %}
{% assign startDate = '2022-09-19' | date: '%s' %}
{% assign secondsDiff = currentDate | minus: startDate %}
{% assign calcTime = secondsDiff | divided_by: 3600 | divided_by: 24 %}

This has only been the beginning. I am continuing to work on portfolio projects to demonstrate the knowledge and skills I've learned over the last {{ calcTime }} days.