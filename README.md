# hkb-dataviz

CAS Dataviz

- Das Modul Datenerhebung, -aufbereitung, -analyse soll die Lücke zwischen Rohdaten und visualisierbaren Daten schliessen. Den Schwerpunkt des Moduls bildet eine Einführung in die deskriptive Statistik. Ein kurzer Exkurs in die Methoden der Datenerhebung rundet das Modul ab. Teil des Moduls sind Hands-on-Sessions, in denen die Teilnehmenden den Umgang mit modernen Tools üben, um Daten einlesen, aufbereiten, vorbereiten und einfache Statistiken erstellen zu können.
  - Online
    - Azure ML Studio
      "https://studio.azureml.net/"
    - Binder (beta)
      "https://mybinder.org/"
      - 
  - Offline
    - Anaconda
      "https://www.anaconda.com/download/"
- 1. Datenquellen von Crowdsourcing bis Open Government Data
  - Hello
  - Hello, data
    - Data explosion
      "https://www.digitaltveurope.com/files/2016/06/Cisco_global_IP_TRaffic_Growth.png"
    - Philosopher's Stone
      "The essential secret of the universe"
    - Stone in a River
      "Impermanence and change"
  - School of Data self sketch
  - Scoda Pipeline
    "http://toolbox.schoolofdata.ch/overview.html"
  - Start with a question
    "http://www.wolframalpha.com/"
  - Googling for data
    "https://privacy.google.com/your-data.html"
  - Crowdsourcing
    - Citizen Science
      "https://github.com/zooniverse/WhaleFM"
    - OpenCorporates
      "https://opencorporates.com/"
    - OpenStreetMap
      "https://www.youtube.com/watch?v=7sC83j6vzjo"
    - WikiData
      "https://query.wikidata.org/"
    - Crowdsensing
      "http://now.makezurich.ch/"
  - Public data
    "https://www.google.com/publicdata/directory#!"
  - Companies
    "http://www.opendata500.com/us/"
  - Services
    "https://www.programmableweb.com/news/research-shows-interest-providing-apis-still-high/research/2018/02/23"
  - Quality
    "https://www.europeandataportal.eu/elearning/en/module5/#/id/co-01"
  - Copyright
    "https://creativecommons.org/about/program-areas/open-data/"
  - Authenticity
    "https://www.wired.com/insights/2013/02/how-to-ensure-authenticity-in-big-data/"
    - "because so much of big data is created externally it is more vulnerable to theft and tampering than if it were created inside the corporate firewall"
    - "more and more business decisions are based on the analysis of external data"
    - "organizations must validate duplicate sets of data and be able to respond quickly to any invalid data set"
    - "cybercrime has emerged as a very profitable business for criminals — underlining the growing need to validate and verify all kinds of data"
    - "A solution needs to ensure that the data is indeed what it portrays itself to be, meaning that no third-party has purposefully or accidentally changed what has been agreed upon and documented."
    - "When data is hosted onsite, the process of data authenticity can certainly be a major challenge. However, when data is not hosted within the traditional internal IT datacenter, organizations face intense pressure to ensure that data authenticity is rock-solid."
  - Government
    "https://opendata.swiss/en/terms-of-use/"
  - Learning
    "https://github.com/altair-viz/vega_datasets"
- 2. Einführung OpenRefine (Installation, Bedienung, Praxisbeispiele)
  - Web application
  - Data wrangling
  - Open source
  - Keeps a history
- 3. Daten einlesen/schreiben in Python («Data Packages» und mehr)
  - Why we are talking about Python and not R or Julia today
    - I.e. why programming languages matter - and why they don't
  - A super short intro to Python
    "http://www.scipy-lectures.org/intro/language/python_language.html"
    - a free software released under an open-source license: Python can be used and distributed free of charge, even for building commercial software.
    - multi-platform: Python is available for all major operating systems, Windows, Linux/Unix, MacOS X, most likely your mobile phone OS, etc.
    - an interpreted (as opposed to compiled, sometimes referred to as scripted) language. Contrary to e.g. C or Fortran, one does not compile Python code before executing it. In addition, Python can be used interactively: many Python interpreters are available, from which commands and scripts can be executed.
    - a very readable language with clear non-verbose syntax
    - a language for which a large variety of high-quality packages are available for various applications, from web frameworks to scientific computing.
    - a language very easy to interface with other languages
    - Python is an object-oriented language, with dynamic typing (the same variable can contain objects of different types during the course of a program).
    - See https://www.python.org/about/ for more information.
  - Python packages, Pip and PyPi
    "https://www.python.org/about/apps/#scientific-and-numeric"
    - Bundles of code
  - What is a Python environment?
    "http://docs.python-guide.org/en/latest/dev/virtualenvs/#lower-level-virtualenv"
    - an isolated environment for your projects
  - Why we use version control
    - Sanity...
    - Remember OpenRefine
  - Connecting to databases
    "http://docs.python-guide.org/en/latest/scenarios/db/"
  - Data structures in Python
    "https://docs.python.org/3.6/tutorial/datastructures.html"
  - Scientific computing
    "https://scipy.org/about.html"
  - Frictionless Data
    "https://frictionlessdata.io/field-guide/"
- 4. Data Wrangling mit «Pandas» und Visualisierung mit «Altair»
  - Notebooks
    - MATLAB
      "https://en.wikipedia.org/wiki/MATLAB"
    - Mathematica
      "https://www.wolfram.com/mathematica/"
    - R Notebooks
      "https://rmarkdown.rstudio.com/r_notebooks.html"
  - JupyterLab
    - Jupyter
      "https://angus.readthedocs.io/en/2017/Jupyter-Notebook-Notes.html"
      - A loose acronym meaning Julia, Python, and R. These programming languages were the first target languages of the Jupyter application, but nowadays, the notebook technology also supports many other languages.
      - Notebooks
      - Application
      - Kernel
      - Dashboard
    - JupyterLab
      - Awesome collaboration
        "https://youtu.be/dSjvK-Z3o3U?t=18m14s"
      - Lots of other awesome
        - https://atom.io/packages/hydrogen
        - https://zeppelin.apache.org/
        - http://rodeo.yhat.com/
    - More awesome
      "https://github.com/markusschanta/awesome-jupyter"
  - Pandas
    - From "panel data", a common term for multidimensional data sets encountered in statistics and econometrics.
    - Data structures in Pandas
      "https://pandas.pydata.org/pandas-docs/stable/dsintro.html"
    - Cute and fluffy
      "https://www.oreilly.de/common/images/cover_masterid/800/12361.jpg"
    - Cuttlefishh
      "https://github.com/cuttlefishh/python-for-data-analysis"
  - Altair
    - What?
      "Altair is a Python API based on Vega-Lite, and is useful for rapidly creating statistical graphics visualizations more comparable to hand-coded designs built with D3 or Processing."
    - Why not matplotlib?
      "http://www.randalolson.com/2014/06/28/how-to-make-beautiful-data-visualizations-in-python-with-matplotlib/"
    - Why not seaborn?
      "https://python-graph-gallery.com"
    - Why not D3?
      "https://d3js.org/"
    - Grammar of graphics: Vega
      "https://paulvanderlaken.com/2017/11/01/vega-the-grammar-of-interactive-graphics/"
    - Vega Lite
      "https://vega.github.io/vega-lite/"
- 5. Interaktive Data Science - «Scikit», «Bokeh», «Plot.ly» 
  - Scikit-Learn
    "conda install scikit-learn"
    - The biggest compendium of data science recipes
    - An open community
  - Bokeh
    "jupyter labextension install jupyterlab_bokeh"
    - Creating web quality interactive graphics 
    - Plurality of interfaces
    - Datashader
      "http://datashader.org/"
    - Quickstart
      "https://bokeh.pydata.org/en/latest/docs/user_guide/quickstart.html"
  - Plotly
    "https://plot.ly/python/"
    - An example data rendering provider
    - Plurality of interfaces
  - Holoviews
    "http://holoviews.org/"
  - Creative limitation
    - Fernando Arturo Torres defined interactivity as, "a particular medium's ability to facilitate the properties necessary in an ideal conversation"
    - "interactive" is the limit you place on your user's creativity
    - Choose the best tool for the job
    - Less is more
      "https://gfycat.com/ImprobableFemaleBasenji"
- Fun notebooks
  - https://applecrazy.github.io/blog/posts/analyzing-browser-hist-using-python/
  - https://github.com/jupyter/jupyter/wiki/A-gallery-of-interesting-Jupyter-Notebooks
  - http://www.scipy-lectures.org/index.html
  - Tales of Data Science
    "https://github.com/martinapugliese/tales-science-data"
