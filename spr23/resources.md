# References and Additional Resources

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
* Learn by example: Use Google to search for examples specifically in Observable, "vega-lite scatterplot site:observablehq.com"

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
