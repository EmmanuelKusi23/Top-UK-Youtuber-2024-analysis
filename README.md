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


# Data source

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


## Data exploration

The dataset is first explored in Excel to perform an initial review, where key columns are identified, data profiling is conducted, and the the patterns in the dataset examined. Once a basic understanding is established, the data is imported into SQL Server to enable more robust handling, and querying, ensuring it is ready for  efficient analysis

## Data cleaning
The objective is to refine the dataset, ensuring it is well-structured and ready for analysis. This involves retaining only relevant columns, ensuring data types are appropriate for each column, and eliminating null values to guarantee that all records are complete and accurate

Below is a table outlining the constraints on our cleaned dataset:
|Property |	Description |
|---------|-------------|
|Number of Rows | 	100 |
|Number of Columns |	4 |

And here is a tabular representation of the expected schema for the clean data:
|Column Name 	|Data Type 	|Null|
|-------------|-----------|----|
|channel_name 	|VARCHAR 	|  NO|
|total_subscribers|INTEGER|NO  |
|total_views| 	INTEGER   |	NO |
|total_videos 	|INTEGER 	|NO  |


## Data transformation

```sql

/*
# 1. Select the required columns
# 2. Extract the channel name from the 'NOMBRE' column
*/

-- 1.
SELECT
    SUBSTRING(NOMBRE, 1, CHARINDEX('@', NOMBRE) -1) AS channel_name,  -- 2.
    total_subscribers,
    total_views,
    total_videos

FROM
    top_uk_youtubers_2024

```

``` sql
/*
# 1. Create a view to store the transformed data
# 2. Cast the extracted channel name as VARCHAR(100)
# 3. Select the required columns from the top_uk_youtubers_2024 SQL table 
*/

-- 1.
CREATE VIEW view_uk_youtubers_2024 AS

-- 2.
SELECT
    CAST(SUBSTRING(NOMBRE, 1, CHARINDEX('@', NOMBRE) -1) AS VARCHAR(100)) AS channel_name, -- 2. 
    total_subscribers,
    total_views,
    total_videos

-- 3.
FROM
    top_uk_youtubers_2024
```

# Data visualisation

Below is a visaulization presentation shwocasing the various youtubers along with their viewship metrics

![Data Visualisation](assets/images/Top UK youtubers 2024.png)

# Findings


![Data Findings](assets/images/excel vs%20 sql analysis.png)





# Recommendations
Based the viewship metrics that is the views per subcriber, Dan Rhodes appears to be the best option because there is a higher ROI compared to other channels































