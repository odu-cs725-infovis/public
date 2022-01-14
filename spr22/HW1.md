# Homework 1 - Vega-Lite Intro 
**Due:** *Wednesday*, January 26, 2022 by 11:59pm

Read the entire assignment before starting.

## Assignment

### Report
You will be using Vega-Lite in an Observable notebook for this assignment.  In addition to creating the charts that are assigned, you must also include an explanation of the charts and how you have created them.  This will serve as your HW report. Use some of the references that we've covered as examples for mixing explanation with charts.  For instance, the [Introduction to Vega-Lite notebook](https://observablehq.com/@uwdata/introduction-to-vega-lite?collection=@uwdata/visualization-curriculum) from [UW IDL](https://idl.cs.washington.edu/) does a nice job of showing the code and explaining what's being done.

Use Markdown formatting to create sections for each of the required charts.  Make it easy for me to be able to determine that you've complete all elements of the assignment.

Every report must have a References and an Appendix section (see our [Vega-Lite Breakout notebook](https://observablehq.com/@weiglemc/cs-725-s22-vega-lite-breakout-notebook?collection=@weiglemc/cs-725-825-spring-2022) for an example).

**Getting Started**
* Login to Observable
* Create a new notebook
* At the top of the notebook, create a Markdown cell and copy/paste the following Markdown code (including the extra spaces at the end of the lines), with edits as appropriate:

```markdown
# HW1 - CS 725/825, Spring 2022
Your Name Here  
Due: Jan 26, 2022
```

### Dataset

We are going to examine a dataset provided by the Virginia Department of Health (VDH) related to COVID-19. The dataset, [Tests_by-LabReportDate](https://data.virginia.gov/Government/VDH-COVID-19-PublicUseDataset-Tests_by-LabReportDa/3u5k-c2gr), has been made available through the [Virginia Open Data Portal](https://data.virginia.gov) and the [VDH's COVID-19 in Virginia page](https://www.vdh.virginia.gov/coronavirus/). 

> This data set includes the number of COVID-19 testing encounters and positive tests for PCR tests and all test types for each [health district in Virginia](https://www.vdh.virginia.gov/local-health-districts/) by lab report date. This data set was first published on May 15, 2020. The data set increases in size daily and as a result, the dataset may take longer to update; however, it is expected to be available by 12:00 noon daily. 

You can either download the CSV (*click the Export button on the dataset page*) and attach the dataset to your notebook (see [File Attachments](https://observablehq.com/@observablehq/file-attachments)) or use the SODA API to have the notebook obtain the latest data when it's run (see the [Using SODA API to access data from the Virginia Open Data Portal notebook](https://observablehq.com/@weiglemc/using-the-soda-api-to-access-data-from-the-virginia-open-data?collection=@weiglemc/cs625) from CS 625).

This dataset contains data similar to that displayed at the [VDH Testing - Coronavirus page](https://www.vdh.virginia.gov/coronavirus/see-the-numbers/covid-19-in-virginia/covid-19-in-virginia-testing/). You should use that to sanity-check your charts.

### Data Cleaning/Manipulation

There is some data cleaning that will need to be performed on the data before charts can be created.  I would encourage the use of the [Arquero library](https://uwdata.github.io/arquero/api/) for this.
* Remove any row where the `lab_report_date` is "Not Reported".
* Remove any row where the `health_district` is "Out of State" or "Unknown".
* Remove any row where the number of PCR tests given is less than 100 (small sample sizes can result in artificially large positivity rates).

You will also need to calculate the positivity rate (or, % positivity) for PCR tests.  As explained in [COVID-19 Testing: Understanding the “Percent Positive”](https://publichealth.jhu.edu/2020/covid-19-testing-understanding-the-percent-positive) from Johns Hopkins, the percent positivity is calculated as (positive tests)/(total tests) x 100%. Create this derived data from the number of PCR tests given and the number of positive PCR tests.

For some charts, you will need to filter to include data from only the latest report date.

For some charts, you will need to filter to include data from only health districts in Hampton Roads.  The following JavaScript code creates a Set with the names of the HR districts.  You can use this along with the `has()` function to determine if a health district in the dataset belongs to this group.
```javascript
hr_districts = new Set(["Western Tidewater", "Peninsula", "Chesapeake", "Virginia Beach", "Norfolk", "Portsmouth", "Hampton"])
```

### Charts to Create

Use Vega-Lite in Observable to create the following charts. All charts should contain helpful [tooltips](https://vega.github.io/vega-lite/docs/tooltip.html), appropriate axis labels, and an informative chart title. If possible, your chart title should be a headline (i.e., an interesting observation) instead of just a description of the chart. Information about the data source should be noted in the chart [subtitle](https://vega.github.io/vega-lite/docs/title.html).

1. Scatterplot 1 - number of PCR tests administered vs. PCR positivity rate
  * x: number of PCR tests given
  * y: % PCR positivity
  * each point represents a particular health district on a given report date
2. Scatterplot 2 - number of PCR tests administered vs. PCR positivity rate (latest report date)
  * x: number of PCR tests given
  * y: % PCR positivity
  * each point represents a particular health district for the latest report date only 
3. Repeated Line Chart - time series of number PCR tests given, number PCR tests positive in VA over time
  * x: time
  * y: {number PCR given, number PCR positive} per lab report day
  * sum data over all health districts for each report day
  * two separate line charts in a single row (hint: use `repeat()` and `columns(2)`)
4. Layered Line Chart -  time series of number PCR tests given, number PCR tests positive in VA over time
  * x: time
  * y: {number PCR given, number PCR positive} per lab report day
  * sum data over all health districts for each report day (same data as previous chart)
  * single chart with number of PCR tests given as line mark (default color) and number of positive PCR tests as line mark with color `#f6ac23`
5. Faceted Line Chart - time series of % PCR positivity for HR health districts
  * filter for only the Hampton Roads health districts
  * x: time
  * y: % PCR positivity per report day 
  * one line chart for each district (should be all in a single row with a single y-axis label) (hint: use `column()`)
6. Horizontal Bar Chart - latest % PCR positivity for certain health districts 
  * filter for only the Hampton Roads health districts
  * x: % PCR positivity (for latest report date only)
  * y: health district
  * bars should be sorted descending by % PCR positivity

## Submission

There are two steps to submission:

1. Publish your Observable notebook to make it viewable.
  * Set the Visibility as "Unlisted" rather than "Public"
  * I will use the latest published/edited timestamp as your submission date. (To see this timestamp, hover over the date next to "Published" near the top of the notebook.)
  * You can edit your notebook after publishing, but the changes will not be viewable until you "Re-publish" the notebook.

2. Submit the URL of your Observable notebook in Blackboard:
  * Click on HW1 under Assignments.
  * Under "Assignment Submission", click the "Write Submission" button.
  * Copy/paste the URL of your Observable notebook into the edit box.
  * Make sure to "Submit" your assignment or I will not be able to find your notebook or grade your work.
