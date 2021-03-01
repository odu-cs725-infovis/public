# Visualization Project

Choose a real-world dataset and develop an interactive dashboard visualization that allows users to better understand the data, such as by discovering patterns, identifying outliers, confirming or rejecting hypotheses, etc.

A well-chosen dataset is key to creating an interesting project.  Choose something that you either already know about or that you're willing to learn about.  The context that you can provide will help determine what features should be highlighted to help the user better understand the data.

All projects will be demonstrated live in class.  These will be scheduled between **April 13-27** with 3 presentations per class meeting.  

For some inspiration, this [slideset](https://courses.cs.washington.edu/courses/cse442/20au/lectures/CSE442-FinalProjects.pdf) contains links to demo videos from projects for Jeffrey Heer's Fall 2020 data visualization course. Note that I am not necessarily expecting this type of output. Their assignment was different and was a group project, but this can give you some ideas of things that could be done. 

## Mechanics

Project topic selection and demo scheduling will be done through Piazza in the "project" folder.  Once all project topics have been chosen, we'll start scheduling the demos in a similar manner.  No two students may choose the exact same dataset.  (Though as I mentioned in class, if multiple students want to look at COVID data, there are lots of different types of that available, from international to national to US state-level data.)

I would prefer for all students to deliver their demos live in Zoom. If you are not able to attend on your scheduled demo date, you may pre-record your demo -- but this must be approved by me ahead of time. Before class time on the day of your scheduled demo, submit a link to the recording (don't try to attach the actual video file) on Blackboard.

Your project must be implemented in Vega-Lite or D3. You may build your project in Observable or on a stand-alone webpage. Here are some references for going from an Observable notebook to a stand-alone webpage: 
* [Advanced Embedding and Downloading](https://observablehq.com/@observablehq/downloading-and-embedding-notebooks)
* [Observable to standalone](https://projet.liris.cnrs.fr/mi2/posts/2019/09/11/observable-to-standalone.html)

You will also provide a report about the design of your project.  This should be done as a Markdown document separate from your project visualization page.  Details are below.  

Your project page/notebook must include your name, CS 725/825 (as appropriate), Spring 2021, and a link to your report.

## Project Guidelines

Your visualization must be in a dashboard design, meaning that it employs multiple interactive charts that allow the user to ask and answer questions about the data.  You may add widgets such as drop-down menus, radio buttons, etc. to provide filtering functions.  There should also be some amount of direct interaction with the charts themselves, at the very least in the form of tooltips. You are encouraged to use brushing and linking and chart navigation (pan/zoom or focus+context) as appropriate. The interactive elements must add value. *Do not add interactivity just because you can.*

Your project may not allow users to just "explore" the data.  *You must have some specific tasks or goals in mind for the visualization.*  Credit to Eytan Adar, ["Banning exploration in my infovis class"](https://medium.com/@eytanadar/banning-exploration-in-my-infovis-class-9578676a4705) (*read this*), for articulating this.  Here are some highlights from that article: 
* "If you’re not seeking anything in particular, any tool that lets you meander through data is perfectly reasonable. It makes the job of deriving insight completely the responsibility of the end-user. In that world, any decision is a reasonable one, evaluation is unnecessary, and there is no grade but an A. But that’s not the real world and so I’ve banned 'explore.'"
* "Forcing students to tell me what they want the end-user to find and/or what decisions they want to enable has led to better projects."
* "What I think is going on is that the students are confusing their own exploration of the data with what the end-user’s exploration will look like. That is, they are mistaking the design task of familiarizing themselves with the data with what the analyst might do."

If appropriate for your data, you are encouraged to employ machine learning (ML) techniques, such as clustering or multi-dimensional scaling, and allow the user to adjust the ML parameters and visualize the results.

## Grading

This assignment is worth 25% of your final grade. 

Your project and report will be largely evaluated on how well they meet the guidelines provided here.  Additional considerations will be made for differences in difficulty (i.e., D3 vs. Vega-Lite), aesthetics, and project ambition.

## Report

Your report must be done in Markdown. Points will be deducted for missing sections, excessive typos or grammatical errors, or a report that is difficult to read.  You may create your report in GitHub or in an Observable notebook separate from your project. 

Your report must include the following sections:

**Introduction.** Describe your visualization topic and motivation for why you chose this topic. Describe the main questions that you are attempting to address (or allow the user to ask) with your visualization.

**Data.** Describe the dataset that you used, including links to the original data sources. As different visualizations can emphasize different aspects of a data set, you should document what aspects of the data you are attempting to most effectively communicate. 

**Visualization.** Describe your visualization. Explain any interactive elements you employed. Address how the visualization addresses the questions you raised in the Introduction.

**Design Decisions.** You must explain every design decision you make and essentially be able to explain the contribution of every pixel in the display. 
* For each chart in your dashboard, document the visual encodings (idioms, marks, channels) you used and why they are appropriate for the data. These decisions include the choice of visualization idiom, size, color, scale, and other visual elements, as well as the use of sorting or other data transformations. How do these decisions facilitate effective communication?  
* Include a description of the principles of effective dashboard design that you used.
* Provide a justification for the interactive elements (filters, facets, etc.) that you provide. Why is this particular representation of the data useful?  How does the interaction contribute to the user's insight into the data?

**Development Process.** Include a commentary on the development process, including answers to the following questions:
* Roughly how much time did you spend developing your visualization?
* What aspects took the most time?

**References.** Include a list of any pre-existing resources (e.g. Stack Overflow, Observable notebooks, etc.) used in your implementation.

## Demo

You will have at most 20 minutes for your demo, but I expect that most projects could be demonstrated in about 10 minutes.  You do not need to provide slides, but you should plan out your demo in advance.  

Your demo should contain the following elements:
* Briefly describe the problem and data you're visualizing.
* Highlight the main features of the visualization by walking through a scenario (or multiple scenarios).
* Demonstrate that the visualization provides effective representation of the data, uses appropriate colors, and supports multiple tasks through interactivity.

You may also want to talk about significant things you learned (such as helpful tips or pitfalls to avoid) while implementing your project.

In addition, you should be prepared to answer questions about your visualization and its implementation after the demo.

## Submission

Before class time on your demo day, submit the links to your project and your project report in Blackboard.  If you use an Observable notebook, make sure that you Publish the notebook so that it is viewable.
* Click on Project under Assignments.
* Under "Assignment Submission", click the "Write Submission" button.
* Copy/paste the URLs of your Observable notebook and report into the edit box. 
* Make sure to "Submit" your assignment.
