# Python-class-Session6-individual-assignment
individual assignment for Session 6 of GitHub

Task 1: Data quality assessment
Load the file and answer:
How many rows and columns?
What are the data types?
Which columns contain missing values?
Are there duplicated rows?
Expected skills (you can use alternatives):
read_csv()
shape
info()
isnull()
duplicated()
Task 2: Data cleaning
Prepare a clean dataset.
Requirements:
standardise categorical variables
handle missing values
remove duplicates
remove non-informative columns
handle outliers
Expected operations:
str.lower()
fillna()
drop_duplicates()
drop()
sns.boxplot() - for outliers detection and stats visualization
describe()
quantile()
Question to answer: Are missing values concentrated in specific regions or products?
Task 3: Revenue analysis
Answer:
Which product generated the highest total revenue?
Visualisation:
Bar chart of total revenue by product.
Expected:
 
groupby()
sum()
sort_values()
sns.barplot()

Task 4: Customer behaviour insights
Questions:
Which customer segment buys the most units?
Does sales channel influence revenue?
Visualisation:
Countplot or barplot
Revenue by sales channel
Expected:
groupby()
agg()
sns.barplot()
sns.countplot()
 

Task 5: Revenue by region
Question
Which region generated the highest total revenue?
Expected operations
 
df.groupby("Region")["xxx"].sum().sort_values()
 
Visualisation
sns.barplot()
horizontal bar chart

Task 6: Discount impact
Question
Does a higher discount lead to higher revenue?
Expected operations
 
df[[xxxx, xxxx]].corr()
 
Visualisation
Scatter plot
Regression plot (sns.regplot())

Task 7: Product popularity
Question
Which product sold the largest number of units?
Expected operations
 
df.groupby
 
Visualisation
Bar chart
Extension
Is the most sold product also the most profitable?
Task 8: Monthly sales trend
Question
How does revenue change over time?
Expected operations
 
df["Date"] = pd.to_datetime(df["Date"])
 
monthly = (
    df.groupby(df["Date"].dt.month)
    ["Revenue"]
    .sum()
)
 
Visualisation
Line chart
Concept tested
Date parsing
Time aggregation

Task 9: Revenue distribution
Question
Is revenue normally distributed?
Expected operations
 
df["Revenue"].describe()
 
Visualisation
Histogram
KDE plot
 
sns.histplot()
 

Advanced (not required)
Create a new column:
 
Profit = Revenue * (1 - Discount)
 
Questions:
Which product has highest profit?
Which region has best profit margin?
Does discount increase or reduce profit?
