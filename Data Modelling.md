# Original AdventureWorks Data
The AdventureWorks database is a comprehensive sample database designed to showcase various aspects of Microsoft SQL Server. It simulates a real-world scenario of a bicycle manufacturer called Adventure Works Cycles. The database includes several schemas representing different business areas such as Sales, Purchasing, Production, and Human Resources.

Schemas in AdventureWorks:

1. Sales: Contains data related to customer orders, sales, and special offers.
2. Purchasing: Contains data about vendors, purchase orders, and shipping methods.
3. Production: Contains data about products, manufacturing processes, and inventory.
4. Human Resources: Contains data about employees and departments.

# Fact and Dimension Tables
## Bus Matrix
![image](https://github.com/user-attachments/assets/b20cbaa2-a7a8-4903-846c-df1b4a6c80bd)

## Data Mapping
In a data warehouse, data is organized into fact tables and dimension tables. Fact tables contain quantitative data for analysis, while dimension tables contain descriptive data that provides context for the facts.

![image](https://github.com/user-attachments/assets/87ec98a2-b9e8-4cb3-a264-220e07b085c2)


# Data Warehouse Model
## Implementation
The data warehouse for AdventureWorks is implemented using SQL Server and includes the following components:

- Data Extraction: Data is extracted from the AdventureWorks OLTP database.
- Data Transformation: Data is cleaned, transformed, and normalized to fit the data warehouse schema.
- Data Loading: Transformed data is loaded into the data warehouse tables.
- Data Analysis: Business intelligence tools like Power BI are used to create dashboards and reports for data analysis.

## Data Model
After having detailed information about the DIM and FACT tables and their relationships, the next step is to build the data warehouse model. Because of the relationship between the DIM and FACT tables, it is determined that the Data warehouse model is in Galaxy Schema type.

![image](https://github.com/user-attachments/assets/801b7128-6c7f-421b-b70a-98ed7b847418)

