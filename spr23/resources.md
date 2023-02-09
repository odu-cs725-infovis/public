# References and Additional Resources

[Jump to this week](#week-5)

## Week 1

[CS 725/825 project highlights (2021-2022)](https://ws-dl.blogspot.com/2022/12/2022-12-02-visualization-class-projects.html)

### Data Vis Overview

* Tamara Munzner's half-day [IEEE VIS 2020 Visualization Analysis & Design Tutorial](https://www.youtube.com/playlist?reload=9&list=PLT4XLHmqHJBffudbh19w_duD7mprvNf4Q)
* Jeffrey Heer, Michael Bostock, and Vadim Ogievetsky, ["A Tour Through the Visualization Zoo"](https://queue.acm.org/detail.cfm?id=1805128%20), *ACM Queue*, Vol. 8, No. 5, May 2010
* [eagereyesTV](https://www.youtube.com/c/eagereyes/videos) - visualization videos from Robert Kosara
* Visualization Idioms
  * Improper use of line charts - <http://callingbullshit.org/case_studies/case_study_musician_mortality.html>
  * [Understanding Pie Charts](https://eagereyes.org/techniques/pie-charts), Robert Kosara, eagereyes.org
  * Stacked Bar charts - <http://www.storytellingwithdata.com/blog/2017/11/22/use-cases-for-stacked-bars>
  * [Histogram Design Decisions](https://policyviz.com/2018/11/27/histogram-design-decisions/), policyviz.com
  * [Why We Love the CDF and Do Not Like Histograms That Much](http://www.andata.at/en/software-blog-reader/why-we-love-the-cdf-and-do-not-like-histograms-that-much.html), Andreas Kuhn, ANDATA Software Blog
  * [Hexagonal Binning – a new method of visualization for data analysis](https://www.meccanismocomplesso.org/en/hexagonal-binning-a-new-method-of-visualization-for-data-analysis/) - nice explanation of why hexagons
* [Dataviz Cheatsheet](https://policyviz.com/2018/08/07/dataviz-cheatsheet/), from policyviz.com
* [my guiding principles](http://www.storytellingwithdata.com/blog/2017/8/9/my-guiding-principles), storytellingwithdata.com -- set of basic principles for vis design
* [How to define a map’s bins to visualize your data](https://policyviz.com/2018/02/08/how-to-define-a-maps-bins-to-visualize-your-data/), Policy Viz

### Data Sources

* [list of public datasets from CS 625-F21, HW6](https://github.com/odu-cs625-datavis/public/blob/main/fall21/HW6.md#data-sources)
* [Data Is Plural archive](https://www.data-is-plural.com/archive/) - weekly newsletter of useful/curious datasets
* [Our World in Data GitHub](https://github.com/owid), [datasets](https://github.com/owid/owid-datasets/tree/master/datasets)
* [US Census Bureau data](https://data.census.gov)
  * articles with tools and tips on using US Census Bureau data, https://www.ncdemography.org/category/story-recipe/
  * R package, https://walker-data.com/tidycensus/
  * Python package, https://pypi.org/project/census/


### Interesting Visualizations

* dots - <https://www.npr.org/2022/06/30/1107868327/trump-election-fraud-jan-6>
* spiral chart - <https://twitter.com/abmakulec/status/1479496579040034822>
* connected scatterplot - <https://twitter.com/visualisingdata/status/1476518279187415045>
* Marey Diagram and others in analysis of Boston subway system - <http://mbtaviz.github.io/>, [commentary by Kaiser Fung](https://junkcharts.typepad.com/junk_charts/2014/06/a-great-visual-of-complicated-schedules.html)

## Week 2

### Visual Analytics

### Observable

* [Getting Started](https://observablehq.com/@observablehq/getting-started)
* [Keyboard Shortcuts](https://observablehq.com/@observablehq/keyboard-shortcuts)
* [A Minimal Introduction to JavaScript and Observable](https://observablehq.com/@uwdata/a-minimal-introduction-to-javascript-and-observable)
* [Observable/GitHub flavored Markdown summary](https://observablehq.com/@ajlimbert/github-flavored-markdown-cheatsheet-observable)
* [Introduction to Data](https://observablehq.com/@observablehq/introduction-to-data)
* [Minimap](https://observablehq.com/@observablehq/minimap)

### Vega-Lite API style

* [Vega-Lite API Reference](https://vega.github.io/vega-lite-api/api/)
* [Observable for Vega-Lite](https://observablehq.com/collection/@observablehq/observable-for-vega-lite) - collection of intro notebooks
  * [Charting with Vega-Lite](https://observablehq.com/@observablehq/vega-lite?collection=@observablehq/observable-for-vega-lite)
  * [Vega-Lite Chart Types](https://observablehq.com/@observablehq/vega-lite-chart-types?collection=@observablehq/observable-for-vega-lite)
  * [Layers and Facets and Concat, Oh My!](https://observablehq.com/@observablehq/layers-facets-concat?collection=@observablehq/observable-for-vega-lite)
* [UW's Data Visualization Curriculum](https://observablehq.com/@uwdata/data-visualization-curriculum) - collection of more detailed notebooks
  * *won't be directly covered in class, but here for your reference*
  * including [Introduction to Vega-Lite](https://observablehq.com/@uwdata/introduction-to-vega-lite), [Data Types, Graphical Marks, and Visual Encoding Channels](https://observablehq.com/@uwdata/data-types-graphical-marks-and-visual-encoding-channels), [Data Transformation](https://observablehq.com/@uwdata/data-transformation), [Scales, Axes, and Legends](https://observablehq.com/@uwdata/scales-axes-and-legends), [Multi-View Composition](https://observablehq.com/@uwdata/multi-view-composition), [Interaction](https://observablehq.com/@uwdata/interaction)
* [Vega-Lite API v4](https://observablehq.com/@vega/vega-lite-api) vs. [Vega-Lite API v5](https://observablehq.com/@vega/vega-lite-api-v5)
* [CS 625 Observable Collection](https://observablehq.com/collection/@weiglemc/cs625)
* Learn by example -- use Google to search for examples specifically in Observable, ex: "scatterplot vega-lite site:observablehq.com"

### Vega-Lite JSON-style

* [Vega-Lite Reference](https://vega.github.io/vega-lite) (JSON-based)
* [Vega Embed](https://github.com/vega/vega-embed)
* [Hello Vega-Embed](https://observablehq.com/@vega/hello-vega-embed)
* [Working with Vega-Lite](https://observablehq.com/@didoesdigital/working-with-vega-lite)
* [Vega-Lite API vs. JSON Examples](https://observablehq.com/@weiglemc/vega-lite-api-vs-json-examples)

### Arquero - dplyr-like data manipulation in JavaScript

* [Arquero](https://github.com/uwdata/arquero/blob/master/README.md)
* [Introducing Arquero](https://observablehq.com/@uwdata/introducing-arquero)
* [Arquero API Reference](https://uwdata.github.io/arquero/api/)
* [Arquero Notebook Collection](https://observablehq.com/collection/@uwdata/arquero)

## Week 3

### IEEE VIS

* IEEE VIS YouTube channel, <https://www.youtube.com/@IEEEVisualizationConference/featured>
* IEEE VIS main website, <https://www.ieee-vis.org>
* IEEE Xplore - <https://ieeexplore-ieee-org.proxy.lib.odu.edu/Xplore/home.jsp>
* [IEEE VisWeek Papers on the Web](http://www.cad.zju.edu.cn/home/vagblog/vispapers.html)
* [IEEE Transactions on Visualization and Computer Graphics (TVCG)](https://www.computer.org/csdl/journal/tg)
  * [TVCG @ IEEE Xplore](https://ieeexplore-ieee-org.proxy.lib.odu.edu/xpl/RecentIssue.jsp?punumber=29456754)
* [Vispubdata](https://sites.google.com/site/vispubdata/home)
* [IEEE Anthology Vis](https://visav.vizhub.ai/)

### Reading Academic Papers

* [My Research Methods Guidelines](https://docs.google.com/document/d/1ZIlCog36OoNKymgWZkJ5D8142JQ19WGjbaqW34ymd_8/edit)
* Example of off-campus access to ACM Digital Library, <https://dl-acm-org.proxy.lib.odu.edu/doi/abs/10.5555/1218112.1218509>
* Example of off-campus access to IEEE Xplore, <https://ieeexplore-ieee-org.proxy.lib.odu.edu/document/6970187>
* Fatcat, <https://fatcat.wiki/>
  * My papers: <https://fatcat.wiki/release/search?q=michele+c.+weigle>
  * Example search for a particular paper, <https://fatcat.wiki/release/search?q=Automatically+Selecting+Striking+Images+for+Social+Cards>
  * Example search for a particular conference venue, <https://fatcat.wiki/container/search?q=Joint+conference+on+digital+libraries>
  * JCDL page, <https://fatcat.wiki/container/kw2apmx5ynfyjf6jhs5gzrrx6e>
  * IEEE Transactions on Visualization and Computer Graphics page, <https://fatcat.wiki/container/hjrujdrg7zaghbdsp5pdzq7cmm>
* Internet Archive Scholar, <https://scholar.archive.org/>
  * My papers: <https://scholar.archive.org/search?q=michele+c.+weigle>
  * Example search for a particular paper, <https://scholar.archive.org/search?q=automatically+selecting+striking+images+for+social+cards>
* S. Keshav, [How to Read a Paper](http://blizzard.cs.uwaterloo.ca/keshav/home/Papers/data/07/paper-reading.pdf)
* [Reading Papers](https://www.cs.odu.edu/~jbrunelle/cs891/lectures/03_reading_papers.pdf) (pdf), lecture slides from Dr. Brunelle's CS 891, Spring 2019
* William Griswold, [How to Read an Engineering Research Paper](http://www.cs.ucsd.edu/users/wgg/CSE210/howtoread.html)
* [Example of marking up a paper](https://drive.google.com/open?id=1UQeT9o-IvLhp5RAv1vAJ7DS-lXQdNW7E)
* Jason Eisner, [How to Read a Technical Paper](http://www.cs.jhu.edu/~jason/advice/how-to-read-a-paper.html)
* Michael Mitzenmacher, [How to Read a Research Paper](http://www.eecs.harvard.edu/~michaelm/postscripts/ReadPaper.pdf)
* Tia Newhall, [Some Tips for Reading Research Papers](http://www.cs.swarthmore.edu/~newhall/cs97/s00/ReadingAdvice.html)

### D3 Data

* NYU Visualization [Guides and Examples Collection](https://observablehq.com/collection/@nyuvis/guides-and-examples)
* JavaScript
  * [Docs @Mozilla Dev Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
  * [Docs @W3Schools](https://www.w3schools.com/jsref/jsref_reference.asp)
  * NYU Vis [JavaScript Basics](https://observablehq.com/@nyuvis/javascript-basics?collection=@nyuvis/guides-and-examples)
* NYU Vis [Data Transformation](https://observablehq.com/@nyuvis/data-transformation)
* NYU Vis [SVG and D3 Basics](https://observablehq.com/@nyuvis/d3-introduction?collection=@nyuvis/guides-and-examples)

## Week 4

### Giving Presentations

* Ashwin Ram, [Presenting a Paper](https://www.cc.gatech.edu/faculty/ashwin/wisdom/how-to-present-a-paper.html) - focuses on presenting others' work
* Jiri Srba, [How to Read and Present a Scientific Paper](https://homes.cs.aau.dk/~srba/courses/FS-07/slides-talk.pdf)
* Nicholas Nethercote, [Giving a Good Research Talk](https://web.archive.org/web/20200220135851/http://njn.valgrind.org/good-talk.html)
* Justin Brunelle, [Presenting Academic Research slides](https://drive.google.com/file/d/1UYJehNbfIYRvcFm5ve5Bx7l0IKZipRWp/view?usp=share_link), from CS 891, Fall 2019
* Tamara Munzner, <http://www.cs.ubc.ca/~tmm/policy.txt>
* Jones et al., [How to Give a Good Research Talk](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/08/giving-a-talk.pdf)
* Arnaud Legout, [How To Give a Talk](http://cel.archives-ouvertes.fr/cel-00529505/en/) - comprehensive set of guidelines, includes advice on slide design
* Jean-luc Doumont, [Creating Effective Slides](https://www.youtube.com/watch?v=meBXuTIPJQk), talk April 4, 2013 at Clark Center, Stanford Univeristy, video (1:03:03)
* English Communication for Scientists, [Giving Oral Presentations](https://www.nature.com/scitable/ebooks/english-communication-for-scientists-14053993/giving-oral-presentations-14239332) (includes delivering as a non-native speaker)

### D3 Vis Intro

* [Video playlist for W209 Data Visualization at UC Berkeley's Masters in Data Science (MIDS) Program](https://www.youtube.com/playlist?list=PLmRfPZr9-VoGodduNBkPKoNNXeOBMmQGz) - includes web development basics, ObservableHQ, Intro to D3 with Observable, Intro to Vega-Lite with Observable, and more!
* [CS725-S23 D3 Vis Intro](https://observablehq.com/@weiglemc/cs725-s23-d3-vis-intro)
  * [NYU Visualization Guides and Examples Collection](https://observablehq.com/collection/@nyuvis/guides-and-examples)
  * [NYU Vis D3 Introduction](https://observablehq.com/@nyuvis/d3-introduction?collection=@nyuvis/guides-and-examples)
  * [SVG Translate Example slides](https://docs.google.com/presentation/d/1TKFcgmPKvybFX22-XDJ8f3Hn_0IVbmo5rt045GX34jE/preview)
  * [NYU Vis Bar Chart Walk-through](https://observablehq.com/@nyuvis/bar-chart-walk-through?collection=@nyuvis/guides-and-examples)
  * [D3 Vis Intro - supplemental slides](https://docs.google.com/presentation/d/1r_hh5f0sdSrxXYb-UJGSu-OlG1U65H32pAgraMVDVg0/preview)
* [Learn D3 Collection](https://observablehq.com/collection/@d3/learn-d3)
  * [Learn D3: By Example](https://observablehq.com/@d3/learn-d3-by-example?collection=@d3/learn-d3)
* [D3 Documentation Collection](https://observablehq.com/collection/@d3/documentation)
* [D3 Gallery](https://observablehq.com/@d3/gallery)
* [D3 API Reference](https://github.com/d3/d3/blob/main/API.md)

## Week 5

### Clustering

* Segaran, [*Programming Collective Intelligence*](https://go.oreilly.com/old-dominion-university/library/view/programming-collective-intelligence/9780596529321/) - textbook used in CS 432/532, includes lots of Python code examples
* [Flat and Hierarchical Clustering | The Dendrogram Explained video](https://www.youtube.com/watch?v=ijUMKMC4f9I)
* K-Means
  * [K-means Clustering Python Example](https://towardsdatascience.com/machine-learning-algorithms-part-9-k-means-example-in-python-f2ad05ed5203)
  * [Visualizing K-Means Algorithm](http://tech.nitoyon.com/en/blog/2013/11/07/k-means/)
  * [K-Means Walkthrough in Observable](https://observablehq.com/@andreaskdk/k-means)
  * [kmeans() in Observable](https://observablehq.com/@spond/k-means-clustering-algorithm)
  * [K Means Clustering: Pros and Cons of K Means Clustering video](https://www.youtube.com/watch?v=YIGtalP1mv0) - watch up to time 4:44

### D3 Vis

* [CS 725/825, S23 Observable Collection](https://observablehq.com/collection/@weiglemc/cs-725-825-spring-2023) - public notebooks for this semester
* [D3 Lessons](http://lessons.vaclab.unc.edu/), UNC INLS 641 Visual Analytics, David Gotz
* [NYU Vis Bar Chart Walkthrough](https://observablehq.com/@nyuvis/bar-chart-walk-through)
* [NYU Vis SVG and D3 Basics Practice](https://observablehq.com/@nyuvis/svg-and-d3-basics-practice-solutions) - scatterplot
* [NYU Vis Lines and Maps](https://observablehq.com/@nyuvis/lines-and-maps) - line and area charts
* [NYT Vis Graphical Encoding Examples](https://observablehq.com/@nyuvis/graphical-encoding-examples) - layered line charts, small multiple area charts
* [Arquero and D3](https://observablehq.com/@uwdata/arquero-and-d3?collection=@uwdata/arquero)
* [Multi-line chart data preparation in Arquero](https://observablehq.com/@uwdata/multi-line-chart-data-preparation)
* [Multi-line chart D3 template](https://observablehq.com/@d3/multi-line-chart)
