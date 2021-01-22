# Homework 1 - Vega-Lite Intro 
**Due:** Thursday, February 4, 2021 by 11:59pm

*Read the entire assignment before starting.*

## Assignment

### Report
You will be using Vega-Lite in an Observable notebook for this assignment.  In addition to creating the charts that are assigned, you must also include an explanation of the charts and how you have created them.  Use some of the references that we've covered as examples for mixing explanation with charts.  For instance, the [Vega-Lite Chart Types notebook](https://observablehq.com/@observablehq/vega-lite-chart-types) does a nice job of showing the code and explaining what's being done.

To get started, login to Observable and fork the [CS725/825, Spr21 - HW1 - Vega-Lite Intro  notebook](https://observablehq.com/@weiglemc/cs-725-825-spr21-hw1-vega-lite-intro?collection=@weiglemc/cs-725-825-spring-2021).  This provides a template for your report and some data processing code to help you get started.

### Dataset

We are going to examine a dataset provided by the Virginia Department of Health (VDH) related to COVID-19. The dataset, [VDH-COVID-19-PublicUseDataset-Cases](https://data.virginia.gov/Government/VDH-COVID-19-PublicUseDataset-Cases/bre9-aqqr), has been made available through the [Virginia Open Data Portal](https://data.virginia.gov) and the [VDH's COVID-19 in Virginia page](https://www.vdh.virginia.gov/coronavirus/).  *Click the Export button on the dataset page to download the CSV.*

> This data set includes the **cumulative (total) number of COVID-19 cases, hospitalizations, and deaths for each locality in Virginia by report date**. This data set was first published on April 01, 2020. The data set increases in size daily and as a result, the dataset may take longer to update; however, it is expected to be available by 12:00 noon daily. When you download the data set, the dates will be sorted in ascending order, meaning that the earliest date will be at the top. To see data for the most recent date, please scroll down to the bottom of the data set. The Virginia Department of Health’s Thomas Jefferson Health District (TJHD) will be renamed to Blue Ridge Health District (BRHD), effective January 2021. More information about this change can be found here: https://www.vdh.virginia.gov/blue-ridge/name-change/

Download and attach the dataset to the notebook you forked earlier.  See [File Attachments](https://observablehq.com/@observablehq/file-attachments) for more information.

### Charts to Create

Use Vega-Lite in Observable to create the following charts. All charts should contain helpful tooltips. You must provide an explanation of your code.

Note: When asked for totals (not over time), you should use only the last day of data since the data reported is cumulative.

1. Scatterplot 1 - total cases vs. deaths per locality
  * x: cases
  * y: deaths
  * each point represents the total number of cases and deaths for a particular locality
2. Scatterplot 2 - total cases vs. hospitalizations in VA over time
  * for each date, sum the cases and hospitalizations over all localities
  * x: cases
  * y: hospitalizations
  * each point represents the number of total cases and hospitalizations in the state as of a particular day
3. Repeated Line Chart - time series of total cases, hospitalizations, and deaths in VA over time
  * x: time
  * y: {cases, hospitalizations, deaths} per day
  * three separate line charts in a single row
4. Layered Line Chart - time series of total cases over time for certain health districts
  * filter for only these health districts: Western Tidewater, Chesapeake, Virginia Beach, Norfolk, Portsmouth, Hampton, Peninsula
  * x: time
  * y: cases per day summed over a district
  * color: health district
5. Faceted Line Chart - time series of total cases over time for certain health districts
  * filter for only these health districts: Western Tidewater, Chesapeake, Virginia Beach, Norfolk, Portsmouth, Hampton, Peninsula
  * x: time
  * y: cases per day summed over a district
  * one line chart for each district (should be all in a single row with a single y-axis label)
6. Horizontal Bar Chart - total cases for certain health districts 
  * filter for only these health districts: Western Tidewater, Chesapeake, Virginia Beach, Norfolk, Portsmouth, Hampton, Peninsula
  * x: total cases
  * y: health district
  * bars should be sorted descending by total cases
7. Boxplot - total cases per health district
  * sum over all localities in each health district (include all in the state)
  * a single boxplot of total cases per health district

## Submission

There are two steps to submission:

1. Publish your Observable notebook to make it viewable.
  * I will use the latest published/edited timestamp as your submission date. (To see this timestamp, hover over the date next to "Published" near the top of the notebook.)
  * You can edit your notebook after publishing, but the changes will not be viewable until you "Re-publish" the notebook.

2. Submit the URL of your Observable notebook in Blackboard:
  * Click on HW1 under Assignments.
  * Under "Assignment Submission", click the "Write Submission" button.
  * Copy/paste the URL of your Observable notebook into the edit box.
  * Make sure to "Submit" your assignment or I will not be able to find your notebook or grade your work.
