---
title: 'Bellabeat - Consumer Usage'
subtitle: 'Coursera Google Data Analytics - Case Study 2'
date: 2023-04-10 10:00:00
description: Analyze consumer usage data to identify opportunities for business growth.
featured_image: '/images/projects/cgda/cs02/cover.jpg'
---
## Introduction

This is a fictional case study through the [Coursera Google Data Analytics Professional Certificate program](https://www.coursera.org/google-certificates/data-analytics-certificate).

As a junior data analyst working in the marketing analyst team at Bellabeat[^1], you have been asked to analyze smart device data to gain insights that will help guide marketing strategy for the company.

>Identify trends in non-Bellabeat branded smart device usage to gain marketing strategy insight.

---

## Data Analysis Phases

### Ask
#### Identify the business task

Analyze data collected from a non-Bellabeat branded smart device to develop insights and identify trends. Develop high-level recommendations based on the analysis in order to help develop new marketing strategies.

#### Consider key stakeholders

Stakeholders include Urška Sršen and the marketing team.

| Deliverable                          |
|--------------------------------------|
| Identify trends in non-Bellabeat branded smart device usage to gain marketing strategy insight. This in turn will be used to develop new marketing strategies. |

### Prepare
#### Download data and store it appropriately.

The data is retrieved from a Kaggle dataset. See disclaimer.[^2]

|---|---|
|Author|MÖBIUS|
|Date of Publication|December 16th 2020|
|Title|FitBit Fitness Tracker Data|
|URL|[Kaggle Dataset](https://www.kaggle.com/datasets/arashnic/fitbit)|
|Date Accessed|April 10th 2023|

The retrieved data is stored on an encrypted drive for authorized users only.

#### Identify how it's organized.

The data is organized in wide format in multiple CSV files. There are 18 files, each with different fitness measurements.

#### Determine the credibility of the data.

The data was supplied by Kaggle user [Möbius](https://www.kaggle.com/arashnic) but appears to have originated from a survey conducted via Amazon Mechanical Turk and originally available through [Zenodo](https://zenodo.org/record/53894).

**We will determine the credibility of the data using the ROCCC method:**
##### Reliable
The data is incomplete as it does not contain consistent data among all respondents. Based on the information provided by the source, there is no documentation on the accuracy of data collection. Selection bias may be at play as the survey source (Amazon Mechanical Turk) incentivizes participants with [financial reward](https://www.mturk.com/worker). Finally, the sample size is small and may not properly represent the targeted demographic. There is no documentation on the participants or verification that the participants represent the targeted demographic.

##### Original
The data is not original. It is supplied by a third-party.

##### Comprehensive
Some of the data provided is missing responses by participants. Additionally, the data only contains approximately one month of data. Trend insights could be affected in that there is not enough data over time to analyze or develop a clear picture of usage.

##### Current
The data is not current and has not been updated since 2016. Additionally, the data provided by the case study scenario only contains data from 4/12/2016-5/12/2016.

##### Cited
The data is cited from an original source on Zenodo. Zenodo cites the original authors/collecters of the data, but no further information is available.

#### Sort and filter the data.

The original collection source of the data, Zenodo, was investigated further and was found to have collected data using [Fitabase](https://www.fitabase.com/). Fitabase has a knowledge base that provides a link to their [data dictionary](https://www.fitabase.com/resources/knowledge-base/exporting-data/data-dictionaries/) for Fitbit data. From here, we are able to determine the expected data types in each field as well as the meaning behind the values.

The data files were renamed to sort the data files while still describing the data contained. The data record rows are identified by a user id as well as the date or datetime.

* dailyActivity_merged.csv -> activity_daily.csv
* dailyCalories_merged.csv -> calories_daily.csv
* dailyIntensities_merged.csv -> intensity_daily.csv
* dailySteps_merged.csv -> steps_daily.csv
* heartrate_seconds_merged.csv -> heartrate_by_seconds.csv
* hourlyCalories_merged.csv -> calories_hourly.csv
* hourlyIntensities_merged.csv -> intensity_hourly.csv
* hourlySteps_merged.csv -> steps_hourly.csv
* minuteCaloriesNarrow_merged.csv -> calories_minutes_narrow.csv
* minuteCaloriesWide_merged.csv -> calories_minutes_wide.csv
* minuteIntensitiesNarrow_merged.csv -> intensity_minutes_narrow.csv
* minuteIntensitiesWide_merged.csv -> intensity_minutes_wide.csv
* minuteMETsNarrow_merged.csv -> met_minutes_narrow.csv
* minuteSleep_merged.csv -> sleep_minutes.csv
* minuteStepsNarrow_merged.csv -> steps_minutes_narrow.csv
* minuteStepsWide_merged.csv -> steps_minutes_wide.csv
* sleepDay_merged.csv -> sleep_daily.csv
* weightLogInfo_merged.csv -> weight_log.csv

| Deliverable                          |
|--------------------------------------|
| Data was obtained via direct download from a [Kaggle dataset](https://www.kaggle.com/datasets/arashnic/fitbit) |

### Process
#### Choose your tools.

I am using the [R programming language](https://www.r-project.org/) with [R Studio](https://posit.co/download/rstudio-desktop/) to check for errors and data limitations as well as to transform and clean the data.

#### Check the data for errors and transform the data

The data was evaluated using R Studio. The individual data files were loaded into data frames for further processing. Columns were evaluated for inconsistent or invalid values. Any removed rows of bad data were separated from the data frame. Data that was considered too incomplete for analysis were documented.

#### Document the cleaning process.
The cleaning and transformation processes were documented in an R Markdown file for repeatability and transparency. The log is available in the Deliverable table below.

| Deliverable                          |
|--------------------------------------|
| {::nomarkdown}<iframe src="{{ site.url }}/downloads/2023-04-10-gda-cs2/cs2-process.html" width="100%" height="400" frameborder="0" allowfullscreen></iframe>{:/} |
| [View the R Markdown HTML output log]({{ site.url }}/downloads/2023-04-10-gda-cs2/cs2-process.html) |
| [Download the R Markdown file]({{ site.url }}/downloads/2023-04-10-gda-cs2/cs2-process.Rmd) |



### Analyze
#### Aggregate your data so it's useful and accessible.
While aggregating data can refer to the combining of separate structures into a structure of similar form, we also refer to aggregation as a means of summarzing the whole of data. The separate structures were already combined into new dataframes of similar structures in the process phase, but we will perform summary analysis on them to take a closer look at the available data. We will investigate the kind of data we have to work with in preparation for analyzing trends and relationships to accomplish the business task.

#### Identify trends and relationships.
Univariate and bivariate analyses were performed to identify trends in the data. ggplot2 was utilized to create a quick look at possible trends in preparation for the Share phase.

| Deliverable                          |
|--------------------------------------|
| {::nomarkdown}<iframe src="{{ site.url }}/downloads/2023-04-10-gda-cs2/cs2-analyze.html" width="100%" height="400" frameborder="0" allowfullscreen></iframe>{:/} |
| [View the R Markdown HTML output log]({{ site.url }}/downloads/2023-04-10-gda-cs2/cs2-analyze.html) |
| [Download the R Markdown file]({{ site.url }}/downloads/2023-04-10-gda-cs2/cs2-analyze.Rmd) |

### Share

#### Determine the best way to share your findings.
I am using Tableau to create charts based on historical data. The charts are separated into individual worksheets for viewing on Tableau.
<div class="gallery" data-columns="4">
	<img src="/downloads/2023-04-02-gda-cs1/gallery/01.png">
	<img src="/downloads/2023-04-02-gda-cs1/gallery/02.png">
    <img src="/downloads/2023-04-02-gda-cs1/gallery/03.png">
    <img src="/downloads/2023-04-02-gda-cs1/gallery/04.png">
    <img src="/downloads/2023-04-02-gda-cs1/gallery/05.png">
    <img src="/downloads/2023-04-02-gda-cs1/gallery/06.png">
    <img src="/downloads/2023-04-02-gda-cs1/gallery/07.png">
</div>

#### Present your findings.
PowerPoint was utilized to create a presentation. I sought to use contrasting colors with clear text and clean design. A shorter presentation style was created with the intention of summarized text and easy-to-read graphics to keep viewer engagement higher.

| Deliverable                          |
|--------------------------------------|
| [View Charts in Tableau](https://public.tableau.com/app/profile/analusis/viz/CGDA-CaseStudy1/TrendCombinedbyMonthYear) |
| [Download the PowerPoint Presentation]({{ site.url }}/downloads/2023-04-02-gda-cs1/CyclisticRiderTrends.pptx) |

### Act
#### Create your portfolio.
I created this website using GitHub Pages and Jekyll to document my case study progress. 

#### Practice presenting your case study.
Using the colleague test, I worked to refine my presentation and delivery. This allowed me to identify areas of confusion that could be clarified or data gaps that further analysis or data collection could uncover.

| Deliverable                          |
|--------------------------------------|
| [https://analusis.dev]({{ site.url }}) |


## Thank you!
Thank you for taking the time to review my case study from the Coursera Google Data Analytics course. This course has given me valuable knowledge and skills that I will continue to improve with future studies, as this is only the beginning of my journey into data analytics, 


[^1]: This business task is fictional through the Coursera Google Data Analytics Certificate Course under the company name Bellabeat. The task uses [real-world data](https://www.kaggle.com/datasets/arashnic/fitbit) provided by [Möbius](https://www.kaggle.com/arashnic).

[^2]:  The data for this case study has been dedicated to the public domain under the CC0: Public Domain license. This case study is neither affiliated with nor endorsed by the creator, [Möbius](https://www.kaggle.com/arashnic).
