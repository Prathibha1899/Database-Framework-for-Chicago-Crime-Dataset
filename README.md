# Chicago Crime Database Project
The aim of this project is to design and implement a comprehensive Chicago Crime Database to store and manage crime-related data. The database will facilitate the storage, retrieval, and analysis of crime data across various districts and neighborhoods in Chicago. Key entities include crime records, district information, FBI codes, ward details, community areas, and other crime-related metadata. The goal is to help law enforcement agencies, researchers, and data analysts efficiently query and analyze crime patterns, trends, and statistics.

## Entity-Relationship Diagram (ERD)
The ER diagram for the Chicago Crime Database includes the following entities:

- District: Contains information about the police districts in Chicago, including district name, address, commander, and contact details.
- FBI Code: Stores the details of FBI crime codes and descriptions used to categorize crimes.
- Community Area: Represents Chicago's community areas, including population, name, and geographic side.
- IUCR(Illinois Uniform Crime Reporting): Defines crime categories and descriptions, including primary and secondary descriptions.
- Ward: Represents the political wards of Chicago, including ward details such as alderman, office contact information, and population.
- Neighborhood: Stores the neighborhood details, linking to community areas.
- Crime: Contains the actual crime records, including case number, date, location, type, and related foreign keys (such as district, IUCR, FBI code).

The relationships between these entities are clearly represented by primary and foreign keys, showing how tables like crime, district, and ward are related.

## SQL Execution Steps
To set up the database, perform the following steps:

1. Run the `create.sql` script to create the tables and relationships. This file contains the SQL statements necessary for defining the schema of the soccer database.

2. Populate the database by executing the `load.sql` script, which should contain INSERT statements for each table.

3. Once the SQL scripts have been executed successfully, verify the integrity of the database by querying the tables to ensure data is populated correctly.

## Queries Execution Comments
After setting up and populating the database, you can run various SQL queries to retrieve, analyze, or manipulate crime-related data. Some example queries include:

- Retrieve crime records by district, date range, or specific crime type.
- Find statistics such as the number of crimes per community area or ward.
- Aggregate crimes based on FBI codes or IUCR codes for trend analysis.
- Get detailed information about police districts and wards, including commanders and alderman details.

# Chicago Crime Database Web Application
The web application provides an interactive platform to query and visualize data from the Chicago Crime Database. Built using Streamlit, the application connects to a PostgreSQL database and allows users to perform predefined and custom SQL queries for insights into crime data.

## Features
### Interactive Query Interface
- Navigate through database tables such as:
  - `District`
  - `FBI Code`
  - `Community Area`
  - `IUCR`
  - `Ward`
  - `Neighborhood`
  - `Crime`
- Retrieve specific insights using predefined queries, e.g.:
  - Districts managed by a specific commander.
  - Community areas sorted by population.
  - Crimes filtered by date range or type.

### Custom Query Support
- Execute ad-hoc SQL queries using the "Custom Query" page.
- Visualize results dynamically in a tabular format.

### Streamlit Framework
- User-friendly interface built with Streamlit.
- Database connection established through SQLAlchemy for seamless interaction.

### Scalable and Responsive
- Optimized to handle large datasets efficiently using indexed queries.
- 
## How to Use

### Navigating the Application

#### Select a Table:
- Use the sidebar to choose a database table (e.g., `District`, `Crime`, `FBI Code`).
- Input parameters (e.g., district number, crime type) for predefined queries.

#### Run Custom Queries:
- Navigate to the "Custom Query" page.
- Write and execute SQL queries, e.g.:
  SELECT * FROM crime WHERE district_no = 1;

### Visualizing Results
- Query results are displayed in a tabular format.
- Export results for further analysis using built-in Streamlit features.

