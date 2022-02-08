# Homework 3 - D3 Intro

**Due:** Wednesday, February 23, 2022 by 11:59pm

*Read the entire assignment before starting.*

## Assignment

In this assignment, you'll be recreating some of the charts from HW1 using D3.

Like with HW1, you will be using D3 in an Observable notebook for this assignment.  In addition to creating the charts that are assigned, you must also include an explanation of the charts and how you have created them.  

Since you'll be using the same data as in HW1, you may want to just fork your HW1 notebook to get started.  If you attached a datafile to your HW1 notebook, the forked notebook will also include the datafile.  You can use the same datafile, or you can download and attach a new one if you want to have updated stats.

Make sure to refer to the examples in our [CS 725/825, Spring 2022 Observable Collection](https://observablehq.com/collection/@weiglemc/cs-725-825-spring-2022).

### Report

Your Observable notebook should function as your report.  This means that after successfully creating your charts, you must go back and edit your notebook to add Markdown cells with explanations, remove items that didn't work, etc. In general, make sure that it is clear what you have done to create the charts.

Make sure to 'unpin' any text cells and to 'pin' any code cells.

Your notebook must have a References section, with links to references that you used, and an Appendix section, with needed imports (d3, Arquero, Swatches, etc.)

### Dataset

We will be using the same dataset as in [HW1](https://github.com/odu-cs725-infovis/public/blob/main/spr22/HW1.md):

> We are going to examine a dataset provided by the Virginia Department of Health (VDH) related to COVID-19. The dataset, [Tests_by-LabReportDate](https://data.virginia.gov/Government/VDH-COVID-19-PublicUseDataset-Tests_by-LabReportDa/3u5k-c2gr), has been made available through the [Virginia Open Data Portal](https://data.virginia.gov) and the [VDH's COVID-19 in Virginia page](https://www.vdh.virginia.gov/coronavirus/). You can either download the CSV (*click the Export button on the dataset page*) and attach the dataset to your notebook or use the SODA API to have the notebook obtain the latest data when it's run.

This dataset contains data similar to that displayed at the [VDH Testing - Coronavirus page](https://www.vdh.virginia.gov/coronavirus/see-the-numbers/covid-19-in-virginia/covid-19-in-virginia-testing/). You should use that to sanity-check your charts.

### Data Manipulation

For the most part, you should be able to use same data manipulation code from HW1.  Note that if you had errors in your HW1, you will need to correct your data those before creating the D3 charts.

For all charts, filter out rows with:

* lab_report_date: "Invalid Date", "Not Reported"
* health_district: "Out of State", "Out Of State", "Unknown"

For charts that use percent positivity, only compute this metric for dates where at least 100 tests were administered.

You can use the following code to generate a Set of the Hampton Roads health districts:

```js
hr_districts = new Set(["Western Tidewater", "Peninsula", "Chesapeake", "Virginia Beach", "Norfolk", "Portsmouth", "Hampton"])
```

It is recommended that you use Arquero to do all of the needed data manipulation in advance, outside of your charting code.

### Charts to Create

Use D3 in Observable to create the following charts.  You do not need tooltips or a legend for any of these charts.  All of these will be single charts (no repeating or faceting as we did with Vega-Lite).  

1. Horizontal Bar Chart - latest percent positivity for Hampton Roads health districts
   * x: % PCR positivity (for latest report date only)
   * y: health district
   * bars should be sorted descending by % PCR positivity
2. Scatterplot - number of PCR tests administered vs. PCR positivity rate (latest report date)
   * x: number of PCR tests given
   * y: % PCR positivity
   * each point represents a particular health district for the latest report date only
3. Line Chart - time series of % PCR positivity for the entire state
   * x: time
   * y: % PCR positivity per report day
4. Layered Area and Line Chart - time series of number PCR tests given, number PCR tests positive in VA over time
   * x: time
   * y: {number PCR given, number PCR positive} per lab report day
   * sum data over all health districts for each report day
   * single chart with number of PCR tests given as an area mark with color 'steelblue' and number of positive PCR tests as line mark with color `#f6ac23`
5. Multi-Line Chart - time series of % PCR positivity for 3 health districts (your choice)
   * x: time
   * y: % PCR positivity per report day
   * color: health district -- use `Swatches()` to generate a legend in the cell above your chart
   * for best readability, choose 3 districts that experienced waves at different times (for instance, one district in Northern VA, one in Hampton Roads, and one in Southwest VA)

*Extra Credit:* Create a small multiples grid visualization showing the % PCR positivity as area charts for each health district over time. You may want to refer to the [NYU Vis Small Multiples notebook](https://observablehq.com/@nyuvis/small-multiples) for an example.

## Submission

There are two steps to submission:

1. Publish your Observable notebook to make it viewable.
   * Set the Visibility as "Unlisted" rather than "Public"
   * I will use the latest published/edited timestamp as your submission date.
   * You can edit your notebook after publishing, but the changes will not be viewable until you "Re-publish" the notebook.

2. Submit the URL of your Observable notebook in Blackboard:
   * Click on HW3 under Assignments.
   * Under "Assignment Submission", click the "Write Submission" button.
   * Copy/paste the URL of your Observable notebook into the edit box.
   * Make sure to "Submit" your assignment or I will not be able to find your notebook or grade your work.
