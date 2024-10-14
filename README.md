# Research Porfolio: Excel to SQL to PowerBI

![Data Transformation Process](assets/images/data transformation.png)

# Table of contents

- [Objective](#objective)
- [Data Source](#data-source)
- [Design](#design)
  - [Tools](#tools)
- [Development](#development)
  - [Data Exploration](#data-exploration)
  - [Data Cleaning](#data-cleaning)
  - [Data Transformation](#data-transformation)
- [Data Quality Test](#data-quality-test)
- [Data Visualisation](#data-visualisation)
- [Findings](#findings)
- [Recommendations](#recommendations)
- [Conclusion](#conclusion) 



# Objective

Design a dashboard that delivers critical insights into the top UK YouTubers, enabling the investment team to strategically identify which creators present the best partnership opportunities based on their viewership metrics. The goal is to help the company choose influencers whose audience engagement and reach can drive product sales, maximize revenue, and contribute to the overall growth of the company and its product portfolio


# Data-source

The data was sourced from kaggle and contains the viewship metrics of each individual youtuber such as channel name,views,subcribers and total videos

# Design

Design a Power BI dashboard that showcases key viewership metrics of individual YouTubers, providing the investment team with a comprehensive and interactive overview of each creator's performance. The dashboard should offer a user-friendly interface, enabling detailed analysis of various metrics to support informed decision-making when selecting potential partners for product promotion and revenue growth

# Tools

|Tool 	|Purpose|
|-------|-------|
|Excel 	|Exploring the data|
|SQL Server 	|Cleaning, testing, and analyzing the data|
|Power BI 	|Visualizing the data via interactive dashboards|
|GitHub 	|Hosting the project documentation and version control|

# Development
The process begins with gathering the relevant dataset, followed by an initial exploration in Excel to understand the data. The data is then loaded into SQL Server for structured storage and cleaned using SQL queries to ensure accuracy. After testing the data for consistency, it is visualized in Power BI, where key viewership metrics and insights are presented. These findings are analyzed to determine the best YouTuber partnerships for the investment team. The process is documented, and finally, the data, insights, and documentation are published on GitHub Pages for easy access and collaboration


## Data-exploration

The dataset is first explored in Excel to perform an initial review, where key columns are identified, data profiling is conducted, and the the patterns in the dataset examined. Once a basic understanding is established, the data is imported into SQL Server to enable more robust handling, and querying, ensuring it is ready for  efficient analysis

## Data-cleaning
The objective is to refine the dataset, ensuring it is well-structured and ready for analysis. This involves retaining only relevant columns, ensuring data types are appropriate for each column, and eliminating null values to guarantee that all records are complete and accurate

Below is a table outlining the constraints on our cleaned dataset:
|Property |	Description |
|---------|-------------|
|Number of Rows | 	100 |
|Number of Columns |	4 |

And here is a tabular representation of the expected schema for the clean data:
|Column Name 	|Data Type 	|Null|
|-------------|-----------|----|
|channel_name 	|VARCHAR 	|NO |
|total_subscribers 	|INTEGER| 	NO|
|total_views| 	INTEGER |	NO|
|total_videos 	|INTEGER 	|NO|


## Data-transformation




Explore the Data in Excel: Conduct an initial review of the dataset in Excel, performing tasks such as data profiling, identifying key columns, and getting a preliminary understanding of patterns or outliers.

Load the Data into SQL Server: Import the dataset into SQL Server for more robust data handling, storage, and querying, ensuring scalability and efficiency for further analysis.

Clean the Data with SQL: Use SQL queries to clean and preprocess the data by removing duplicates, handling missing values, correcting inconsistencies, and transforming raw data into structured formats for better analysis.

Test the Data with SQL: Validate the data's integrity by running SQL tests to ensure accuracy, consistency, and reliability. This includes verifying data ranges, relationships, and constraints.

Visualize the Data in Power BI: Build interactive visualizations and dashboards in Power BI, showcasing key metrics like viewership, subscriber growth, engagement rates, and other performance indicators of each YouTuber.

Generate Findings Based on Insights: Analyze the Power BI visuals to derive meaningful insights about the YouTubers' performance, identifying trends and metrics that are crucial for decision-making, such as which YouTubers offer the best partnership potential.

Write the Documentation + Commentary: Document the entire process, including data acquisition, cleaning steps, testing procedures, insights from visualizations, and a narrative commentary explaining the results and recommendations for stakeholders.

Publish the Data to GitHub Pages: Share the final data, visualizations, and documentation publicly by publishing them to GitHub Pages, allowing for easy access and collaboration across the team or broader audience


























