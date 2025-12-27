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

1	SK_ID_CURR	ID of loan in our sample

2	TARGET	Target variable (1 - client with payment difficulties: he/she had late payment more than X days on at least one of the first Y installments of the loan in our sample, 0 - all other cases)

3	NAME_CONTRACT_TYPE	Identification if loan is cash or revolving

4	CODE_GENDER	Gender of the client

5	CNT_CHILDREN	Number of children the client has

6	AMT_INCOME_TOTAL	Income of the client

7	AMT_CREDIT	Credit amount of the loan

8	AMT_ANNUITY	Loan annuity

9	AMT_GOODS_PRICE	For consumer loans it is the price of the goods for which the loan is given

10	NAME_TYPE_SUITE	Who was accompanying client when he was applying for the loan

11	NAME_INCOME_TYPE	Clients income type (businessman, working, maternity leave,…)

12	NAME_EDUCATION_TYPE	Level of highest education the client achieved

13	NAME_FAMILY_STATUS	Family status of the client

14	NAME_HOUSING_TYPE	What is the housing situation of the client (renting, living with parents, ...)

15	REGION_POPULATION_RELATIVE	Normalized population of region where client lives (higher number means the client lives in more populated region)

16	DAYS_BIRTH	Client's age in days at the time of application

17	DAYS_EMPLOYED	How many days before the application the person started current employment

18	DAYS_REGISTRATION	How many days before the application did client change his registration

19	DAYS_ID_PUBLISH	How many days before the application did client change the identity document with which he applied for the loan

20	OCCUPATION_TYPE	What kind of occupation does the client have

21	CNT_FAM_MEMBERS	How many family members does client have

22	REGION_RATING_CLIENT	Our rating of the region where client lives (1,2,3)

23	REGION_RATING_CLIENT_W_CITY	Our rating of the region where client lives with taking city into account (1,2,3)

24	WEEKDAY_APPR_PROCESS_START	On which day of the week did the client apply for the loan

25	HOUR_APPR_PROCESS_START	Approximately at what hour did the client apply for the loan

26	REG_REGION_NOT_LIVE_REGION	Flag if client's permanent address does not match contact address (1=different, 0=same, at region level)

27	REG_REGION_NOT_WORK_REGION	Flag if client's permanent address does not match work address (1=different, 0=same, at region level)

28	LIVE_REGION_NOT_WORK_REGION	Flag if client's contact address does not match work address (1=different, 0=same, at region level)

29	REG_CITY_NOT_LIVE_CITY	Flag if client's permanent address does not match contact address (1=different, 0=same, at city level)

30	REG_CITY_NOT_WORK_CITY	Flag if client's permanent address does not match work address (1=different, 0=same, at city level)

31	LIVE_CITY_NOT_WORK_CITY	Flag if client's contact address does not match work address (1=different, 0=same, at city level)

32	ORGANIZATION_TYPE	Type of organization where client works

33	OBS_30_CNT_SOCIAL_CIRCLE	How many observation of client's social surroundings with observable 30 DPD (days past due) default

34	DEF_30_CNT_SOCIAL_CIRCLE	How many observation of client's social surroundings defaulted on 30 DPD (days past due) 

35	OBS_60_CNT_SOCIAL_CIRCLE	How many observation of client's social surroundings with observable 60 DPD (days past due) default

36	DEF_60_CNT_SOCIAL_CIRCLE	How many observation of client's social surroundings defaulted on 60 (days past due) DPD

37	DAYS_LAST_PHONE_CHANGE	How many days before application did client change phone

38	AMT_REQ_CREDIT_BUREAU_HOUR	Number of enquiries to Credit Bureau about the client one hour before application

39	AMT_REQ_CREDIT_BUREAU_DAY	Number of enquiries to Credit Bureau about the client one day before application (excluding one hour before application)

40	AMT_REQ_CREDIT_BUREAU_WEEK	Number of enquiries to Credit Bureau about the client one week before application (excluding one day before application)

41	AMT_REQ_CREDIT_BUREAU_MON	Number of enquiries to Credit Bureau about the client one month before application (excluding one week before application)

42	AMT_REQ_CREDIT_BUREAU_QRT	Number of enquiries to Credit Bureau about the client 3 month before application (excluding one month before application)

43	AMT_REQ_CREDIT_BUREAU_YEAR	Number of enquiries to Credit Bureau about the client one day year (excluding last 3 months before application)

44	AMT_GOODS_PRICE_RANGE	#N/A

45	AMT_INCOME_TOTAL_RANGE	#N/A

46	AMT_CREDIT_RANGE	#N/A

47	AMT_ANNUITY_RANGE	#N/A

48	DAYS_EMPLOYED_RANGE	#N/A

49	DAYS_BIRTH_RANGE	#N/A



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
