---
title: About me
subtitle: Learning data analytics
description: Personal is the perfect theme for developers, designers and other creatives.
featured_image: /images/demo/about.jpg
---

## Who

I'm a full-time paramedic with an interest in data analytics. It is my mission to learn how to collect, analyze, and share data to improve the world around me.

## Where

I am located in the Dallas-Fort Worth area of Texas.

## When

My journey started in September 2022 with the <a href="https://www.coursera.org/google-certificates/data-analytics-certificate" target="_blank">Coursera Google Data Analytics Course</a>.

I completed the course in April 2023 with the following case studies:
* <a href="">Cyclistic</a>
* <a href="">Wellness</a>

{% assign currentDate = site.time | date: '%s' %}
{% assign startDate = '2022-09-19' | date: '%s' %}
{% assign secondsDiff = currentDate | minus: startDate %}
{% assign calcTime = secondsDiff | divided_by: 3600 | divided_by: 24 %}

This has only been the beginning. I am continuing to work on portfolio projects to demonstrate the knowledge and skills I've learned over the last {{ calcTime }} days.