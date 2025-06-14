# Airbnb Data Analysis

![seattle](https://github.com/user-attachments/assets/11f713b5-aa9f-43a7-b203-1a68f21ba25b)




## Overview
### What are the factors and features of a listing that make an Airbnb listing in Seattle more expensive?  
  
That is the question this project aims to answer. We started of by collecting data of listings in Seattle from [Kaggle](https://www.kaggle.com/airbnb/seattle). Then, we cleaned the data to a useful format for data analysis. We then did Exploratory Analysis on the data by focusing on 3 sub-problems:

1. What are the features/facilities/ammenities of a property that affect its price?
2. Are there particular locations in Seattle where Airbnb listings fetch higher prices?
3. Does textual data in the summary and sentiments of reviews affect price?

Afterwards, we did Machine Learning on the data by adpoting 6 different **Regression** models for our regression problem. They were:

1. Linear Regression
2. Random Forrest
3. XGBoost
4. CatBoost
5. Ridge Regression
6. Lasso Regression

## Enhancements

We enhanced our exploratory analysis by adding:

1. Interactive visualizations with Plotly for better data exploration.

2. Dropdown filters, hover tooltips, zoom, and pan features for improved user experience.

3. Storytelling markdown cells that guide the user through insights and key takeaways from the data.

We partitioned the data into train and test sets and evaluated the models on their prediction accuracy. Once we found the most accurate prediction model, we used that model in a library called **TreeInterpreter** which decomposed the prediction into a sum of contributions from each feature: `Prediction = Bias + Feature1 x Contribution1 + … + FeatureN x ContributionN`. We used this to find the most important features that affected the price of a listing.

## Getting Started

### Prerequisites

If you would like to download and run all the data analysis and prediction models on your own machine, it is recommended to use to **Anaconda** and **Jupyter Notebook**. If you use **Anaconda** most of the packages used in this project are pre-installed except the following few:

+ Graphviz
+ Langdetect
+ Wordcloud
+ XGBoost
+ CatBoost
+ TreeInterpreter

### Installing and running

Install the required packages by running the following commands in your terminal:

```
pip install graphviz
pip install langdetect
pip install wordcloud
pip install xgboost
pip install catboost
pip install treeinterpreter
pip install plotly 
pip install ipywidgets
```

Enable interactive widgets in Jupyter Notebook:
```
jupyter nbextension enable --py widgetsnbextension
```

You can then open the following files with **Jupyter Notebook**:
```
Exploratory Analysis Problem 1.ipynb
Exploratory Analysis Problem 2.ipynb
Exploratory Analysis Problem 3.ipynb 
Machine Learning Models.ipynb
``` 

## Built with

+ [Python 3](http://www.python.org/) - Main programming language used, done in Jupyter Notebook
+ [Pandas](https://pandas.pydata.org/) - Main library used to manipulate the datasets
+ [Scikit-learn](https://scikit-learn.org/stable/) - Main library used for machine learning
+ [Matplotlib](https://matplotlib.org/) - Used for graph plots and visualizations
+ [Python NLTK](https://www.nltk.org/) - Used during exploratory analysis to get further insights into the textual data
+ [XGBoost](https://xgboost.readthedocs.io/en/latest/) - Used to implement gradient boost decision trees
+ [CatBoost](https://catboost.ai/) - Used to implement gradient boost decision trees
+ [TreeInterpreter](https://pypi.org/project/treeinterpreter/) - Used to decompose predictions into a sum of contributions from each feature
+ [Plotly](https://plotly.com/python/) - Interactive visualizations
+ [Ipywidgets](https://ipywidgets.readthedocs.io/en/latest/) - Interactive controls (dropdowns, sliders)

