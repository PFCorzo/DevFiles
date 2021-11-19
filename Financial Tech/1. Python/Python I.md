# Install, Print, Variables, Functions 
## What are todays objective? 
	1. Learn how to open a project using JupyterLab
	2. Pseudocode a task using Python comments
	3. Create, store, and retrieve data using Python variables
	4. Control program flow with conditional logic
	5. Repeat blocks of code with loops

## What is Python? 
[[Python]] Is a [[Interpreted Language]], [[Object-Oriented Programming]], [[High Level Programming Language]] with [[Dynamic Semantics]].  

It is an [[Interpreted Language]] because at run time, the python engine figures out what the code means. As opposed to a [[Compiled Language]] that at run time, is converted  into a file by a compiler and you run the code at another time. It is considered an [[Object-Oriented Programming]] because it can deal with things like [[Objects]], [[Events]],  [[Properties]], and [[Methods]]. It is a [[High Level Programming Language]] because it is not at the level of the machine, but at the level of the individual because the average human can read the code. It has [[Dynamic Semantics]] which means that some of the code written will be understood by Python dynamically and possibly fix it. 

![[Python Features.png]]
**Figure 1.0**
Due to the feauture listed in **Figure 1.0** it is a powerful data science tool because of libraries make it easy to do what wanna do with [[Data Science]] and [[Deep-Machine Learning]]

## What is JupyterLab
[[JupyterLab]] is an [[Environement]], [[IDE]], or [[Editor]] that has a useful feature called [[Jupyter Notebooks]]. Jupyter Notebooks is an [[Open-Source]] [[Web Application]] that allows you to create and share documents that contain live code, equations, vizualizations, and narrative text.
But before we got on to show you an example, follow this instruction guide on how to setup your [[Anaconda Environement]] and [[Kernel]], download JupyterLab, JupyterNotebook, and install the necessary JupyterNotebook extension [[VSCode]].

### FinTech Conda Environment Setup

#### Initial Environment Setup
At an [[Anaconda Prompt]]:

``` Bash

conda create --name FinTech python=3.8

conda activate FinTech

conda install anaconda

conda install -c conda-forge nodejs

conda install hvplot

conda install plotly

pip install pytrends

  

# Avoid "JavaScript heap out of memory" errors (Pick One)

# (Mac/OS X/Linux)

export NODE_OPTIONS=--max-old-space-size=4096

# (Windows)

set NODE_OPTIONS=--max-old-space-size=4096

  

jupyter labextension install @jupyter-widgets/jupyterlab-manager --no-build

jupyter labextension install jupyterlab-plotly --no-build

jupyter labextension install plotlywidget --no-build

jupyter lab build

  

pip install plaid-python

pip install alpaca-trade-api

pip install psycopg2

pip install sqlalchemy

conda install -c conda-forge imbalanced-learn

pip install mysql-connector-python

pip install census

conda install python-graphviz

conda install -c conda-forge pydotplus

pip install nltk

  

```

#### Create the kernel for VS Code we need
``` Bash

python -m ipykernel install --user --name FinTech --display-name "Python 3.8 (FinTech)"

```

#### Occasionally Update Anaconda
``` Command

conda update -n base -c defaults conda

```


#### Additional Libraries to Add

  

#### For Pandas Module 

  

At an Anaconda Prompt
``` Bash

conda install -c conda-forge numpy-financial

pip install yfinance

```

  



### JupyterNotebook 
When you are in a JupyterNotebook, you will be able to run multiple snippets of code and run them to check for errors with the code. 



## 


