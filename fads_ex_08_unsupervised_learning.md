# Fundamentals of Agro-Environmental Data Science

# Exercise 8 - Unsupervised Learning

Unsupervised Learning is a class of algorithms to be applied to data to which we 
do not know the expected output - data records do not contain a *label*. Two main 
types of analysis can be applied to these datasets:
- create groups or clusters of data points that have more similarities between 
themselves, based on a measure of distance and strategy of clustering - **clustering**
- reduce the dimensionality of the dataset - reduce the number of variables - 
keeping the common variance between variables - **dimensionality reduction**


## Description of the exercise

In this exercise you will in Jupyter Notebook two analysis of unsupervised
learning. The goal is to provide a very general overview of the steps involved 
in the analysis, without the need to understand all the details. The learning
of the methods will be done in the Machine Leaning course, latter in the master
programme. However, you should be able by know to understand the code in python
and do different attempts with the parameters of the algorithms, to check different
outputs.

If you have troubles setting your environment or starting Jupyter, check the FADS
Exercise 05 that explains how to get started.

## 1. Run a cluster analysis 

You can run the notebook `031-cluster-example.ipynb` in your environment, or 
in Google Colab. In each case, you should provide the environment with the 
necessary data file.

The notebook for the cluster analysis is available at https://github.com/isa-ulisboa/greends-fads-jupyter/tree/main/example03-cluster. The data file is in the `raw-data` 
directory, and was generated from the dms_INE database using the SQL script 
available at the `scripts` directory.

This notebook will run to cluster approaches, a **K-means** and a **Hierarchical cluster
analysis**.

All the required python modules to run the notebook should be by now installed in
the environment you are using. But in case a missing module error is triggered, 
you can always install it from the notebook creating a new cell and doing
```
!pip install <name_of_module>
```

## 2. Run a dimensionality reduction analysis

This second notebook `032-pca-example.ipynb` will allow to run a PCA. 
The notebook is a followup of the previous notebook, and is also available 
from https://github.com/isa-ulisboa/greends-fads-jupyter/tree/main/example03-cluster. 
It will use the same data file.

In this example, we will use PCA to reduce the number of variables, before repeating 
the cluster analysis. By doing this, we will reduce the noise of the data, and 
also eliminate redundant variables, i.e., correlated variables that structurally  
contain the same information. 









