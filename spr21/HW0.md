# Homework 0: Tool Setup

**Recommended Due Date:** Friday, January 22, 2021

This is an *optional, but highly recommended* assignment. It will cover the necessary steps to get set up for the semester.  There is nothing to submit, but there are review questions listed so that you can assess your own understanding.

*For this assignment only -- you may ask others in the class for help with these setup tasks.  Please use Piazza and post in the `hw0` folder for these questions so that others may benefit from the answers.*

## ODU-CS Linux

We will be using the [ODU-CS Linux systems](https://systems.cs.odu.edu/Unix_and_Linux_Services) for part of the course (read the information in the linked webpage). If you do not already have an account, request one at https://accounts.cs.odu.edu/validate/

If you are not familiar with Unix/Linux systems, I strongly encourage you to read the materials from [CS 252 - Unix for Programmers](https://www.cs.odu.edu/~zeil/cs252/latest/Directory/outline/index.html).

If you already have a webpage setup on the cs.odu.edu server, you can skip these steps, but you will need to be able to create new webpages in that space this semester.

1. Login to the ODU-CS Linux system using ssh, Putty, or an appropriate ssh client. The host name is linux.cs.odu.edu and the port number is 22.

2. Your website will reside in the directory named `secure_html`, which should be found in the home directory. Set the group ownership and access permission for your website, so that the web server can access its contents:

```
chgrp -R http ~/secure_html
chmod -R 770 ~/secure_html
```

The -R flag on each command will apply the command to all contents of the directory, i.e., your entire website. 

This command should be repeated for each new directory and file that you add to your website. It can be applied recursively at the top level, as shown above, or it can be applied individually to each new item in the website.

3. Create a directory named `cs725` or `cs825`(note the lower-case spelling) under the `secure_html` directory. Assign the group and access permissions as described above. 

4. Create an initial home page in your class folder (named `index.html`) using the following content (replace MYNAME with your name):

```{html}
<!DOCTYPE html>
<html xmlns="https://www.w3.org/1999/xhtml" lang="en">
<head>
<title>My CS 725/825 Home Page</title>
<meta charset="UTF-8"/>
</head>
<body>
<h3>Welcome to MYNAME's CS 725/825 home page!</h3>
</body>
</html>
```

Make sure to set the appropriate read permissions on the file (see step 2).  Then, this webpage should be accessible at https://www.cs.odu.edu/~username/cs725/ - where you replace "username" with your ODU-CS username and replace cs725 with cs825 if that's what you named your folder.

## Git, GitHub 

Git is a version control system for tracking changes in source code, used in the popular [GitHub](https://github.com) code hosting platform.  To become familiar with the basics of Git, read [git - the simple guide](https://rogerdudler.github.io/git-guide/).

If you do not have one already, you must create a GitHub account.  I recommend a username that incorporates at least part of your actual name (e.g., mine is [weiglemc](https://github.com/weiglemc)).  If you already have a GitHub account, you do *not* need to create a new one for this class.

Mr. Thomas Kennedy has a nice introduction and walkthrough of Git available.  Read through [his materials](https://git-community.cs.odu.edu/tkennedy/git-workshop/-/wikis/Git-Workshop) and work through all of the exercises in the "Setting Up a Local Git Repository" section to create a repository, make changes, commit them locally, and then create a remote repo at GitHub. 

Notes about the "Adding a Remote" section:
* You will be using GitHub (not GitLab)
* Mr. Kennedy's example output is based on using GitLab and git-community.cs.odu.edu.  You are not using that system.

**Q1.** What is your GitHub username?

**Q2.** What is the URL of your remote GitHub repo (created through Mr. Kennedy's exercises)?

## Markdown

Markdown is a lightweight markup language that is widely used in GitHub, especially for README pages.  

Here are some helpful links for Markdown (and GitHub-flavored Markdown):
* [Markdown Basic Syntax](https://www.markdownguide.org/basic-syntax)
* [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
* [Markdown on GitHub](https://help.github.com/en/categories/writing-on-github) -- it can be slightly different than regular Markdown
  * [Mastering Markdown](https://guides.github.com/features/mastering-markdown/) (GitHub flavor)

**Q3.** Complete the following tasks:
* a) Create a bulleted list with at least 3 items
* b) Write a sentence or paragraph that demonstrates the use of *italics*, **bold**, ***bold italics***, and `inline code`.
* c) Create an example of a fenced code block.
* d) Create a level 4 heading
* e) Create a line that includes a link to a website (your choice)

## LaTeX and Overleaf

LaTeX is *the* markup language for academic publication. [Overleaf](https://overleaf.com) provides an online setup for writing and compiling LaTeX into PDF.  

Sign up for a free [Overleaf](https://overleaf.com) account.

Walk through [part 1](https://www.overleaf.com/learn/latex/Free_online_introduction_to_LaTeX_(part_1)) and [part 2](https://www.overleaf.com/learn/latex/Free_online_introduction_to_LaTeX_(part_2)) of this [LaTeX introduction](https://www.overleaf.com/learn/latex/Free_online_introduction_to_LaTeX_(part_1)). 

**Q4.** What environment is used for bulleted lists?  What command is used to start a bulleted list?

**Q5.** What is the command to include an image in a LaTeX file?

## Observable and Vega-Lite

[Observable](https://observablehq.com) is a notebook platform that is based on JavaScript. It's similar to other notebooks, but [R Notebooks](https://bookdown.org/yihui/rmarkdown/notebook.html) are based on R and [Jupyter Notebooks](https://jupyter.org) were originally based on Python.  [Vega-Lite](http://vega.github.io/vega-lite/) is a high-level language for building interactive visualizations on the web. It is based on [D3](https://d3js.org).  Because it is JavaScript-based, Vega-Lite can be embedded in Observable notebooks.

Observable can be tied to your GitHub account, so to get started, make sure that you're logged into GitHub.

Open the [A Taste of Observable](https://observablehq.com/@observablehq/a-taste-of-observable) notebook and work through the examples and questions that it asks. 

**Q6**. In the "New York City weather forecast" section, try replacing `Forecast: detailedForecast` with `Forecast: shortForecast`. Then press the blue play button  or use Shift-Return to run your change. What happens?

**Q7**. Under the scatterplot of temperature vs. name, try replacing `markCircle()` with `markSquare()`. Then press the blue play button  or use Shift-Return to run your change. What happens? How about `markPoint()`?

**Q8**. Under "Pick a location, see the weather forecast", pick a location on the map.  Where was the point you picked near?  (Be a little patient with the updates.)

Read through the [Introduction to Data](https://observablehq.com/@observablehq/introduction-to-data) notebook. There are no exercises to work, but this will be useful material for you going forward.

## The Missing Semester of Your CS Education

From: https://missing.csail.mit.edu/about/
> Over the years, we have helped teach several classes at MIT, and over and over we have seen that many students have limited knowledge of the tools available to them. ... These topics are not taught as part of the university curriculum: students are never shown how to use these tools, or at least not how to use them efficiently, and thus waste time and effort on tasks that *should* be simple. The standard CS curriculum is missing critical topics about the computing ecosystem that could make students’ lives significantly easier.  

MIT has provided an excellent resource, [The Missing Semester of Your CS Education](https://missing.csail.mit.edu/), for learning about the command-line, version control (like Git), and many other essential Unix-based tools that probably haven't been covered in your formal coursework.  This is organized as a course, with video lectures, webpages of notes and examples, and suggested exercises.  All of it is freely available.  If you don't have much Unix experience, this is *highly recommended*.  In particular, I recommend the following modules:
* Course overview + the shell
* Shell Tools and Scripting
* Editors (Vim)
* Data Wrangling 
* Version Control (Git)
