# Install, Print, Variables, Functions 
## Overview 
1. Learn how to open a project using JupyterLab
2. Pseudocode a task using Python comments
3. Create, store, and retrieve data using Python variables
4. Control program flow with conditional logic
5. Repeat blocks of code with loops

## Python 
[[Python]] Is a [[Interpreted Language]], [[Object-Oriented Programming]], [[High Level Programming Language]] with [[Dynamic Semantics]].  

It is an [[Interpreted Language]] because at run time, the python engine figures out what the code means. As opposed to a [[Compiled Language]] that at run time, is converted  into a file by a compiler and you run the code at another time. It is considered an [[Object-Oriented Programming]] because it can deal with things like [[Objects]], [[Events]],  [[Properties]], and [[Methods]]. It is a [[High Level Programming Language]] because it is not at the level of the machine, but at the level of the individual because the average human can read the code. It has [[Dynamic Semantics]] which means that some of the code written will be understood by Python dynamically and possibly fix it. 

![[Python Features.png]]
**Figure 1.0**
Due to the feauture listed in **Figure 1.0** it is a powerful data science tool because of libraries make it easy to do what wanna do with [[Data Science]] and [[Deep-Machine Learning]]

### Tools 

#### JupyterLab
[[JupyterLab]] is an [[Environement]], [[IDE]], or [[Editor]] that has a useful feature called [[Jupyter Notebooks]]. Jupyter Notebooks is an [[Open-Source]] [[Web Application]] that allows you to create and share documents that contain live code, equations, vizualizations, and narrative text.
But before we got on to show you an example, follow this instruction guide on how to setup your [[Anaconda Environement]] and [[Kernel]], download JupyterLab, JupyterNotebook, and install the necessary JupyterNotebook extension [[VSCode]].

#### Anaconda
[[Anaconda]] Individual Edition is a package manager, an environment manager, a Python/R data science distribution, and a collection of over 7,500+ open-source packages. Anaconda is platform-agnostic, so you can use it whether you are on Windows, macOS, or Linux. Anaconda is free and easy to install. 

#### Anaconda install 
[[Anaconda]] To install Anaconda on Windows visit: 
https://docs.anaconda.com/anaconda/install/windows/

To install Anaconda on Mac visit: 
https://docs.anaconda.com/anaconda/install/mac-os/

#### Initial Environment Setup #CondaEnvSetUp
With conda, you can create, export, list, remove, and update [[Environement]]s that have different versions of Python and/or packages installed in them. Switching or moving between environments is called activating the environment. You can also share an environment file.

For this course we will need the following [[Libraries]] to program our software. Follow the steps below.
At an [[Anaconda Prompt]]:

``` Bash

conda create --name FinTech python=3.8

conda activate FinTech

conda install conda 

conda install -c conda-forge nodejs

```

#### Avoid "JavaScript heap out of memory" errors (Pick One)

```
# (Mac/OS X/Linux)

export NODE_OPTIONS=--max-old-space-size=4096

# (Windows)

set NODE_OPTIONS=--max-old-space-size=4096
```

```
conda install hvplot

conda install plotly

pip install pytrends#
```

#### Download the necessary extensions for Jupyter lab to work well with [[VSCode]]
  
```
jupyter labextension install @jupyter-widgets/jupyterlab-manager --no-build

jupyter labextension install jupyterlab-plotly --no-build

jupyter labextension install plotlywidget --no-build

jupyter lab build
```

#### Install different dependencies 

```
conda install hvplot

conda install plotly

pip install pytrends#

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

#### At an [[Anaconda Prompt]] update your [[Anaconda Environement]] frequently. Make sure you  are in the [[Dev Environment]] 
``` 
conda update -n base -c defaults conda
```

#### JupyterNotebook 
When you are in a [[Jupyter Notebooks]], you will be able to run multiple snippets of [[Code]] and run them to check for errors with the code.  



##### Jupyternotebook in VSCode extension 

## Coding In Python #Python
### Print 
Every running program has a text output area called "standard out", or sometimes just "stdout". The Python print() function takes in python data such as ints and strings, and prints those values to standard out. 
You can run a program from the terminal, standard out appears right there. [](https://cs.stanford.edu/people/nick/py/python-print.html) 

#### Printing a String command 
All [[Functions]] in Python start with a module that tells it what tasks to accomplish, and are followed by a [[Data Type]]. The ```print``` function in Python [[Output]]s any type of data type. In this case, the data type will be a [[String]](**str**); which basically means text. 
All string data types must be within the paranthasees and have quotes surrounding it; either single or double quoted is fine. However, If the output you are trying to display has text containing an apostrophe('), then it must be double quoted so that the string isn't ended earlier.
Run:
```
print("InsertString") 
```
At [[Run Time]], the output will then be: 

													        Insert String
Run:															
```
print("Maribel's car was on fire")
```
At [[Run Time]], the output will then be: Maribel's car was on fire
*This will only run because it was double quoted because if you notice, between the l and s in "Maribel's", there is an apostrophe.  

### Variables 
[[Variables]] are containers for storing data [[Value]]s.

#### Creating Variables
A [[Variable]] is created the moment you first assign a value to it.
To create a variable in Python, give the variable a name(in this case it will be X) followed by an equal sign, and plug in the [[Value]] you wish to assign it. 

Variables do not need to be double quoted to print at all.

For example: 
```
x = 5 
```
Here we assigned the X to hold the value of 5; therefore, it became a variable. So if we were to ```print(x)``` then the output will be: 5. 
This is because even though we told it to print X, it hold the value of 5. 

Variables do not need to be declared with any particular type, and can even change type after they have been set. To change the variable of X that was created earlier, simply assign X to hold another value.

#### Variable Types
When you are dealing with variables in Python, there will be different [[Variable Types]] or [[Data Type]]s. They are as follows: 

Text Type: `str` or [[String]]
Numeric Types: `int` or [[Integer]], `float` or [[Floating Point Number]], `complex`
Sequence Types: `list`, `tuple`, `range`
Mapping Type: `dict`
Set Types: `set`, `frozenset`
Boolean Type: `bool`
Binary Types: `bytes`, `bytearray`, `memoryview`

To figure out what data type it is, you will use the ```print``` function, followed by open paranthesees. 
Within those paranthasees you will insert the ```type``` function. 

```
print(type)
```

But a parameter needs to be set. This can be accomplished by giving the type functions its own set of paranthasees; and within it's paranthasees, a variable, that the ```type``` function can act upon, must be inserted. 

```
print(type(InsertVariable))
```
The *print* output will now be the data *type* of the *variable*.  (ie., str, flt, int)

#### Math with variables
When you want to print two variables together, use the print function and, within the paranthesees, insert the first variable, followed by a plus sign, and then insert the second variable. 

For example:
```
var1 = 4 
var2 = 9
print(var1 + var2)
```
The outpull will be: 13. This is because you are adding two variable, var1 and var 2, that hold the values 4 and 9, respectively; and 4 + 9 = 13

However, you can not add two variables that are of different data types. 

A [[Integer]] and a [[Floating Point Number]] can not be added because python will automatically convert whatever result into a whole number. 

A [[Integer]] and a [[String]] can not be added because you cannot add a variable holding the value '4' and a variable holding the value 'Hello'; and hope that the output is 900. *Sarcasm*,**BUT** you can convert the variable holding the integer into a string; and then, if you add those same two variable, it would be the equivelant of you adding two strings together. Which we can do because they are the same [[Data Type]]s. 

For example: You are given the following variables 

```
var1 = 4
var2 = "Hello"
```
If you try to add them, 
```
print(var1 + var2)
```
Your code wont run because they are not of the same data type. So use the ```str``` function to modify the integer. In this case, var1 is equal to 4; therfore it will be the variable that the str function needs to modify.

```
print(var2 + "" + str(var1))
```
The output you would get is: Hello 4. 
*The two apostrophes in the middle, are just to add a space when generating an output.*

The image below is some math practice with variables. 
![[Pasted image 20211119231439.png]]
(1)A variable called "miles" was created, and it was assigned the value of 120; (2)another variable called "hours" was created, and it was assigned the value of 3; finally, (3)a third variable called "speed" was created, and it was assigned the value of the variable "miles", divided by, the variable "hours".  
Rember that two of the same data type, will give you the same data type when you receive your output, **but** this one didn't. 
```
miles = 120
hours = 3
```
The "miles" variable is an integer; the "hours" variable is also an integer. Yet we still got the following output:
```
40.0 
```
We got an float. 
Listen to ![[Recording 20211119234205.webm]] and here why python gave us back that result. #interesting 


### Functions 
[[Functions]] in python are block(s) of code which only run when it is called.
You can pass data, known as [[Parameters]], into a function.
A function can return data as a result.




---------------------------------------------------------------------------------------
														Work Cited 
1. https://cs.stanford.edu/people/nick/py/python-print.html





