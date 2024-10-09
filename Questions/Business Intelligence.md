# Business Intelligence Candidate Questions

## Previous Experience

* Describe a report or dashboard you created that directly influenced a key business decision.
* Provide an example where you addressed a challenging or complex business request, and how you ensured client satisfaction while delivering the solution.

## Third-Party Data Integration

* How do you approach the integration of third-party data providers in a BI solution? What kind of QA processes do you implement to ensure data accuracy and consistency?
* How do you handle challenges with inconsistent or unreliable third-party data sources?

## Skills and Adaptability

* How do you adapt BI solutions to evolving business needs, particularly in fast-paced or highly dynamic environments?
* Share examples of data visualization techniques that you've found most effective in communicating insights to stakeholders.
* How do you approach the balance between real-time data reporting versus batch-based reports in a modern BI environment?
* What tools have you used to automate and optimize data pipelines and BI workflows?

## General BI Concepts

### What is a Data Warehouse?

A data warehouse is a centralized repository that stores large volumes of structured data for the purpose of analytics, reporting, and decision-making. It is often used for historical data storage and supports business intelligence tools by providing a consolidated view of data from multiple sources.

### What is Data Analytics?

Data analytics is the process of analyzing raw data to extract useful insights that can inform business decisions. Modern data analytics often leverages techniques such as statistical modeling, machine learning, and data mining to generate predictions and trends.

### What are the benefits of a Data Warehouse?

A data warehouse centralizes and organizes data from multiple sources, improving reporting accuracy, consistency, and accessibility. It also supports historical analysis and trend detection by allowing for time-series data and multidimensional analysis. It enhances decision-making, increases operational efficiency, and provides a foundation for business intelligence.

### What is the difference between OLTP and OLAP?

* **OLTP (Online Transaction Processing)**: Systems optimized for transaction-oriented tasks, focusing on inserting, updating, and retrieving small amounts of data efficiently.
* **OLAP (Online Analytical Processing)**: Systems optimized for querying and reporting, focusing on retrieving large datasets to perform complex analytical queries and aggregations.

### What is a Data Mart?

A data mart is a subset of a data warehouse that is tailored to the needs of a specific business area or department, such as Finance, Marketing, or HR. Data marts allow for faster querying and reporting by focusing on a narrower scope of data.

### What is Dimensional Modeling?

Dimensional modeling is a design technique used for data warehouses and BI systems that focuses on optimizing the structure for query performance. It consists of fact tables (containing measurable, quantitative data) and dimension tables (containing descriptive, qualitative data).

### What is a Dimension?

A dimension is a descriptive attribute or set of attributes that defines the context for a fact. For example, in a sales data model, "Product," "Region," and "Time" could be dimensions.

### What is a Fact?

A fact is a quantifiable metric or measurement that is stored in a fact table in a data warehouse. Facts are typically numerical and can be aggregated, such as sales amounts, quantities, or counts.

### What is a Star Schema?

A star schema is a type of database schema used in data warehouses where a central fact table is connected to multiple dimension tables. It is called a star schema because its structure resembles a star, with the fact table at the center and dimensions radiating outward.

### What is a Snowflake Schema?

A snowflake schema is a variation of the star schema where dimension tables are normalized into multiple related tables. This increases the level of normalization in the data warehouse, often reducing redundancy but also adding complexity to querying.

### What is Data Governance, and why is it important?

Data governance refers to the management of data availability, usability, integrity, and security within an organization. It ensures that data is accurate, consistent, and compliant with regulations like GDPR or CCPA, and that the proper policies are in place for data management.

### How do you handle data security and privacy in BI solutions?

Explain your approach to securing sensitive data in a BI environment, including role-based access control, encryption, audit logging, and compliance with privacy laws. You could also discuss the use of anonymization techniques or masking sensitive data in reports.

### What is ETL, and how has modern ETL evolved?

ETL stands for Extract, Transform, and Load, and it refers to the process of extracting data from different sources, transforming it into a consistent format, and loading it into a data warehouse. Modern ETL processes have evolved to ELT (Extract, Load, Transform), where transformation happens after data is loaded into the target system, often enabling better scalability using cloud-based tools.

### What is Self-Service BI, and how do you enable it?

Self-service BI allows non-technical users to access, analyze, and visualize data without requiring technical intervention. Enabling self-service BI involves setting up user-friendly tools like Power BI, Tableau, or Looker, ensuring data accessibility, and creating intuitive, reusable data models.

---

## Advanced Concepts

### What are Additive, Semi-Additive, and Non-Additive Measures?

* **Additive**: Measures that can be summed across any dimension, such as sales or revenue.
* **Semi-Additive**: Measures that can be summed across some dimensions but not all, like account balances (which can be summed over different accounts but not over time).
* **Non-Additive**: Measures that cannot be summed, such as ratios or percentages.

### What are Slowly Changing Dimensions (SCD)?

SCD refers to dimensions that change slowly over time. Common types include:
* **Type 1**: Overwrite the old data with new data.
* **Type 2**: Create new records for changes, tracking the history.
* **Type 3**: Store both the old and new values in the same record (limited history tracking).

### What is a Conformed Dimension?

A conformed dimension is a dimension that is consistent and reusable across different fact tables or data marts in a data warehouse. For example, a "Customer" dimension could be used in both sales and marketing data marts, providing a unified view.

### What is a Fact-less Fact Table?

A fact-less fact table is a table that captures events or relationships without having a quantifiable measure. It is often used to model many-to-many relationships, such as tracking student attendance in courses or logging website activity.

---

## Visualization and Reporting

### What are some data visualization tools you have experience with, and which do you prefer?

Discuss the tools you have used (e.g., Power BI, Tableau, Looker, Google Data Studio) and why you prefer certain ones for specific types of reports, dashboards, or data sets.

### How do you ensure that your visualizations communicate insights clearly to non-technical stakeholders?

Explain your approach to designing intuitive dashboards, choosing appropriate chart types, and ensuring that visualizations are both insightful and actionable for business users.

### How do you approach performance optimization in BI tools for large datasets?

Discuss methods such as query optimization, using pre-aggregated data, caching, and using efficient data models to ensure quick performance even when working with large datasets.

---

## Cloud-Based BI and Modern Tools

### How do cloud-based BI tools (like Power BI, Google Data Studio, or Looker) differ from traditional on-prem solutions?

Discuss the advantages of cloud BI, such as scalability, real-time collaboration, automatic updates, integration with other cloud services, and the reduction of infrastructure maintenance.

### How do you implement data pipelines in cloud environments (e.g., using AWS, Azure, GCP)?

Explain your experience with cloud-native ETL/ELT tools like AWS Glue, Azure Data Factory, or Google Cloud Dataflow, and how they can be used to build scalable and reliable data pipelines for BI solutions.
