# Fundamentals of Agro-Environmental Data Science

# Exercise 6 - Run Data Science workflows in Jupyter Notebook 

This is a learning/reading exercise, with several tasks. You should repeat all 
the examples given in your system, and check that you obtain equivalent results.

> An exercise submission via Moodle is required once completed. The deadline for submissions is **1st November 2024**.


## Introduction

Jupyter Notebook is a opensource web application for creating and sharing interactive
computing documents using multiple programming languages. It uses the file format
`.ipynb`, which combines text (in markdown format), code, and outputs in a single 
file. The code can be in more that 40 different languages (R, Julia, Scala, etc...), 
although in this course we will use **python**. Jupyter Notebook also integrates 
well with big data tools (e.g. Apache Spark). The `.ipynb` files are, internally 
text files with a **JSON** format.

The fact it is interactive makes it very convenient to develop data science analysis.
After running, you can export the notebook as a report to PDF or HTML.

The cluster of Jupyter tools include other tools:
- Jupyter Lab: a newer interface web application that enables to open several notebooks 
at once;
- Jupyter Hub: the multi-user application for teams and companies.

## Structure of a Jupyter Notebook

Jupyter Notebooks are a combination of three types of components:
- code cells, which contains code in the language selected for the kernel
- text cells, which contain text in Markdown format
- output components, that display outputs of the code execution. It can contain 
text outputs, tables, charts, pictures, etc.

You can add many as cells as you want to your Notebook. At the moment you add a 
cell, you set it as being of type code or Markdown.

## Workflow in Jupyter Notebook

### Jupyter Notebook Dashboard
When opening a new Jupyter Notebook session, your browser will open a new window 
with the **Jupyter Notebook Dashboard**. This shows the files and directories of your 
current working directory (the one you run the session). You can use the Dashboard to:
- create, duplicate, rename and delete directories
- create, duplicate, rename, download and delete files
- create, duplicate, rename, shutdown, download and delete notebooks
- upload files
- check and change the status of notebooks: running, shutdown

### Jupyter Notebook

On the Dashboard, as mentioned, you can create Notebooks with the option 
`New --> Python 3 (ipykernel)`. This will open a new tab in the browser with the 
new notebook named `Untitled`. The working windows of the new Notebook includes 
the menu, the toolbar and the working area. It is, at this stage, ready to run 
your code, placed in code cells. Or you can add cells of Markdown type, to add 
text to the notebook. This is useful to explain the steps of the code, including 
options, and the outputs.

**Code cells** start with empty square brackets `[]`on the left. This means that the 
code of this cell was not run yet. To run, you can place the cursor on the cell, 
and the press CTRL+ENTER. A number will appear on the square brackets. This number
will be sequential between code cells, indicating the sequence you run the code
cells. If the code run has output, this will appear bellow the run cell.

**Markdown cells** can be edited, to add your text. After that, to render to formatted
text, also press CTRL+ENTER. To edit again, simple click twice on the text, to 
enter the edit mode again.

## Run your first Notebook. 

We will proceed our exercise now so that you run your first Jupyter Notebook in 
your local computer. We will use a pre-created example on health, that creates 
a model to predict breast cancer. In this example, you will not understand the code
and algorithms you will run, and this is OK. You will learn later in the master
how to create and interpret these models. The purpose of this exercise is only
to learn how to start and use Jupyter Notebooks.

### Pre-requisites

To be able to run Jupyter in our computer, you need to have:
- python installed
- pip installed
- Jupyter installed

Assuming that the first two are already installed, to install Jupyter, first 
upgrade pip in a terminal:
```
$ pip3 install --upgrade pip
```
Then install Jupyter
```
$ pip3 install jupyter
```

### 1. Start your Jupyter environment

1. Open a bash terminal and change directory to the place you want your jupyter 
files to be. It's a good idea to create a new directory for this.

2. First, download the example. In the terminal, run:
   ```
   $ curl https://raw.githubusercontent.com/isa-ulisboa/greends-fads-jupyter/main/example01-breast-cancer/example-health.ipynb > example-health.ipynb
   ```
   This will create a new local file named `example-health.ipynb`.

3. Now you can open your Jupyter session. Run:
   ```
   $ jupyter notebook .
   ```
   A new browser window will open with the Jupyter Notebook Dashboard at the 
   address http://localhost:8888/tree. 
   The terminal now shows logs of the jupyter session, so you can not use it for 
   interacting with the system. You will use it to end the jupyter session, using CTRL+C.

   In the Dashboard, you will find the just created `example-health.ipynb` file.

### 2. Download data from Kaggle

**Kaggle** is an excellent resource for data scientists, including many real data 
sets, and complete notebooks with analysis, models, etc, made by the community 
and freely available to reuse. You can use Kaggle to seek for examples and guidance, 
and can even use the platform to run your analysis. To use **Kaggle**, you will 
need to register [at the site](https://www.kaggle.com). 

Now, let's prepare our environment to contain raw data. 

1. Using the Notebook Dashboard, create a new folder with the name `raw-data`. This 
folder will contain  But, before running it, we need to download the data file. 

2. Go to
https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data and download 
the csv data file. Place the downloaded file inside the `raw-data` folder you created before. 

### 3. Run your first notebook

1. Now your should have all things set to run your Jupyter Notebook. In the Dashboard,
click on the `example-health.ipynb`. This will open a new browser tab.

2. Read the introductory text of the notebook, that explains the problem. After 
that, run each code cell sequentially (you can use CTRL+ENTER, or SHIFT+ENTER to 
run and jump to the next cell), and check the output and explanations.

### 4. Run in Google Colab

You can run the example also in Google Colab.

1. Open a Colab session and upload the notebook file from your computer.

2. Create a new folder named `raw-data`, and upload the `data.csv` file.

3. Run the notebook cells, as you did in your computer.

## 5. Submit your update repository
> Share the Google colab and submit the link to Moodle at [Exercise 6 submission](https://elearning.ulisboa.pt/mod/assign/view.php?id=476839).


## Wrap up
In this exercise, you learned about Jupyter Notebook:
- What is Jupyter Notebooks
- The structure and components of Jupyter Notebook
  - code cells
  - markdown cells
- Start Jupyter Notebook
- Manage files with Jupyter Notebook Dashboard
- What is Kaggle 
- Run code in Jupyter Notebook
- Run jupyter notebook in Google Colab

# References
https://docs.jupyter.org/en/latest/  









