# Global EV Sales (2010-2024) Data Analysis
## Overview
This project analyzes the Global Electric Vehicle (EV) Sales Data from 2010 to 2024 using Python and various data science libraries. The data provides insights into the adoption of EVs across different regions, modes of transport, and powertrain types.

The dataset used for this analysis was sourced from Kaggle. It contains information such as EV sales, stock share, and powertrain for different years and regions.


## Key Objectives
To analyze the trends in EV sales over the years.
To compare the adoption of different types of EVs across various regions.
To examine the parameters such as EV stock share, EV sales, and EV powertrain.
To visualize the data to gain insights into the global EV market growth.
## Dataset
The dataset is available on Kaggle:

Filename: IEA Global EV Data 2010-2024
Source: Kaggle Global EV Sales Dataset
Data fields:
region: The region where the EVs were sold.
category: Category of the data (e.g., historical).
parameter: Data parameter (EV stock share, EV sales, etc.).
mode: Mode of transport (Cars, Buses, etc.).
powertrain: Powertrain type (BEV, PHEV).
year: Year of the data point.
unit: Unit of measurement (percent, vehicles).
value: The actual value of the parameter.
Tools & Technologies
Python: Primary programming language for data analysis.
Pandas: Used for data manipulation and cleaning.
Matplotlib & Seaborn: For visualizing data trends and relationships.
Jupyter Notebook: For interactive data analysis and visualization.
## Key Steps in the Analysis:
Data Loading:

```python

df = pd.read_csv('/kaggle/input/global-ev-sales-2010-2024/IEA Global EV Data 2010-2024.csv')
df.head()
```
Data Exploration:

```
df.head() to display the first few rows of the dataset.
df.info() to get the general structure of the dataset.
```
## Data Cleaning:

Handling missing values.
Renaming columns for clarity.
Filtering data by regions and years.
## Data Visualization:

Bar plots for EV sales trends over the years.
Heatmaps to show EV sales distribution across different regions.
Line graphs to illustrate EV stock growth across time.
## Insights Gained:

Significant increase in EV adoption from 2010 onwards.
Regions like China and Europe lead in EV sales.
The shift from traditional vehicles to electric ones is becoming more evident, especially in the passenger car segment.
## Example Visualizations:
EV Sales Trends Over Years:

```python

sns.lineplot(data=df, x='year', y='value', hue='region')
plt.title('EV Sales Trends Over Years')
plt.show()
```
EV Stock Share Distribution Across Regions:

```python

sns.heatmap(data=df.pivot('region', 'year', 'value'), annot=True)
plt.title('EV Stock Share Distribution Across Regions')
plt.show()
```
## Conclusion
The data analysis provides valuable insights into how electric vehicles are becoming an integral part of the automotive market, especially in regions like Europe and China. The analysis also highlights the importance of clean energy initiatives in driving the growth of EVs globally.
