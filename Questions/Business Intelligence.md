# Business Intelligence Candidate Questions

## Previous experience

* Describe a report you created that led to an important decision by the report recipients?
* Provide example demonstrating your ability to address a difficult or "unreasonable" customer request.

## Third Parties

* What is your QA approach to integrating 3rd party data providers?

## Skills

* How do you adapt a BI solution to keep current with fluid business requirements?
* What are some data visualization techniques that have worked for you?

## General

### What is data warehouse?

A data warehouse is a electronic storage of an Organization's historical data for the purpose of Data Analytics, such as reporting, analysis and other knowledge discovery activities.

Other than Data Analytics, a data warehouse can also be used for the purpose of data integration, master data management etc.

According to Bill Inmon, a datawarehouse should be subject-oriented, non-volatile, integrated and time-variant. 

### What is meant by Data Analytics?

Data analytics (DA) is the science of examining raw data with the purpose of drawing conclusions about that information. A data warehouse is often built to enable Data Analytics 

### What are the benefits of a data warehouse?

A data warehouse helps to integrate data and store them historically so that we can analyze different aspects of business including, performance analysis, trend, prediction etc. over a given time frame and use the result of our analysis to improve the efficiency of business processes. 

### What is the difference between OLTP and OLAP?

* *OLTP* is the transaction system that collects business data. Whereas *OLAP* is the reporting and analysis system on that data.
* *OLTP* systems are optimized for INSERT, UPDATE operations and therefore highly normalized. On the other hand, *OLAP* systems are deliberately denormalized for fast data retrieval through SELECT operations. 

### What is data mart?

Data marts are generally designed for a single subject area. An organization may have data pertaining to different departments like Finance, HR, Marketing etc. stored in data warehouse and each department may have separate data marts. These data marts can be built on top of the data warehouse. 

### What is ER model?

ER model or entity-relationship model is a particular methodology of data modeling wherein the goal of modeling is to normalize the data by reducing redundancy. This is different than dimensional modeling where the main goal is to improve the data retrieval mechanism.

### What is dimensional modeling?

Dimensional model consists of dimension and fact tables. Fact tables store different transactional measurements and the foreign keys from dimension tables that qualifies the data. The goal of Dimensional model is not to achieve high degree of normalization but to facilitate easy and faster data retrieval.

### What is dimension?

A dimension is something that qualifies a quantity (measure). Dimensions are mutually independent. Technically speaking, a dimension is a data element that categorizes each item in a data set into non-overlapping regions. 

### What is Fact?

A fact is something that is quantifiable (Or measurable). Facts are typically (but not always) numerical values that can be aggregated. 

### What are additive, semi-additive and non-additive measures?

*Non-additive Measures*

Non-additive measures are those which can not be used inside any numeric aggregation function (e.g. SUM(), AVG() etc.). One example of non-additive fact is any kind of ratio or percentage. Example, 5% profit margin, revenue to asset ratio etc. A non-numerical data can also be a non-additive measure when that data is stored in fact tables, e.g. some kind of varchar flags in the fact table. 

*Semi Additive Measures*

Semi-additive measures are those where only a subset of aggregation function can be applied. Let’s say account balance. A sum() function on balance does not give a useful result but max() or min() balance might be useful. Consider price rate or currency rate. Sum is meaningless on rate; however, average function might be useful. 

*Additive Measures*

Additive measures can be used with any aggregation function like Sum(), Avg() etc.

### What is Star-schema?

This schema is used in data warehouse models where one centralized fact table references number of dimension tables so as the keys (primary key) from all the dimension tables flow into the fact table (as foreign key) where measures are stored. This entity-relationship diagram looks like a star, hence the name. 

*Note* Star schema provides a de-normalized design 

### What is snow-flake schema?

This is another logical arrangement of tables in dimensional modeling where a centralized fact table references number of other dimension tables; however, those dimension tables are further normalized into multiple related tables. 

*Note* Snow-flake increases degree of normalization in the design. 

### What are the different types of dimension?

In a data warehouse model, dimension can be of following types,

* Conformed Dimension
* Junk Dimension
* Degenerated Dimension
* Role Playing Dimension 

These can be further classified into

* Unchanging or static dimension (UCD)
* Slowly changing dimension (SCD)
* Rapidly changing Dimension (RCD) 

### What is a 'Conformed Dimension'?

A conformed dimension is the dimension that is shared across multiple subject area. Consider 'Customer' dimension. Both marketing and sales department may use the same customer dimension table in their reports. Similarly, a 'Time' or 'Date' dimension will be shared by different subject areas. These dimensions are conformed dimension.

Theoretically, two dimensions which are either identical or strict mathematical subsets of one another are said to be conformed. 

### What is degenerated dimension?

A degenerated dimension is a dimension that is derived from fact table and does not have its own dimension table.

A dimension key, such as transaction number, receipt number, Invoice number etc. does not have any more associated attributes and hence can not be designed as a dimension table. 

### What is junk dimension?

A junk dimension is a grouping of typically low-cardinality attributes (flags, indicators etc.) so that those can be removed from other tables and can be junked into an abstract dimension table.

These junk dimension attributes might not be related. The only purpose of this table is to store all the combinations of the dimensional attributes which you could not fit into the different dimension tables otherwise. Junk dimensions are often used to implement Rapidly Changing Dimensions in data warehouse. 

### What is a role-playing dimension?

Dimensions are often reused for multiple applications within the same database with different contextual meaning. For instance, a "Date" dimension can be used for "Date of Sale", as well as "Date of Delivery", or "Date of Hire". This is often referred to as a 'role-playing dimension' 

### What is SCD?

SCD stands for slowly changing dimension, i.e. the dimensions where data is slowly changing. These can be of many types, e.g. Type 0, Type 1, Type 2, Type 3 and Type 6, although Type 1, 2 and 3 are most common. Read this article to gather in-depth knowledge on various SCD tables. 

### What is rapidly changing dimension?

This is a dimension where data changes rapidly. Read this article to know how to implement RCD. 

### Describe different types of slowly changing Dimension (SCD)

#### Type 0:

A Type 0 dimension is where dimensional changes are not considered. This does not mean that the attributes of the dimension do not change in actual business situation. It just means that, even if the value of the attributes change, history is not kept and the table holds all the previous data.

#### Type 1:

A type 1 dimension is where history is not maintained and the table always shows the recent data. This effectively means that such dimension table is always updated with recent data whenever there is a change, and because of this update, we lose the previous values.

#### Type 2:

A type 2 dimension table tracks the historical changes by creating separate rows in the table with different surrogate keys. Consider there is a customer C1 under group G1 first and later on the customer is changed to group G2. Then there will be two separate records in dimension table like below, 

| Key | Customer | Group | Start Date | End Date    |
|-----|----------|-------|------------|-------------|
| 1   | C1       |  G1   | 1 Jan 2000 | 31 Dec 2005 |
| 2   | C1       |  G2   | 1 Jan 2006 | NULL        |

Note that separate surrogate keys are generated for the two records. NULL end date in the second row denotes that the record is the current record. Also note that, instead of start and end dates, one could also keep version number column (1, 2 … etc.) to denote different versions of the record.

#### Type 3:

A type 3 dimension stored the history in a separate column instead of separate rows. So unlike a type 2 dimension which is vertically growing, a type 3 dimension is horizontally growing. See the example below,

| Key | Customer | Previous Group | Current Group |
|-----|----------|----------------|---------------|
|  1  |    C1    |      G1        |      G2       |

This is only good when you need not store many consecutive histories and when date of change is not required to be stored. 

#### Type 6:

A type 6 dimension is a hybrid of type 1, 2 and 3 (1+2+3) which acts very similar to type 2, but only you add one extra column to denote which record is the current record.

| Key | Customer | Group | Start Date   | End Date      | Current Flag |
|-----|----------|-------|--------------|---------------|--------------|
|  1  |    C1    |  G1   | 1st Jan 2000 | 31st Dec 2005 |      N       |
|  2  |    C1    |  G2   | 1st Jan 2006 |    NULL       |      Y       |

### What is a mini dimension?

Mini dimensions can be used to handle rapidly changing dimension scenario. If a dimension has a huge number of rapidly changing attributes it is better to separate those attributes in different table called mini dimension. This is done because if the main dimension table is designed as SCD type 2, the table will soon outgrow in size and create performance issues. It is better to segregate the rapidly changing members in different table thereby keeping the main dimension table small and performing. 

### What is a fact-less-fact?

A fact table that does not contain any measure is called a fact-less fact. This table will only contain keys from different dimension tables. This is often used to resolve a many-to-many cardinality issue.

Consider a school, where a single student may be taught by many teachers and a single teacher may have many students. To model this situation in dimensional model, one might introduce a fact-less-fact table joining teacher and student keys. Such a fact table will then be able to answer queries like,

* Who are the students taught by a specific teacher.
* Which teacher teaches maximum students.
* Which student has highest number of teachers.etc. etc. 

### What is a coverage fact?

A fact-less-fact table can only answer 'optimistic' queries (positive query) but can not answer a negative query. Again consider the illustration in the above example. A fact-less fact containing the keys of tutors and students can not answer a query like below,

* Which teacher did not teach any student?
* Which student was not taught by any teacher? 

Why not? Because fact-less fact table only stores the positive scenarios (like student being taught by a tutor) but if there is a student who is not being taught by a teacher, then that student's key does not appear in this table, thereby reducing the coverage of the table.

Coverage fact table attempts to answer this - often by adding an extra flag column. Flag = 0 indicates a negative condition and flag = 1 indicates a positive condition. To understand this better, let's consider a class where there are 100 students and 5 teachers. So coverage fact table will ideally store 100 X 5 = 500 records (all combinations) and if a certain teacher is not teaching a certain student, the corresponding flag for that record will be 0.
What are incident and snapshot facts

A fact table stores some kind of measurements. Usually these measurements are stored (or captured) against a specific time and these measurements vary with respect to time. Now it might so happen that the business might not able to capture all of its measures always for every point in time. Then those unavailable measurements can be kept empty (Null) or can be filled up with the last available measurements. The first case is the example of incident fact and the second one is the example of snapshot fact.

### What is aggregation and what is the benefit of aggregation?

A data warehouse usually captures data with same degree of details as available in source. The "degree of detail" is termed as granularity. But all reporting requirements from that data warehouse do not need the same degree of details.

To understand this, let's consider an example from retail business. A certain retail chain has 500 shops accross Europe. All the shops record detail level transactions regarding the products they sale and those data are captured in a data warehouse.

Each shop manager can access the data warehouse and they can see which products are sold by whom and in what quantity on any given date. Thus the data warehouse helps the shop managers with the detail level data that can be used for inventory management, trend prediction etc.

Now think about the CEO of that retail chain. He does not really care about which certain sales girl in London sold the highest number of chopsticks or which shop is the best seller of 'brown breads'. All he is interested is, perhaps to check the percentage increase of his revenue margin across Europe. Or may be year to year sales growth on eastern Europe. Such data is aggregated in nature. Because Sales of goods in East Europe is derived by summing up the individual sales data from each shop in East Europe.

Therefore, to support different levels of data warehouse users, data aggregation is needed.

### What is slicing-dicing?

Slicing means showing the slice of a data, given a certain set of dimension (e.g. Product) and value (e.g. Brown Bread) and measures (e.g. sales).

Dicing means viewing the slice with respect to different dimensions and in different level of aggregations.

Slicing and dicing operations are part of pivoting.

### What is drill-through?

Drill through is the process of going to the detail level data from summary data.

