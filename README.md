# DataScienceML-JupyterNotebook

Personal Project

## Description

I have written a Jupyter notebook in Python in order to perform exploratory data analysis on a large number of wine reviews given by different tasters for various wines from across the world and to integrate a machine learning algorithm as to predict the label of a specific wine having only its description as input.

I have preprocessed the dataset, after reading the two CSV files in a Spark dataframe, by dropping irrelevant columns, merging the files, dropping rows containing missing data, renaming certain columns and casting them to numeric data types so they can serve as input to a ML algorithm. Then I have set up a pipeline with stages as it follows: tokenizing regular expressions, counting the words from each wine description and indexing the strings from the label column. I have split the dataframe in test data and training data (70% and 30% respectively) and I have fitted a model implementing the Naive Bayes algorithm on the training data, then transforming the test data to make predictions. The model achieved a score of roughly 60% when using the multiclass classification evaluator from Spark.

I have plotted data using seaborn (which is based on matplotlib) in bar, line and whisker plots, to emphasize correlations between features such as: wine country of origin and its price, evolution of awarded points and price (based on the countries' mean price) and the price/points distribution in the provinces with the highest mean price and by country of origin. These plots had their data provided by dataframes which resulted from grouping, sorting and aggregating the initial dataframe.
