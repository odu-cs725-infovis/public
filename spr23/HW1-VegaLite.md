# Homework 1 - Vega-Lite Intro

**Due:** Monday, January 30, 2023 by 4pm

Read the entire assignment before starting.

## Assignment

You will be using Vega-Lite in an Observable notebook to create five different charts using data of your choice.  

The main objectives of this assignment are that you will:

* gain more experience in determining what visualization idioms are appropriate for different types of data
* gain experience creating different types of charts using Vega-Lite
* investigate data sources and datasets that might be of interest for your final visualization project

### Report

In addition to creating the charts that are assigned, you must also include an explanation of the data used, the charts you have created, and how you have created the charts. This will serve as your report and should be incorporated into your Observable notebook along with your charts.

* Use some of the references that we've covered as examples for mixing explanation with charts.  For instance, the [Introduction to Vega-Lite notebook](https://observablehq.com/@uwdata/introduction-to-vega-lite?collection=@uwdata/visualization-curriculum) does a nice job of showing the code and explaining what's being done.
* Observable cells containing source code should be visible and cells containing Markdown source should be hidden.

Your report must have the following elements:

* Appropriate heading (Markdown example below). This must be included on every assignment this semester. Update the HW title, your name, and due date for each assignment.

```markdown
# HW1 - Vega-Lite
Your Name Here  
CS 725/825, Spring 2023  
Due: Jan 30, 2023
```

* Markdown formatted sections for each of the required charts - make it easy for me to be able to determine that you've complete all elements of the assignment
* Data section - describe the dataset(s) you've chosen, including the source of your data (with a link) and why you chose that dataset
* References section - list of examples you've referred to, include links
* Appendix - include the import statements for the vega-lite-api, arquero, and any other libraries used

### Dataset

Use one or more datasets of your choosing.  

*Your final project will be to create an interactive dashboard using dataset(s) of your choosing. Use this assignment as an opportunity to start investigating some interesting datasets.*

### Charts

Create the following charts:

1. scatterplot
2. horizontal bar chart
3. repeated line chart - multiple separate line charts in a single row (use `repeat()` and `columns()`)
4. layered line chart - single chart with multiple lines
5. faceted line chart - multiple line charts in a single row with a single y-axis label (use `column()`)

All charts must contain:

* helpful [tooltips](https://vega.github.io/vega-lite/docs/tooltip.html)
* appropriate axis labels
* an informative chart title
  * should be a headline (i.e., an interesting observation) instead of just a description of the axes
* a [subtitle](https://vega.github.io/vega-lite/docs/title.html) that contains information about the data source

In addition, you must explain how each chart you've created is appropriate for the data source that was used.

## Evaluation Criteria

Your assignment will be evaluated on the following criteria:

* Does the implemented chart match the assigned chart type?
* Is the visualization idiom appropriate for the data that is shown?
* Does the chart contain the required elements?
  * Attention to detail, including spelling, and overall aesthetics will  be a factor.
* Was the data thoughtfully chosen?
  * For example, more credit will be given for datasets selected from original sources rather than those found on Kaggle or standard example datasets.
* Does the report contain the required elements?
  * Attention to detail, including spelling, and overall aesthetics will  be a factor.

## Submission

Submit the URL of your Observable notebook in the HW1 Assignment in Canvas.
