# Homework 1 - Vega-Lite Intro

**Due:** Monday, January 30, 2022 by 4pm

Read the entire assignment before starting.

## Assignment

You will be using Vega-Lite in an Observable notebook to create five different charts using a data of your choice.  

### Report

In addition to creating the charts that are assigned, you must also include an explanation of the charts and how you have created them.  This will serve as your report. Use some of the references that we've covered as examples for mixing explanation with charts.  For instance, the [Introduction to Vega-Lite notebook](https://observablehq.com/@uwdata/introduction-to-vega-lite?collection=@uwdata/visualization-curriculum) does a nice job of showing the code and explaining what's being done.

Every report must have the following elements:

* Appropriate heading (example below)

```markdown
# HW1 - Vega-Lite
Your Name Here  
CS 725/825, Spring 2023  
Due: Jan 30, 2023
```

* Markdown formatted sections for each of the required charts - make it easy for me to be able to determine that you've complete all elements of the assignment
* References section - list of examples you've referred to, include links
* Appendix - include the import statements for the vega-lite-api, arquero, and any other libraries used

### Dataset

Use one or more datasets of your choosing.  The goal of this assignment is to allow you to practice creating different types of charts using Vega-Lite and to gain more experience with how different charts are appropriate for different types of data.

You must have a section in your report labeled "Data" where you describe the dataset(s) you've chosen. This should include the source of your data (with a link) and why you chose that dataset.

*Note that your final project will be to create an interactive dashboard using a dataset of your choosing. Use this assignment as an opportunity to start investigating some interesting datasets.*

### Charts

Create the following charts:

1. scatterplot
2. horizontal bar chart
3. repeated line chart - multiple separate line charts in a single row (use `repeat()` and `columns()`)
4. layered line chart - single chart with multiple lines
5. faceted line chart - multiple line charts in a single row with a single y-axis label) (use `column()`)

All charts must contain:

* helpful [tooltips](https://vega.github.io/vega-lite/docs/tooltip.html)
* appropriate axis labels
* an informative chart title, ideally this should be a headline (i.e., an interesting observation) instead of just a description of the chart
* a [subtitle](https://vega.github.io/vega-lite/docs/title.html) that contains information about the data source

In addition, you must explain how each chart you've created is appropriate for the data source that was used.

## Submission

Submit the URL of your Observable notebook in the HW1 Assignment in Canvas.
