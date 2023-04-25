---
title: 'Cyclistic - Rider Usage Trends'
subtitle: 'Coursera Google Data Analytics - Case Study 1'
date: 2023-04-02 07:00:00
description: Analyze rider data from the last 12 months to identify trends in usage between member and casual riders.
featured_image: '/images/projects/cgda/cs01/cover.jpg'
---
## Introduction

This is a fictional case study through the [Coursera Google Data Analytics Professional Certificate program](https://www.coursera.org/google-certificates/data-analytics-certificate).

As a junior data analyst working in the marketing analyst team at Cyclistic[^1], a question has been identified out of a list of three to guide the future marketing program.

>How do member and casual riders use Cyclistic bikes differently?

---

| Case Study Presentations             |
|--------------------------------------|
| [View Charts in Tableau](https://public.tableau.com/app/profile/analusis/viz/CGDA-CaseStudy1/TrendCombinedbyMonthYear) |
| [Download the PowerPoint Presentation]({{ site.url }}/downloads/2023-04-02-gda-cs1/CyclisticRiderTrends.pptx) |
| [Download the Presentation PDF]({{ site.url }}/downloads/2023-04-02-gda-cs1/CyclisticRiderTrends.pdf) |

---

## Data Analysis Phases

### Ask
#### Identify the business task

Analyze historical ride data to reveal trends in usage of the Cyclistic program between rider types.

#### Consider key stakeholders

Stakeholders include Lily Moreno and the executive team.

| Deliverable                          |
|--------------------------------------|
| Analyze rider data from the last 12 months to identify trends in usage of Cyclistic between member and casual riders. Insights into the data can reveal new or improved marketing opportunities to convert casual riders into annual-pass holders. |

### Prepare
#### Download data and store it appropriately.

The data is retrieved from Cyclistic's[^1] online repository. See disclaimer.[^2]

|---|---|
|Author|Divvy|
|Date of Publication|April 6th 2022 through March 7th 2023|
|Title|Historical Trip Data - 3/2022-2/2023|
|URL|[Divvy Data](https://divvybikes.com/system-data), [divvy-tripdata](https://divvy-tripdata.s3.amazonaws.com/index.html)|
|Date Accessed|March 27th 2023|

The retrieved data is stored on an encrypted drive for authorized users only.

#### Identify how it's organized.

The data is organized in wide format in a CSV file. Each month of data is contained within its own CSV file.

#### Sort and filter the data.

The data has been named and sorted, with each file representing a different month/year of data. The data is pre-sorted to contain only rows of individual trips. The data was filtered by the source to remove trips taken by staff as well as any trips lasting less than 60 seconds, and contains no PII.

#### Determine the credibility of the data.

The data has been supplied by Cyclistic and there is no supposition of bias. The data appears to be objective measurements and information obtained directly from recorded rider trips. The data is reasonably reliable and original as it is sourced from Cyclistic. The data appears to be comprehensive in that it provides enough information for the current business task. There may be limitations in analyzing trends that relate to a rider's Cyclistic service area and the inability to know if the same user has purchased multiple single passes due to pre-filtering of PII. The data is from 3/1/2022 through 2/28/2023.

| Deliverable                          |
|--------------------------------------|
| Data was obtained via direct download from the [Cyclistic website](https://divvy-tripdata.s3.amazonaws.com/index.html). |

### Process
#### Choose your tools.

I am using [Excel](https://www.microsoft.com/en-us/microsoft-365/excel) to take a quick look at the data and familiarize myself. Due to there being a few million records, I am using the [R programming language](https://www.r-project.org/) with [R Studio](https://posit.co/download/rstudio-desktop/) to check for errors as well as transform and clean the data.

#### Check the data for errors.

The data was evaluated using R Studio. The individual data files were loaded into data frames and then combined into a single data frame for further processing. The resulting data frame was inspected further and columns not being used for this analysis were removed. Columns were evaluated for inconsistent values (such as differences in member_casual) and bad datetime values, such as start times occuring after end times, were removed. The removed rows were separated from the data frame but saved separately for transparency and possible future correction.

#### Transform the data so you can work with it effectively.

Data transformation was performed by loading the data into an R dataframe for processing. Detection of data types and familiarization of the structure was performed. If inconsistencies were found, they were noted for immediate action and future analysis purposes.

#### Document the cleaning process.
The cleaning and transformation processes were documented in an R Markdown file for repeatability and transparency. The log is available in the Deliverable table below.

| Deliverable                          |
|--------------------------------------|
| {::nomarkdown}<iframe src="{{ site.url }}/downloads/2023-04-02-gda-cs1/cs1-process.html" width="100%" height="400" frameborder="0" allowfullscreen></iframe>{:/} |
| [View the R Markdown HTML output log]({{ site.url }}/downloads/2023-04-02-gda-cs1/cs1-process.html) |
| [Download the R Markdown file]({{ site.url }}/downloads/2023-04-02-gda-cs1/cs1-process.Rmd) |
| The original data is 1.12 GB in size and contains 5,829,084 records. |
| The cleaned data is 896 MB in size and contains 5,828,546 records. |
| [Download the removed data.]({{ site.url }}/downloads/2023-04-02-gda-cs1/removed_rides.csv) The removed data is 80.8 KB in size and contains 538 records. |



### Analyze
#### Aggregate your data so it's useful and accessible.
The started_at datetime field was split into individual items while maintaining the original data in the started_at column. Two additional new columns were created from existing data to aid in discovering trends, a weekday column based on the started_at date, and a ride_length column to calculate the duration of each ride.

#### Identify trends and relationships.
Univariate and bivariate analyses were performed to identify trends in the data. ggplot2 was utilized to create a quick look at possible trends in preparation for the Share phase.

| Deliverable                          |
|--------------------------------------|
| {::nomarkdown}<iframe src="{{ site.url }}/downloads/2023-04-02-gda-cs1/cs1-analyze.html" width="100%" height="400" frameborder="0" allowfullscreen></iframe>{:/} |
| [View the R Markdown HTML output log]({{ site.url }}/downloads/2023-04-02-gda-cs1/cs1-analyze.html) |
| [Download the R Markdown file]({{ site.url }}/downloads/2023-04-02-gda-cs1/cs1-analyze.Rmd) |
| The analyzed data is 1.05 GB in size and contains 5,828,546 records. |

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
| [Download the Presentation PDF]({{ site.url }}/downloads/2023-04-02-gda-cs1/CyclisticRiderTrends.pdf) |

### Act
#### Create your portfolio.
I created this website using GitHub Pages and Jekyll to document my case study progress. 

#### Practice presenting your case study.
Using the colleague test, I worked to refine my presentation and delivery. This allowed me to identify areas of confusion that could be clarified or data gaps that further analysis or data collection could uncover.

| Deliverable                          |
|--------------------------------------|
| [https://analusis.dev]({{ site.url }}) |


## Thank you!
Thank you for taking the time to review my case study from the Coursera Google Data Analytics course. This course has given me valuable knowledge and skills that I will continue to improve with future studies, as this is only the beginning of my journey into data analytics.


[^1]: This business task is fictional through the Coursera Google Data Analytics Certificate Course under the fictional company name Cyclistic. The task uses real-world data provided by [Divvy](https://divvybikes.com/), which is a program of the [Chicago Department of Transportation](https://www.chicago.gov/city/en/depts/cdot.html) in Illinois, United States.

[^2]:  The data belongs to and originated from Divvy. The data is provided according to the Divvy Data License Agreement. The data has been anonymized by Divvy and is public-access. In accordance with the Divvy Data License Agreement, no attempt will be made to deanonymize or correlate the data with PII or members of the program. This case study is not affiliated with, endorsed by, or sponsored by [Divvy](https://divvybikes.com/) or the [Chicago DOT](https://www.chicago.gov/city/en/depts/cdot.html).