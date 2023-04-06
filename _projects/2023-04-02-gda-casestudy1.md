---
title: 'Cyclistic - Rider Usage Trends'
subtitle: 'Coursera Google Data Analytics - Case Study 1'
date: 2018-06-30 00:00:00
description: Analyze rider data from the last 12 months to identify trends in usage between member and casual riders.
featured_image: '/images/projects/cgda/cs01/cover.png'
---
## Introduction

This is a fictional case study through the [Coursera Google Data Analytics Professional Certificate program](https://www.coursera.org/google-certificates/data-analytics-certificate).

As a junior data analyst working in the marketing analyst team at Cyclistic[^1], a question has been identified out of a list of three to guide the future marketing program.

>How do member and casual riders use Cyclistic bikes differently?

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

I am using [Excel](https://www.microsoft.com/en-us/microsoft-365/excel) to take a quick look at the data and familiarize myself. Due to there being a few million records, I am using the [R programming language](https://www.r-project.org/) with [R Studio](https://posit.co/download/rstudio-desktop/) to check for errors and clean the data.

#### Check the data for errors.

The data was evaluated using R Studio. The individual data files were loaded into data frames and then combined into a single data frame for further processing. The resulting data frame was inspected further and columns not being used for this analysis were removed. Columns were evaluated for inconsistent values (such as differences in member_casual) and bad datetime values, such as start times occuring after end times, were removed. The removed rows were separated from the data frame but saved separately for transparency and possible future correction.

#### Transform the data so you can work with it effectively.
#### Document the cleaning process.

| Deliverable                          |
|--------------------------------------|
| {::nomarkdown}<iframe src="{{ site.url }}/downloads/2023-04-02-gda-cs1/cs1-process.html" width="100%" height="400" frameborder="0" allowfullscreen></iframe>{:/} |
| [Download the R Markdown HTML output log]({{ site.url }}/downloads/2023-04-02-gda-cs1/cs1-process.html) |
| [Download the R Markdown file]({{ site.url }}/downloads/2023-04-02-gda-cs1/cs1-process.Rmd)



### Analyze
#### Aggregate your data so it's useful and accessible.
#### Organize and format your data.
#### Perform calculations.
#### Identify trends and relationships.

| Deliverable                          |
|--------------------------------------|
|                                      |

### Share
#### Determine the best way to share your findings.
#### Create effective data visualizations.
#### Present your findings.
#### Ensure your work is accessible.

| Deliverable                          |
|--------------------------------------|
|                                      |

### Act
#### Create your portfolio.
#### Add your case study.
#### Practice presenting your case study.

| Deliverable                          |
|--------------------------------------|
|                                      |

=======================================================

**Obviously,** we’ve styled up *all the basic* text formatting options [available in markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

You can create lists:

* Simple bulleted lists
* Like this one
* Are cool

And:

1. Numbered lists
2. Like this other one
3. Are great too

You can also add blockquotes, which are shown at a larger width to help break up the layout and draw attention to key parts of your content:

> “Simple can be harder than complex: You have to work hard to get your thinking clean to make it simple. But it’s worth it in the end because once you get there, you can move mountains.”

The theme also supports markdown tables:

| Item                 | Author        | Supports tables? | Price |
|----------------------|---------------|------------------|-------|
| Duet Jekyll Theme    | Jekyll Themes | Yes              | $49   |
| Index Jekyll Theme   | Jekyll Themes | Yes              | $49   |
| Journal Jekyll Theme | Jekyll Themes | Yes              | $49   |


[^1]: This business task is fictional through the Coursera Google Data Analytics Certificate Course under the fictional company name Cyclistic. The task uses real-world data provided by [Divvy](https://divvybikes.com/), which is a program of the [Chicago Department of Transportation](https://www.chicago.gov/city/en/depts/cdot.html) in Illinois, United States.

[^2]:  The data belongs to and originated from Divvy. The data is provided according to the Divvy Data License Agreement. The data has been anonymized by Divvy and is public-access. In accordance with the Divvy Data License Agreement, no attempt will be made to deanonymize or correlate the data with PII or members of the program. This case study is not affiliated with, endorsed by, or sponsored by [Divvy](https://divvybikes.com/) or the [Chicago DOT](https://www.chicago.gov/city/en/depts/cdot.html).

You can throw in some horizontal rules too:

---

### Image galleries

Here's a really neat custom feature we added – galleries:

<div class="gallery" data-columns="3">
	<img src="/images/demo/demo-portrait.jpg">
	<img src="/images/demo/demo-landscape.jpg">
	<img src="/images/demo/demo-square.jpg">
	<img src="/images/demo/demo-landscape-2.jpg">
</div>

Inspired by the Galleries feature from WordPress, we've made it easy to create grid layouts for your images. Just use a bit of simple HTML in your post to create a masonry grid image layout:

```html
<div class="gallery" data-columns="3">
    <img src="/images/demo/demo-portrait.jpg">
    <img src="/images/demo/demo-landscape.jpg">
    <img src="/images/demo/demo-square.jpg">
    <img src="/images/demo/demo-landscape-2.jpg">
</div>
```

*See what we did there? Code and syntax highlighting is built-in too!*

Change the number inside the 'columns' setting to create different types of gallery for all kinds of purposes. You can even click on each image to seamlessly enlarge it on the page.

---

### Image carousels

Here's another gallery with only one column, which creates a carousel slide-show instead.

A nice little feature: the carousel only advances when it is in view, so your visitors won't scroll down to find it half way through your images.

<div class="gallery" data-columns="1">
	<img src="/images/demo/demo-landscape.jpg">
	<img src="/images/demo/demo-landscape-2.jpg">
</div>

### What about videos?

Videos are an awesome way to show off your work in a more engaging and personal way, and we’ve made sure they work great on our themes. Just paste an embed code from YouTube or Vimeo, and the theme makes sure it displays perfectly:

<iframe src="https://player.vimeo.com/video/148003889" width="640" height="360" frameborder="0" allowfullscreen></iframe>

---

## Pretty cool, huh?

We've packed this theme with powerful features to show off your work.

Why not put them to use on your new portfolio?

<a href="https://jekyllthemes.io/theme/personal-website-jekyll-theme" class="button button--large">Get This Theme</a>