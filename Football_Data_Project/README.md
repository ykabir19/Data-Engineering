# ⚽️ Football Players Data Pipeline

## Project Overview
This project focuses on building a data pipeline and performing analysis on football player data. The dataset was sourced from [Kaggle](https://www.kaggle.com/datasets/maso0dahmed/football-players-data) and contains information on player attributes, performance metrics, and financial details. The goal of this project is to process, clean, store, and analyze this data using Python and MySQL.

![image](<img width="658" alt="Screenshot 2024-10-25 at 15 29 30" src="https://github.com/user-attachments/assets/1e2c5a12-5dcc-42b9-a430-51bc2bd99d67">)
## Table of Contents
- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Database Design and Schema](#database-design-and-schema)
- [Data Pipeline](#data-pipeline)
- [Key Features](#key-features)
- [Future Improvements](#future-improvements)

## Technologies Used
- Python: For data ingestion, cleaning, and transformation.
- MySQL: For data storage and relational database management.
- pandas: For data manipulation and analysis.
- SQL: For querying and managing the database.
- Jupyter Notebook: For analysis and reporting.


## Database Design and Schema
### Methodology
The database design for this project is based on a relational model, ensuring efficient data organization, minimal redundancy, and optimized querying capabilities. The following design principles guided the schema structure:
- Normalization: Data was split into logical tables to reduce redundancy and ensure consistency. By adhering to 3rd Normal Form (3NF), each piece of information is stored only once, and tables are connected via foreign key relationships.
- Data Separation: Player attributes are divided into separate tables based on categories—personal information, performance metrics, financial details, and national team data. This separation not only keeps the data organized but also allows for easier modifications and updates as new metrics or attributes are added.
- Scalability and Flexibility: The schema is designed to support future data extensions, such as additional performance metrics, new financial details, or expanded player data. By structuring the tables relationally, new data types can be added without altering the overall design.

### Schema Overview
The database consists of four main tables:
- Players: Contains core static player data, such as name, birth_date, age, nationality, and physical attributes like height_cm and weight_kgs.
- Performance_Metrics: Stores detailed performance metrics for each player, including attributes like overall_rating, potential, dribbling, and sprint_speed. This table is connected to Players via a foreign key, allowing for efficient linkage and analysis of player statistics.
- Financials: Includes financial data such as value_euro, wage_euro, and release_clause_euro. By keeping financial details separate, the schema allows independent updating of contract-related information.
- National_Team: Holds information on players' participation in national teams, with fields for national_team, national_rating, and national_team_position. This setup supports focused analysis on national team players while keeping the main player data intact.

This relational model provides a clean, scalable database structure for comprehensive and efficient querying, making it ideal for handling sports data and supporting in-depth analysis of football players.

## Data Pipeline
1. Data Ingestion:
The dataset was imported from a CSV file containing player attributes and performance metrics.

2. Data Cleaning:
Missing values were handled by imputing medians for financial data, filling in categorical values, and transforming data types.
Created additional features, such as calculating player age based on their birth date.

3. Data Transformation:
The data was normalized and split into relational tables to minimize redundancy and ensure data integrity.

4. Data Storage:
The cleaned and transformed data was loaded into a MySQL database with separate tables for player information, performance metrics, financials, and national team data.

## Key Features 
- Data Pipeline: End-to-end pipeline for ingestion, cleaning, and transformation of football player data.
- MySQL Storage: Efficient storage using a normalized relational database design.
- Data Analysis: Basic querying and insights extraction using SQL.

## Future Improvements
- Implement advanced data visualization to explore player metrics.
- Integrate real-time data ingestion from football APIs for live updates.
- Build a front-end dashboard for interactive data exploration.

