# Homework 2 - Data Manipulation
**Due:** *Wednesday*, February 9, 2022 by 11:59pm

Read the entire assignment before starting.

## Assignment

The goal of this assignment is to practice Arquero and D3 data manipulation and produce Vega-Lite charts to see the result of the data manipulation.  We will continue to examine COVID-19 data from the Virginia Department of Health (VDH), made available through the [Virginia Open Data Portal](https://data.virginia.gov) and the [VDH's COVID-19 in Virginia page](https://www.vdh.virginia.gov/coronavirus/)

### Report
You will be using JavaScript and Vega-Lite in an Observable notebook for this assignment.  In addition to writing code to answer the questions that are asked, you must also include an explanation of your code.  This will serve as your HW report. Remember that every report must have a References and an Appendix section.

**Getting Started**
* Login to Observable
* Create a new notebook
* At the top of the notebook, create a Markdown cell and copy/paste the following Markdown code (including the extra spaces at the end of the lines), with edits as appropriate:

```markdown
# HW2 - CS 725/825, Spring 2022
Your Name Here  
Due: Due Date Here
```

### Datasets 

There are two options for this assignment, but both will use the Virginia population dataset developed at https://observablehq.com/@weiglemc/cs725-s22-virginia-population-data-manipulation.  To import this data, use
```js
import {state_population} from "@weiglemc/cs725-s22-virginia-population-data-manipulation"
```

You may choose to use the SODA API to access the other VDH datasets.  To help with this, you may want to import the `buildURI()` function using
```js
import {buildURI} from "@weiglemc/using-the-soda-api-to-access-data-from-the-virginia-open-data"
```

You may choose to examine either vaccines or {infections, hospitalizations, deaths}:
* daily vaccines administered per locality - https://data.virginia.gov/Government/VDH-COVID-19-PublicUseDataset-Vaccines-DosesAdmini/28k2-x2rj
* weekly data of new {infections, hospitalizations, deaths} per Virginia health region - https://data.virginia.gov/dataset/VDH-COVID-19-PublicUseDataset-Cases-by-Vaccination/vsrk-d6hx

### Questions/Tasks

**Q1.** Perform appropriate data cleaning and aggregation on your chosen dataset.

vaccines
* we only want to look at rates of full vaccination (and we'll simplify this to mean 2 doses), so only request data for `dose_number=2` (API hint: use `buildURI("28k2-x2rj", 500000, "&dose_number=2")` to request this data)
* make sure to filter out any "Out of State", "Not Reported", or other rows that don't correspond to a particular locality
* aggregate the vaccine doses adminstered by date and locality (we don't care about the manufacturer or facility where given)

{infections, hospitalizations, deaths}
* there will be multiple report dates in the dataset, filter the data to keep only the latest report date
* make sure to filter out any "Out of State", "Not Reported", or other rows that don't correspond to a particular health region
* choose one of the {infections, hospitalizations, deaths} attributes to use going forward
* aggregate your chosen attribute by `week_ending_date` and health region

**Q2.** Use D3 functions to determine the range of dates in your dataset.

**Q3.** Use D3 functions to determine the range of values (over all dates) for your chosen attribute. 

**Q4.** Use D3 functions to determine the range of values and the median for your chosen attribute on the latest date.

**Q5.** Join the population dataset to your aggregated dataset to produce an aggregated dataset over time per health region.
* vaccines - after joining, you should have a population attribute for each locality, then aggregate the vaccines administered and population by date and health region
  * Note that not all localities administered shots every day, so double-check your calculation of population per health region against the population dataset.
* {infections, hospitalizations, deaths} - you should aggregate the data to produce a population attribute for each health region
  * Note that for the join to work, you'll need to normalize the value in `health_region` in the two datasets.  Either remove " Region" from the items in this dataset or add " Region" to the values in the population dataset.

**Q6.** Derive a new attribute that represents the rate of occurrence of your chosen attribute per 100,000 people. This allows us to compare data between areas that have different sized populations.  The general formula is `rate_per_100k = (attribute / population) * 100000`. For example, if there were 100 COVID cases in one week and there were 200,000 people, then  

`rate_per_100k = (100 / 200,000) * 100000 = 50`  

This means that this rate is equivalent to 50 cases in a population of 100,000.

The data for vaccines is noisy (since it's daily data), so compute a 7-day rolling average over each health region (see [Arquero Cookbook: Rolling Average](https://observablehq.com/@uwdata/arquero-cookbook?collection=@uwdata/arquero#rolling_avg)).

**Q7.** Use Vega-Lite to create a layered line chart showing the rate per 100k (or 7-day rolling average) of your attribute over time for each health region.  Use appropriate axis labels, title, and tooltips.

**Q8.** Use Vega-Lite to create a horizontal bar chart showing your attribute summed over time for each health region.  Sort the bars in descending order (i.e., longest bar at the top).  The chart should have a height of 150 and width of 400

**Q9.** To create the same bar chart as Q8 in D3, we first need to set up D3 scales to calculate the domain and range for the x and y axes.  Create the scales (height 150, width 400) and demonstrate the values generated with:
* x-axis: min, max, and median values from your dataset
* y-axis: 'Northern', 'Eastern', and 'Southwest' health regions

**Q10.** Compare the bar chart in Q8 to the values you computed in Q9.  Explain how the values produced match up to the dimensions of the bar chart in Q8.

## Submission

There are two steps to submission:

1. Publish your Observable notebook to make it viewable.
  * Set the Visibility as "Unlisted" rather than "Public"
  * I will use the latest published/edited timestamp as your submission date. (To see this timestamp, hover over the date next to "Published" near the top of the notebook.)
  * You can edit your notebook after publishing, but the changes will not be viewable until you "Re-publish" the notebook.

2. Submit the URL of your Observable notebook in Blackboard:
  * Click on HW2 under Assignments.
  * Under "Assignment Submission", click the "Write Submission" button.
  * Copy/paste the URL of your Observable notebook into the edit box.
  * Make sure to "Submit" your assignment or I will not be able to find your notebook or grade your work.
