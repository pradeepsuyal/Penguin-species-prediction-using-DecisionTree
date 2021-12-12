# Penguin species prediction using DecisionTree


![penguin](https://user-images.githubusercontent.com/86251750/145718893-09c56388-ab36-4854-a4ca-049862fb8158.jpg)

## Table of CONTENTS 
---------------------
 * [Aim](#aim)
 * [Dataset used](#data)
 * [Exploring the Data](#viz)
   - [Matplotlib](#matplotlib)
   - [Seaborn](#seaborn)
 * [using DecisionTree](#conclusion)
 

## AIM:<a name="aim"></a>

Our goal is to create a model that can help predict a species of a penguin based on physical attributes, then we can use that model to help researchers classify penguins in the field, instead of needing an experienced biologist

## Dataset Used:<a name="data"></a>

We will be using the same dataset through our discussions on classification with tree-methods (Decision Tree,Random Forests, and Gradient Boosted Trees) in order to compare performance metrics across these related models.

We will work with the "Palmer Penguins" dataset, as it is simple enough to help us fully understand how changing hyperparameters can change classification results.

Data were collected and made available by Dr. Kristen Gorman and the Palmer Station, Antarctica LTER, a member of the Long Term Ecological Research Network.

Gorman KB, Williams TD, Fraser WR (2014) Ecological Sexual Dimorphism and Environmental Variability within a Community of Antarctic Penguins (Genus Pygoscelis). PLoS ONE 9(3): e90081. doi:10.1371/journal.pone.0090081

Summary: The data folder contains two CSV files. For intro courses/examples, you probably want to use the first one (penguins_size.csv).

penguins_size.csv: Simplified data from original penguin data sets. Contains variables:

* species: penguin species (Chinstrap, Adélie, or Gentoo)

* culmen_length_mm: culmen length (mm)

* culmen_depth_mm: culmen depth (mm)

* flipper_length_mm: flipper length (mm)

* body_mass_g: body mass (g)

* island: island name (Dream, Torgersen, or Biscoe) in the Palmer Archipelago (Antarctica)

* sex: penguin sex

(Not used) penguins_lter.csv: Original combined data for 3 penguin species

    Note: The culmen is "the upper ridge of a bird's beak"

## Exploring the Data:<a name="viz"></a>

Here I will use pandas and seaborn visualization skills to determine if Fandango's ratings in 2015 had a bias towards rating movies better to sell more tickets.

**Matplotlib:**<a name="matplotlib"></a>
--------
Matplotlib is a Python 2D plotting library which produces publication quality figures in a variety of hardcopy formats and interactive environments across platforms. Matplotlib can be used in Python scripts, the Python and IPython shells, the Jupyter notebook, web application servers, and four graphical user interface toolkits.You can draw up all sorts of charts(such as Bar Graph, Pie Chart, Box Plot, Histogram. Subplots ,Scatter Plot and many more) and visualization using matplotlib.

Environment Setup==
If you have Python and Anaconda installed on your computer, you can use any of the methods below to install matplotlib:

     pip: pip install matplotlib

     anaconda: conda install matplotlib
     
     import matplotlib.pyplot as plt

for more information you can refer to [matplotlib](https://matplotlib.org/) official site

**Seaborn:**<a name="seaborn"></a>
------
Seaborn is built on top of Python’s core visualization library Matplotlib. Seaborn comes with some very important features that make it easy to use. Some of these features are:

**Visualizing univariate and bivariate data.**

**Fitting and visualizing linear regression models.**

**Plotting statistical time series data.**

**Seaborn works well with NumPy and Pandas data structures**

**Built-in themes for styling Matplotlib graphics**

**The knowledge of Matplotlib is recommended to tweak Seaborn’s default plots.**

Environment Setup==
If you have Python and Anaconda installed on your computer, you can use any of the methods below to install seaborn:

    pip: "pip install seaborn"*

    anaconda: " conda install seaborn"*
    import seaborn as sns
    
for more information you can refer to [seaborn](https://seaborn.pydata.org/) official site.


## using DecisionTree for prediction:<a name="conclusion"></a>

Decision tree is the most powerful and popular tool for classification and prediction. A Decision tree is a flowchart like tree structure, where each internal node denotes a test on an attribute, each branch represents an outcome of the test, and each leaf node (terminal node) holds a class label. 

**Construction of Decision Tree :**

A tree can be “learned” by splitting the source set into subsets based on an attribute value test. This process is repeated on each derived subset in a recursive manner called recursive partitioning. The recursion is completed when the subset at a node all has the same value of the target variable, or when splitting no longer adds value to the predictions. The construction of decision tree classifier does not require any domain knowledge or parameter setting, and therefore is appropriate for exploratory knowledge discovery. Decision trees can handle high dimensional data. In general decision tree classifier has good accuracy. Decision tree induction is a typical inductive approach to learn knowledge on classification.

![DecisionTree](https://j.gifs.com/KzQbjl.gif)

**Evaluation with  Classification Report**

                precision    recall  f1-score   support

      Adelie       0.95      0.95      0.95        40
     Chinstrap     0.93      0.96      0.95        27
      Gentoo       1.00      0.97      0.98        33

    accuracy                           0.96       100
    
**Visualizing the Tree**

Online Documentation: https://scikit-learn.org/stable/modules/generated/sklearn.tree.plot_tree.html

![download](https://user-images.githubusercontent.com/86251750/145719157-dfba7ab7-fa12-4a81-8f54-49a52e1d6cb7.png)

**Max Depth**

                precision    recall  f1-score   support

      Adelie       0.87      0.97      0.92        40
    Chinstrap      0.91      0.78      0.84        27
      Gentoo       1.00      0.97      0.98        33

    accuracy                           0.92       100
    
![download](https://user-images.githubusercontent.com/86251750/145719205-16277bcd-eaff-45b2-9d40-d5af5d4adb13.png)

**Max Leaf Nodes**

                precision    recall  f1-score   support

      Adelie       0.95      0.95      0.95        40
    Chinstrap      0.91      0.78      0.84        27
      Gentoo       0.86      0.97      0.91        33

    accuracy                           0.91       100

![download](https://user-images.githubusercontent.com/86251750/145719263-d0b1c957-fd2b-41c7-b842-c1d88006447f.png)

**Criterion**

                precision    recall  f1-score   support

      Adelie       0.95      0.97      0.96        40
    Chinstrap      0.96      0.96      0.96        27
      Gentoo       1.00      0.97      0.98        33

    accuracy                           0.97       100

![download](https://user-images.githubusercontent.com/86251750/145719309-ab646cea-38fb-4e97-9aab-df1e24526a37.png)

**Our model gives us an accuracy of 96% which is quite good**

***language used***
--------------------------
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

**Tools**
-----------------------
[![Made withJupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=for-the-badge&logo=Jupyter)](https://jupyter.org/try)    ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)   ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)  ![Made with matplotlib](https://user-images.githubusercontent.com/86251750/132984208-76ce70c7-816d-4f72-9c9f-90073a70310f.png)  ![seaborn](https://user-images.githubusercontent.com/86251750/132984253-32c04192-989f-4ebd-8c46-8ad1a194a492.png)

