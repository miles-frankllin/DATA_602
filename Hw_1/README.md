# Overview

The goal of this project was to impliment a Linear Regression on a dataset of my choice. I chose to regress alcohol density onto percent alchol content from a pair of data sets from UCIML. While exploring the data, I became interested in how the rated quality effectd this measurement, and how the color of while effect the results. This exploration was not published in the [Technical Notebook](), altough the exploratory graphs can be found in [Additional Notebook](). 

# Navigation (Need to link notebooks)

[Technical Notebok](https://github.com/a-woodbury/A-House-with-a-View#data) -
[Additional NoteBook](https://github.com/a-woodbury/A-House-with-a-View#model) -
[Data - Kaggle](https://www.kaggle.com/uciml/red-wine-quality-cortez-et-al-2009) - 
[Data - UCIML](https://archive.ics.uci.edu/ml/machine-learning-databases/wine-quality/)

# Requirements
<pre>
Languages    : Python 3.8.3
Tools/IDE    : Anaconda
Libraries    : pandas, matplotlib, seaborn, numpy, scipy, sklearn
</pre>

# Data Sources
Note: Initial data was found from [Kaggle](https://www.kaggle.com/uciml/red-wine-quality-cortez-et-al-2009), but was all downloaded from [UCIML](https://archive.ics.uci.edu/ml/machine-learning-databases/wine-quality/) 

### Red Wine Data
<pre>
File Name      : winequality-red.csv
URL            : https://archive.ics.uci.edu/ml/machine-learning-databases/wine-quality/
Limitations    : N/A
Concerns       : N/A
Dimensions     : 1599 rows × 12 columns
Columns        : fixed acidity (float64), volatile acidity (float64), citric acid (float64), residual sugar (float64), chlorides (float64), free sulfur dioxide (float64), total sulfur dioxide (float64), density (float64), pH (float64), sulphates (float64), alcohol (float64), quality (int64)
</pre>
### White Wine Data
<pre>
File Name      : winequality-white.csv
URL            : https://archive.ics.uci.edu/ml/machine-learning-databases/wine-quality/
Limitations    : N/A
Concerns       : N/A
Dimensions     : 4898 rows × 12 columns
Columns        : fixed acidity (float64), volatile acidity (float64), citric acid (float64), residual sugar (float64), chlorides (float64), free sulfur dioxide (float64), total sulfur dioxide (float64), density (float64), pH (float64), sulphates (float64), alcohol (float64), quality (int64)
</pre>
### Cleaned Data Set
<pre>
File Name      : winequality-both_cleaned.csv
URL            : N/A
Limitations    : N/A
Concerns       : There are many more instances of white wine than red wine.
Dimensions     : 6491 rows × 13 columns
Columns        : fixed acidity (float64), volatile acidity (float64), citric acid (float64), residual sugar (float64), chlorides (float64), free sulfur dioxide (float64), total sulfur dioxide (float64), density (float64), pH (float64), sulphates (float64), alcohol (float64), quality (int64), color (object)
</pre>

# References
<pre>
URL            : https://github.com/a-woodbury/A-House-with-a-View
Author         : Alphonso Woodbury, Joseph McHugh
Purpose        : I reference the source code of this project to better understand how to format a project in Jupyter NoteBook.
<pre>
