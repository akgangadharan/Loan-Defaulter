Aim of the Project

Using historical loan data, identify what kinds of customers/loan applications are high risk and low risk, so that the company can:
Approve loans to good (low‑risk) customers.
Flag, price higher, or reject loans to high‑risk customers.
Design better credit policies and risk strategies.

Objectives of the Project

The objective is to analyse past loan data to find what kind of customers or loans are more likely to default, and use those insights to improve lending decisions..


About the Dataset
This case study aims to give us an idea of applying EDA in a real business scenario. In this case study, apart from applying the techniques that we have learnt in the EDA module, we will also develop a basic understanding of risk analytics in banking and financial services and understand how data is used to minimise the risk of losing money while lending to customers.

Key Features in the Dataset


➤ Workflow of the Project
The project follows a structured end-to-end data analysis workflow. The major steps included are:

1. Data Loading & Initial Overview
•	Importing necessary libraries
•	Loading the dataset
•	Viewing rows, columns, and structure

3. Data Cleaning & Pre-Processing
•	Handling missing values  
•	Removing duplicates

5. Feature Engineering
•	Binning
•	Value modification

7. Exploratory Data Analysis (EDA)
•	Visualizing 
   Univariate numeric variables analysis
   Bivariate analysis

9. Insight Generation
•	Summarizing key findings from all visuals
•	Identifying business opportunities and improvement areas
10. Report Preparation
•	Organizing results
•	Writing documentation
•	Preparing project summary and conclusion
Import Required Libraries
In this project, we use several Python libraries that help us load, clean, analyze, and visualize the supermarket sales dataset. Each library plays an important role in completing different steps of the analysis.

1. Pandas
Definition: A powerful library use for data manipulation and analysis.

Usage: Loading the dataset, cleaning data, exploring rows & columns, and creating new features.

Syntax:
import pandas as pd


2. Matplotlib
Definition: A basic visualization library for creating charts and graphs.
Usage: Bar charts, line graphs, scatter plots, and other basic visualizations.
Syntax:
import matplotlib.pyplot as plt

3. Seaborn
Definition: A statistical visualization library built on top of Matplotlib.
Usage: Heatmaps, boxplots, countplots, and advanced visualizations with clean styling.
Syntax:
import seaborn as sns

Read Data
To begin working with the supermarket dataset, we load the CSV file using the pd.read_csv() function. This reads the file and stores it in a DataFrame called df, which allows us to explore and analyze the dataset.

After loading, we use df.head() to display the first few rows and confirm that the data has been imported correctly.
