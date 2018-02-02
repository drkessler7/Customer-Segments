## Customer Segments

### Overview
One of the biggest costs to today’s businesses is shipping. This project explores how machine learning can help companies reduce their delivery costs while maintaining customer satisfaction. As an engineer dedicated to staying up-to-date with the latest tools and trends, I completed this unsupervised learning project as part of a continuing education program at Udacity.

### Problem
As businesses continue to grow and more people shop online, the demand for delivery services increases. Millions of people across America buy from Amazon, and take advantage of free 2-day shipping that is included with Amazon Prime memberships. This service is widely popular, and draws more and more new customers to Amazon. 

However, it costs a lot of money to provide such fast shipping. Amazon spent more than $7billion in 2016 on shipping alone, and expects to spend more each year. They have experimented with various ways to cut back on shipping costs. Some of these include bicycle couriers, Prime Air drones, Prime Now delivery, and a crowdsourced package delivery system called Amazon Flex. By improving delivery schedules, businesses can save millions of dollars.

### Process

#### Data Source
This project uses data from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Wholesale+customers) and is open to the public to use.

#### Data Description
The data  consists of a single .csv file that contains information for 440 clients of a wholesale distributor. There are eight attributes given for each client, and six of them are closely examined. These attributes are numerical values that describe the amount of cash each client spent on the following item categories from the distributor: ‘Fresh’, ‘Milk’, ‘Grocery’, ‘Frozen’, ‘Detergents_Paper, and ‘Delicatessen’. 

#### Data Exploration
First, basic descriptive statistics such as the average, minimum, and maximum values are calculated for each of the six features. Then I compare features to each other by plotting the values of one feature on one axis, and values for the other feature on the other axis. I do this for all combinations of features to see if there are any interesting correlations between two features.

#### Data Preprocessing
I apply a simple mathematical operation to the all of the feature values to change them in a way what will make the data easier to observe and work with later. Next I look for strange values called ‘outliers’ in the data which can diminish the accuracy of a machine learning model. Not all outliers are bad, as they can help point out important insights about the data. Here I remove unhelpful outliers.

#### Feature Transformation
I apply a kind of transformation called ‘Principal Component Analysis (PCA)’ on all six features. This effectively creates a reduced number of new features that can be used by machine learning models to produce better results.

#### Clustering ML Algorithms
I consider two different machine learning algorithms for this project: K-means clustering and a Gaussian Mixture Model (GMM). I look at the data and consider the advantages and disadvantages of each algorithm. I use a GMM to take the client data and break the clients down into different groups. After numerous trials, I find that clients are best grouped when they are broken into two groups.

#### Conclusion
By identifying two different groups of clients, the distributor can better plan how they deliver to their clients. If one group needs more fresh produce or items that may spoil quickly, they may need more frequent deliveries than the other one. 

The distributor can drop their costs if they can reduce the frequency of deliveries to the other group. By adjusting their delivery schedule, the distributor can save money while maintaining their clients’ satisfaction. Additionally, if they begin to serve a new client, they can look at the expenditure data of that client to anticipate their delivery needs.

## About Files/Folders in this Repository
* ‘customer_segments.ipynb’: This Jupyter Notebook explains the in-depth reasoning behind all of the steps that I take in completing this project. It contains Python code cells that can be run individually, as well as markdown cells that only contain text to explain the each of the steps. 

* ‘customer_segments.html’: This html file’s contents are the same as those of the ‘customer_segments.ipynb’ notebook, and can be opened in a web browser. 

* ‘Customer Segments Images’: This folder contains screenshots of various images and charts created by this notebook. 

* ‘Customer Segments Starter Files’: This folder contains the files provided by Udacity to start this project.

## Installation
The installation documentation for the Jupyter platform can be found [here](https://jupyter.readthedocs.io/en/latest/install.html).

Documentation for advanced usage of Jupyter notebook can be found [here](https://jupyter-notebook.readthedocs.io/en/latest/).

This project requires **Python 2.7** and the following Python libraries installed:
* [numpy](http://www.numpy.org/)
* [pandas](http://pandas.pydata.org)
* [scikit-learn](http://scikit-learn.org/stable/)
* [matplotlib](http://matplotlib.org/)

To run locally on your machine, launch from a command prompt with:
 
     $ jupyter notebook
