# Homework 2 - Data Manipulation

**Due:** Monday, February 13, 2023 by 4pm

Read the entire assignment before starting.

## Assignment

The goal of this assignment is to practice Arquero and D3 data manipulation.

### Report
You will be using JavaScript and Vega-Lite in an Observable notebook for this assignment.  In addition to writing code to answer the questions that are asked, you must also include an explanation of your code.  This will serve as your HW report. 

Remember that every report must have an appropriate heading (with HW name, your name, semester, due date, etc.), appropriate section headings, a References section, and an Appendix section.

### Datasets 

Use dataset(s) of your choosing. This could be the same as you used in HW1 or a different one.

*Your final project will be to create an interactive dashboard using dataset(s) of your choosing. Use this assignment as an opportunity to start investigating some interesting datasets.*

### Questions/Tasks

*The questions/tasks do not each need to be completed in a single Observable cell.*

First, briefly describe the dataset you've chosen. Discuss the most important attributes and their datatypes. 

**Q1.** Similar to **Q2** from our D3 Data Intro exercises, write a function to sort your dataset based on some criteria. This sort function should use the JavaScript arrow notation. Explain in words what you intend your sort function to do.  Demonstrate that this sort function works as intended.

**Q2.** In a single statement, import your data into an Arquero data structure and display the first 10 rows.  Display the last 10 rows.

**Q3.** Use Arquero to filter your dataset by some criteria. Explain in words what you intend your filter statement to do.

**Q4.** Use Arquero to pull the values from one of your attributes into an array.

**Q5.** Demonstrate the use of Arquero's `groupby()` and `rollup()` functions on your dataset. Explain in words what your operations are trying to show (or what question you're trying to answer). 

**Q6.** Take at least three non-nominal attributes in your dataset and use D3 functions to determine the range of values (i.e., min and max) in each of those attributes. One these attributes must be a date.  (If your dataset does not contain a date attribute, obtain a dataset with a date attribute for this portion of the question.)

**Q7.** Use Arquero to create a derived attribute on your data. The function to compute the derived attribute should use at least one of Arquero's `op`
 operators. Explain in words what the derived attribute represents.

**Q8.** Find or create a second dataset that shares a key with your dataset. Demonstrate the use of Arquero's `join()` (or filtered join with `semijoin()` or `antijoin()`). Explain in words how you have combined the two datasets.

**Q9.** Use Vega-Lite to create a chart from the resulting dataset from **Q5** (groupby/rollup), **Q7** (derived attribute), or **Q8** (joined data). The type of chart is up to you. Use appropriate axis labels, title, and tooltips.

**Q10.** Assume you'll be creating a horizontal bar chart with the values from a categorial attribute and one of your quantitative attributes. Create the D3 linear and band scales needed for the bar chart. Assume the chart dimensions (range) will be 500 (width) x 200 (height). Use `visualizeTicks()` to visualize the scales.  *You do not need to actually create the bar chart.*

## Evaluation Criteria

Your assignment will be evaluated on the following criteria:

* Was the data thoughtfully chosen?
* How well do the answers demonstrate an understanding of the Arquero and D3 functions?
* Does the report contain the required elements?
  * Attention to detail, including spelling, and overall aesthetics will be a factor.

## Submission

Submit the URL of your Observable notebook in the HW2 Assignment in Canvas.
