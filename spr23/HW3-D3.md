# Homework 3 - D3 Intro 
**Due:** Monday, February 27, 2023 by 4pm

*Read the entire assignment before starting.* 

## Assignment 

In this assignment, you'll be recreating some of the charts from HW1 using D3.

You will be using D3 in an Observable notebook for this assignment.  In addition to creating the charts that are assigned, you must also include an explanation of the charts and how you have created them.  

Make sure to refer to the examples in our [CS 725/825, Spring 2023 Observable Collection](https://observablehq.com/collection/@weiglemc/cs-725-825-spring-2023).

### Report

Your Observable notebook should function as your report.  This means that after successfully creating your charts, you must go back and edit your notebook to add Markdown cells with explanations, remove items that didn't work, etc. In general, make sure that it is clear what you have done to create the charts.

Make sure to 'unpin' any text cells and to 'pin' any code cells.

Your notebook must have a References section, with links to references that you used, and an Appendix section, with needed imports (D3, Arquero, Swatches, etc.)

### Dataset and Data Manipulation

You should use the same dataset(s) that you used for HW1.  However, you might want to do additional data manipulation outside of your charting code to make your D3 vis code simpler. Using Arquero is recommended (though not required).  (Since you'll be using the same data as in HW1, you may want to fork your HW1 notebook to get started.  If you attached a datafile to your HW1 notebook, the forked notebook will also include the datafile.)

**Note:** If you had comments from me on the appropriateness of your data to chart mapping in HW1, please talk with me before starting on your D3 code. I don't want you recreating exactly what you had in HW1 if it was not appropriate.

### Charts to Create

Use D3 in Observable to create the following charts.  You *do not* need tooltips or a legend for any of these charts (except where noted).  All of these are single charts (no repeating or faceting as we did with Vega-Lite).  

1. scatterplot
2. horizontal bar chart
3. line chart - single line
4. layered line and area chart - one area and at least one line - *talk to me if this won't make sense for your data*
5. multi-line chart - between 2-5 lines, each representing a different item or category, use color to distinguish the lines and `Swatches()` to generate a legend in the cell above your chart

*Extra Credit:* Create a small multiples grid visualization showing how a single quantative attribute changes over time for different values in a categorical attribute. (You may want to refer to the [NYU Vis Small Multiples notebook](https://observablehq.com/@nyuvis/small-multiples) for an example. In the unemployment rate example, the single attribute is unemployment rate and the categorical attribute is the state.)

## Submission

Submit the URL of your Observable notebook in the HW3 Assignment in Canvas.
