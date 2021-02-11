# Homework 2 - D3 Intro 
**Due:** Thursday, February 25, 2021 by 11:59pm

*Read the entire assignment before starting.* 

## Assignment 

In this assignment, you'll be recreating some of the charts from HW1 using D3.

Like with HW1, you will be using D3 in an Observable notebook for this assignment.  In addition to creating the charts that are assigned, you must also include an explanation of the charts and how you have created them.  

Since you'll be using the same data as in HW1, you may want to just fork your HW1 notebook to get started.  The forked notebook will include the datafile that you attached to your HW1.  You can use the same datafile, or you can download and attach a new one if you want to have updated stats.

Since different types of charts will use different scales, axes, margins, etc., you may create a separate notebook for each chart or for each type of chart.  It's up to you.  The notebook that contains your charts should also contain the explanation for that chart (i.e., don't separate your report description from your chart).  You can tie multiple notebooks together in a collection, as I've done with our [CS 725/825, Spring 2021 collection](https://observablehq.com/collection/@weiglemc/cs-725-825-spring-2021).  Your notebooks should be ordered appropriately in the collection, and each notebook must include your name, HW2, and the question number that you are addressing with the notebook.

### Dataset

We will be using the same dataset as in [HW1](https://github.com/cs725-infovis-master/public/blob/main/spr21/HW1.md):

> We are going to examine a dataset provided by the Virginia Department of Health (VDH) related to COVID-19. The dataset, [VDH-COVID-19-PublicUseDataset-Cases](https://data.virginia.gov/Government/VDH-COVID-19-PublicUseDataset-Cases/bre9-aqqr), has been made available through the [Virginia Open Data Portal](https://data.virginia.gov) and the [VDH's COVID-19 in Virginia page](https://www.vdh.virginia.gov/coronavirus/).  *Click the Export button on the dataset page to download the CSV.*

If you are using a collection, one option is to create a notebook that holds the various datasets and import them into the chart notebooks.  This way, you only need to attach the main datafile to a single notebook.  The data notebook needs to be made public so that you can import items into other notebooks.

### Charts to Create

Use D3 in Observable to create the following charts.  You do not need tooltips or a legend for any of these charts.  All of these will be single charts (no repeating or faceting as we did with Vega-Lite).  You must provide an explanation of your code.

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
3. Line Chart 1 - time series of total cases in VA over time
  * x: time
  * y: cases per day
4. Superimposed Line Chart - time series of total cases over time for certain health districts
  * *this was called Layered Line Chart in HW1*
  * filter for only these health districts: Western Tidewater, Chesapeake, Virginia Beach, Norfolk, Portsmouth, Hampton, Peninsula
  * x: time
  * y: cases per day summed over a district
  * color: health district
5. Line Chart 2 - time series of total cases over time for a single health district (your choice)
  * filter for only a single health district
  * x: time
  * y: cases per day summed over a district
6. Horizontal Bar Chart - total cases for certain health districts 
  * filter for only these health districts: Western Tidewater, Chesapeake, Virginia Beach, Norfolk, Portsmouth, Hampton, Peninsula
  * x: total cases
  * y: health district
  * bars should be sorted descending by total cases

### Hints

In D3, you will usually want to transform your data appropriately outside of your charting code. 

When parsing the datafile, you can sort the data by date in the same cell:

~~~js
covid = d3.csvParse(await FileAttachment("VDH-COVID-19-PublicUseDataset-Cases@4.csv").text(), function(d) {
  return {
    date: d3.timeParse("%x")(d["Report Date"]),
    fips: d.FIPS,
    locality: d.Locality,
    district: d["VDH Health District"],
    cases: +d["Total Cases"],
    hospitalizations: +d.Hospitalizations,
    deaths: +d.Deaths
  };})
  .sort(function (a, b) {return a.date - b.date;});
~~~

For Chart 2 (cases vs. hospitalizations), you'll need to rollup and sum multiple attributes.  You can use the following JavaScript code to do this, but you will need to explain how it works in your notebook.

~~~js
casesHospPerDay = 
 d3.rollups(covid, v => [d3.sum(v, d => d.cases), d3.sum(v, d => d.hospitalizations)], d => d.date)
   .map(obj => {let rObj= {}; rObj["date"] = obj[0]; rObj["cases"] = obj[1][0]; 
                rObj["hospitalizations"] = obj[1][1]; return rObj;})
~~~

## Submission

There are two steps to submission:

1. Publish your Observable notebook/collection to make it viewable.
  * If you are using a collection, you must Publish all notebooks in the collection and make the collection itself Public.
  * I will use the latest published/edited timestamp as your submission date. 
  * You can edit your notebook after publishing, but the changes will not be viewable until you "Re-publish" the notebook.

2. Submit the URL of your Observable notebook/collection in Blackboard:
  * Click on HW2 under Assignments.
  * Under "Assignment Submission", click the "Write Submission" button.
  * Copy/paste the URL of your Observable notebook/collection into the edit box. (If you have created a collection, you only need to provide the URL of the collection, not the individual notebooks.)
  * Make sure to "Submit" your assignment or I will not be able to find your notebook or grade your work.
