# Python workshop @ Dataviz HKB/BFH

> Das Modul Datenerhebung, -aufbereitung, -analyse soll die Lücke zwischen Rohdaten und visualisierbaren Daten schliessen. Den Schwerpunkt des Moduls bildet eine Einführung in die deskriptive Statistik. Ein kurzer Exkurs in die Methoden der Datenerhebung rundet das Modul ab. Teil des Moduls sind Hands-on-Sessions, in denen die Teilnehmenden den Umgang mit modernen Tools üben, um Daten einlesen, aufbereiten, vorbereiten und einfache Statistiken erstellen zu können.

The following are notes in English from this workshop at the [Bern University of the Arts](https://www.hkb.bfh.ch/en/) on 14 April 2018.

> The data collection, preparation and analysis module intends to close the gap between raw data and visualisable data. The module focuses on an introduction to descriptive statistics. A short excursion into the methods of data collection rounds off the module. Part of the module are hands-on sessions in which the participants practice the use of modern tools in order to read in, process, prepare and create simple statistics.

## 0. Setup

We recommend installing [Anaconda](https://www.anaconda.com/download/) if you have a modern laptop with at least 4 GB, ideally 8+ GB RAM. It comes with [Anaconda Navigator](https://docs.anaconda.com/anaconda/navigator/), which along with the `conda` command line tool makes installing Python packages for data science easier. Alternatively, students were encouraged to install a [modern browser](https://browsehappy.com/) and login with a (free) Microsoft account to [Azure ML Studio](https://studio.azureml.net/).

In the workshop, we mostly used Anaconda and [Binder (beta)](https://mybinder.org/) - which provides free, time-limited access to live Jupyter notebooks in the cloud, to work on code exercises. You can use the notebook in this repository to get started, by putting the full link to this repository, i.e.

`https://github.com/schoolofdata-ch/hkb-dataviz`

and clicking the **launch** button. Note that your changes *will not be saved*, so you need to **Download** your notebook from the menu if you want to keep any of your work.

## 1. Sources

After an introduction to each other and our learning interests using the School of Data "Advanced Data & Dragons" worksheets, we had a discussion about the various tools and programming languages involved in working with data, and what kind of things are worth paying attention to when setting out to learn a new tool.

[![Cisco global IP traffic growth](https://httpscisco-a.akamaihd.net/1384193102001/1384193102001_3593023850001_vs-53862492e4b0066273553e90-1592194027001.jpg?pubId=1918791313001&videoId=3593058341001)](https://video.cisco.com/detail/videos/visual-networking-index/video/3593058341001/global-ip-traffic-growth)

*Image: [Cisco](https://video.cisco.com/detail/videos/visual-networking-index/video/3593058341001/global-ip-traffic-growth)*

Keeping in mind the pervasiveness and explosion of usage and interest in data, we discussed concepts like open data and big data, open source and enterprise software, levels of abstraction, and our shared goals in combining analytical techniques for communicating with evocative design and data visualization.

Two "mindsets" when dealing with data challenges were presented:

1. A *Philosopher's Stone* approach, if not searching for "the essential secret of the universe", then at least attempting to use [epistemic](https://en.wikipedia.org/wiki/Epistemology) approaches, which prioritize aggregating sources of information in structures that allow interoperability and wide-reaching access as [Linked Open Data](https://en.wikipedia.org/wiki/Linked_data#Linking_Open_Data_community_project).
2. A *Stone in a River* mindset in which data is considered a part of the natural order of "impermanence and change", where a sampling of data has a different result from day to day, and in fact changes the data itself as per the [Observer effect](https://en.wikipedia.org/wiki/Observer_effect_(physics)) from quantum physics. In this mindset access to streaming data sources like the [Twitter firehose](https://www.forbes.com/sites/benkepes/2015/04/11/how-to-kill-your-ecosystem-twitter-pulls-an-evil-move-with-its-firehose/) are of primary interest.

These points were followed with an overview of the Swiss [Open Government Data program](https://opendata.swiss/en/terms-of-use/), a look at featured [applications](https://opendata.swiss/en/app/) and several open datasets on the portal:

- [Consultations by gender, age and nationality](https://opendata.swiss/en/dataset/beratungsfalle-nach-geschlecht-alter-und-nationalitat)
- [Data inventory of the Federal Administration Data](https://opendata.swiss/en/dataset/data-inventory-of-the-federal-administrationdata)
- [Results of the opendata.admin.ch survey](https://opendata.swiss/en/dataset/results-of-the-opendata-admin-ch-survey)

## 2. Introduction

Our introduction to data wrangling for visualization began with [OpenRefine](http://toolbox.schoolofdata.ch/clean/analyse/2017/08/02/OpenRefine.html), an open source, web-based tool for tabular data widely used in the Data Journalism community. We loaded in some data and looked at how it helps to convert, explore and correct datasets, while crucially keeping track of the history of changes. Experiences were shared from real life projects like [Pharmagelder](https://www.beobachter.ch/gesundheit/pharmagelder-der-doktor-und-sein-sponsor).

[![](https://datalets.ch/projects/openrefine.jpg)](http://toolbox.schoolofdata.ch/clean/analyse/2017/08/02/OpenRefine.html)

We then covered the steps in the [School of Data Pipeline](http://toolbox.schoolofdata.ch/overview.html) as a generalised method of data wrangling which emphasizes goal-setting, validation/source-checking and careful cleaning of datasets. Some of the advice shared for finding good data to visualize included:

1. Start with a good **question**. Think about how [Wolfram Alpha](http://www.wolframalpha.com/) and [Google search](https://developers.google.com/search/docs/guides/intro-structured-data) use *Structured Data* to respond to natural language search queries with rich search results.
2. Understand why **crowdsourcing** works. Explore data from [Citizen Science](https://scistarter.com/citizenscience.html) projects like the ones in [Zooniverse](https://github.com/zooniverse/). Compare this with efforts to collect quality information from a globally distributed user base like [Wikipedia / WikiData](https://wikidata.org/), [OpenStreetMap](https://www.youtube.com/watch?v=7sC83j6vzjo) (10th anniversary video on YouTube), or [OpenCorporates](https://opencorporates.com/). Think about the **standards** that enable "crowdsensing" initiatives like [MakeZurich](http://now.makezurich.ch/).
3. Explore **Public Data**, from [Amazon](https://aws.amazon.com/public-datasets/) to [Google](https://www.google.com/publicdata/directory#!) and [Kaggle](https://www.kaggle.com/datasets), companies [around the world](http://www.opendata500.com/) use contests (hackathons), data portals and [web service interfaces](https://www.programmableweb.com/news/research-shows-interest-providing-apis-still-high/research/2018/02/23) (APIs) to share their data troves, with various strategic purposes in mind, but also to the great benefit of researchers and the curious. The [Swisscom](http://opendata.swisscom.com/) and [Swiss Post](https://swisspost.opendatasoft.com) portals were demoed.
4. Think about what affects the [**quality** of data](https://www.europeandataportal.eu/elearning/en/module5/#/id/co-01). Understand the issues surrounding [Copyright](https://creativecommons.org/about/program-areas/open-data/) and other terms of use.
5. Consider that **authenticity** is a particularly stringent question, as outlined (for example) in this 2013 [Wired article](https://www.wired.com/insights/2013/02/how-to-ensure-authenticity-in-big-data/): *"more and more business decisions are based on the analysis of external data", "big data created externally is .. more vulnerable to theft and tampering than if it were created inside the corporate firewall", "organizations must validate duplicate sets of data and be able to respond quickly to any invalid data set", "cybercrime has emerged as a very profitable business for criminals — underlining the growing need to validate and verify all kinds of data", "a solution needs to ensure that the data is indeed what it portrays itself to be, meaning that no third-party has purposefully or accidentally changed what has been agreed upon and documented."*

## 3. Wrangling

Most of the workshop morning was spent explaining the particularities of and setting up [Python](https://www.python.org/about/), [Pandas](http://pandas.pydata.org/) and [Jupyter](http://jupyter.readthedocs.io/en/latest/install.html) on the various laptops. While more experienced Python users in the room started reading in datasets, we had a mini-intro to Python programming, covering basic types and operations, lists, dictionaries, flow control, and loading modules.

Quick dives into [Python environments](http://docs.python-guide.org/en/latest/dev/virtualenvs/#lower-level-virtualenv) and [version control](https://guides.github.com/) (GitHub) were made along the way. However, our focus was on descriptive statistics, which were possible in a a couple of lines of code using Pandas `read_csv` and the DataFrame's `describe()` functions.

Our initial sample is available in this repository, towards the top of [klasse.ipynb](klasse.ipynb)

[![Python book cover](https://www.oreilly.de/common/images/cover_masterid/800/12361.jpg)](http://shop.oreilly.com/product/0636920023784.do)

This roughly followed the excellent [SciPy introductory lectures](http://www.scipy-lectures.org/intro/language/python_language.html), which are recommended along with courses from [Software Carpentry](https://software-carpentry.org/lessons/) and a new one by [Luke Thompson](https://github.com/cuttlefishh/python-for-data-analysis), as well as the O'Reilly classic [Python for Data Analysis](http://shop.oreilly.com/product/0636920023784.do) text.

After a lunch break, we talked about [Frictionless Data](https://frictionlessdata.io/field-guide/), a standardization initiative that aims to improve the way public and open data is distributed, published and made more accessible. Drilling into a few [Core datasets](https://datahub.io/core) on Datahub.io, such as [Pharmaceutical Drug Spending by Country](https://datahub.io/core/pharmaceutical-drug-spending), it was suggested that the more experienced Python users in the class try [Datapackage-py](https://github.com/frictionlessdata/datapackage-py) to load in some data by schema-first.

With a quick recap of the importance of [Data structures](https://docs.python.org/3.6/tutorial/datastructures.html), we focused on wrangling and visualizing data. Our focus switched from console coding to using Jupyter and JupyterLab. The history of digital notebooks for scientific computing was quickly covered, from [MATLAB](https://en.wikipedia.org/wiki/MATLAB) and [Mathematica](https://www.wolfram.com/mathematica/), to iPython and [R Notebooks](https://rmarkdown.rstudio.com/r_notebooks.html) today.

> "A loose acronym meaning Julia, Python, and R. These programming languages were the first target languages of the Jupyter application, but nowadays, the notebook technology also supports many other languages." ([Angus docs](https://angus.readthedocs.io/en/2017/Jupyter-Notebook-Notes.html))

There was lots to ground to cover, from Jupyter kernels to the 135'303 [PiPy packages](https://pypi.python.org/pypi) on offer. Questions were asked about alternative IDE's, so in discussion we mentioned [Apache Zeppelin](https://zeppelin.apache.org/), [Yhat Rodeo](http://rodeo.yhat.com/), [PyCharm](https://www.jetbrains.com/pycharm/) and [Atom/Hydrogen](https://atom.io/packages/hydrogen) - all great interfaces for working on data projects. By the way, check out Markus Schanta's [Awesome Jupyter](https://github.com/markusschanta/awesome-jupyter) list for lots of links to related tools and tutorials.

## 4. Exploration

While several participants were already using Pandas [plotting functions](https://pandas.pydata.org/pandas-docs/stable/visualization.html) and [Matplotlib](https://de.wikipedia.org/wiki/Matplotlib) to render their data [beautifully](http://www.randalolson.com/2014/06/28/how-to-make-beautiful-data-visualizations-in-python-with-matplotlib/), we discussed some reasons behind the large variety of frameworks and libraries for data visualization in Python.

The *Grammar of Graphics*, a dataviz concept [spanning languages](https://ramnathv.github.io/pycon2014-r/visualize/ggplot2.html), was something that we tried to understand in the course. Read the excellent introduction by [Liz Sander](https://codewords.recurse.com/issues/six/telling-stories-with-data-using-the-grammar-of-graphics) (recurse.com) or explore [Python Graph Gallery](https://python-graph-gallery.com) to get an appreciation for how a standard set of plots can be combined to make data speak concisely, correctly and in a way that allows for aesthetically pleasing and flexible designs. Or read the 2010 paper by [Hadley Wickham](http://byrneslab.net/classes/biol607/readings/wickham_layered-grammar.pdf) for a more systematic perspective.

While Matplotlib, [Seaborn](https://seaborn.pydata.org/index.html), [Bokeh](https://bokeh.pydata.org/en/latest/), and [others](https://dsaber.com/2016/10/02/a-dramatic-tour-through-pythons-data-visualization-landscape-including-ggplot-and-altair/) offer sensible and versatile approaches to the problem of graphing data, we considered the way [D3.js](https://d3js.org/), particularly through the efforts of [Mike Bostock](https://bl.ocks.org/mbostock), has led to a supportive community and a rich palette of reusable open source data visualizations, that were nevertheless hard for beginners to code read and extend.

[![Altair chart](https://altair-viz.github.io/_static/candlestick_chart.png)](https://altair-viz.github.io/)

Implementing the theories of the Grammar of Graphics, the `JSON` based [Vega](https://vega.github.io) project, well described by [Paul van der Laken](https://paulvanderlaken.com/2017/11/01/vega-the-grammar-of-interactive-graphics/), and today extended into [Vega Lite](https://vega.github.io/vega-lite/), has found its way into the Python world through the [Altair](https://altair-viz.github.io/) package.

> Altair is a Python API based on Vega-Lite, and is useful for rapidly creating statistical graphics visualizations more comparable to hand-coded designs built with D3 or Processing.

We were convinced by the outstanding documentation and examples, and tried to install Altair on our machines, however this led to general dismay as errors or other technical difficulties prevented it from working for many of the participants, mostly through a confusing process of integrating with Jupyter that the final 2.0 release will hopefully soon [resolve](https://github.com/altair-viz/altair/issues/751).

The example notebook we worked through is available in this repository, in the second half of [klasse.ipynb](klasse.ipynb)

In the workshop we only briefly skimmed the subject of [Scikit-Learn](http://scikit-learn.org/), the biggest compendium of data science recipes, caught small glimpses of cool tools like [Datashader](http://datashader.org/)/[Holoviews](http://holoviews.org/) or [Plotly for Python](https://plot.ly/python/), and hopefully despite the torrent of information the participants gained some insight into the thought and effort that goes on to publish and support good data sources, as well as opening the door to using Python and it's huge toolboxes/sandboxes of packages for data exploration and visualization.

Fernando Arturo Torres defined interactivity as, *"a particular medium's ability to facilitate the properties necessary in an ideal conversation"*, and so my own main takeaway from the workshop is the effect of **Creative limitation** on our work as visualizers and communicators of information.

[![](https://thumbs.gfycat.com/ImprobableFemaleBasenji-size_restricted.gif)](https://gfycat.com/ImprobableFemaleBasenji)

While choosing the best tool for the job is important, we need to settle on something and learn it deeply (no pun intended), until we find ourselves at ease, in the flow, exploring data in a natural and relaxed way. Something that everyone, including our course participants, will hopefully come to experience on their own terms.

Thanks to HKB/BFH, and especially to [Oliver Hümbelin](https://sites.google.com/view/oliverhuembelin/home) and [Fabienne Kilchör](http://emphase.ch/) for making this workshop possible.

## 5. Post partum

Here are some fun activities to try and Jupyter notebooks to go explore next:

- [Analyzing browser history using Python](https://applecrazy.github.io/blog/posts/analyzing-browser-hist-using-python/)
- [A gallery of interesting Jupyter notebooks](https://github.com/jupyter/jupyter/wiki/A-gallery-of-interesting-Jupyter-Notebooks)
- [Tales of Data Science](https://github.com/martinapugliese/tales-science-data)
- [Altair example notebooks](https://github.com/altair-viz/altair_notebooks)
- [Fluent Python tutorial](https://github.com/ducminhkhoi/fluent-python-tutorial)
- [The Python cookbook](https://github.com/Phil9l/python-cookbook.git)
- [Python Data Science handbook](https://github.com/jakevdp/PythonDataScienceHandbook)
- [Python for Probability, Statistics, and Machine Learning](https://github.com/unpingco/Python-for-Probability-Statistics-and-Machine-Learning.git)
