# Analytics Data Storage

Over the past 40 years, businesses have had a common problem- the data trying to create analytics information off raw application data doesn't work well. The format isn't ideal for analytics tools, and analytics workloads can cause spikes in performance for critical applications, and the data for a single report could come from many different sources. AI has worsened the issue since it needs another type of data formatting and access. The primary solution has been to copy the data into a separate storage solution better suited to analytics and AI needs.

## Data Warehouses

Data warehouses are large, centralized repositories for storing, managing, and analyzing vast amounts of structured data from various sources. They are designed to support efficient querying and reporting, providing businesses with crucial insights for informed decision-making. Data warehouses utilize a schema-based design, often employing star or snowflake schemas, which organize data in tables related by keys. They are usually built using SQL engines. Small data warehouses can easily be created on the same software as applications, but specialized SQL engines like Amazon Redshift, Google BigQuery, and Snowflake are designed to handle analytics data on a much larger scale.

The main goal of a data warehouse is to support Online Analytical Processing (OLAP), allowing users to perform multidimensional data analysis, exploring it from different perspectives and dimensions. The primary issue with this format is that they aren't well suited for machine learning applications because the data access options don't work with machine learning tools at scale.

### Star Schemas

Star and snowflake schemas are similar- a snowflake schema is essentially a star schema that allows for additional complexity. The name comes from the fact that diagrams of the various tables and their connections look like stars and snowflakes.

Data is divided into two types of tables: fact tables and dimensions. Dimension tables contain all the data common across events. For a specific sale at a retailer, there might be tables for customer information, the sale date, the order status, and the products sold. Those would be linked to a single fact table containing data specific to that sale, like the purchase and retail prices.

## Data Lakes

Data warehouses had three main failings that required the creation of data lakes.

1. The data isn't easily accessible for ML tools.
2. Data Warehouses don't handle unstructured data like images and audio very well.
3. Data storage costs are much higher than what would become data lakes.

Data lakes are usually built on top of an implementation of HDFS or a Hadoop Distributed File System. Previous file storage options had limits on how much data they could store, and large companies were starting to exceed those limits. HDFS effectively removes those limits since existing technology can handle data storage at a significantly larger scale than any current data lake requirements, and it is possible to expand this in the future.

Data warehouses are considered "schema on write," where the data is organized into tables before it is written to storage. Data lakes are stored in files that are primarily "schema on read" where the data may only be partially structured in the loading process and transformations are applied when a system goes to read the data.

Data lakes are often structured in layers. The first layer is the data in its original, raw format. The following layers will have increasing levels of structure. For example, an image might be in its raw form in the first layer, but later layers may have information about the image instead. The new file might have the image's metadata, a link to the original image, and an AI-generated description of what it contains.

Data lakes solved the scale problem and are more useful for machine learning, but they didn't have the same quality controls over that data that warehouses do, and "schema on read" creates significant performance problems. For the past decade, companies have maintained a complex ecosystem of data lakes, warehouses, and real-time analytics engines like Kafka. This supports analytics and ML, but creating, maintaining, and processing data is exceptionally time-consuming with many systems involved.

## Data Lakehouse

Data Lakehouse is an emerging style of data storage that attempts to combine the benefits of both data lakes and data warehouses. The foundation of a lakehouse is a data lake to support the exabytes of data that data lakes can currently contain.

The first innovation in this direction is technologies like delta lake, which combines Apache Spark for data processing with parquet file formats to create data lake layers that support transactions and data quality controls while maintaining a compact data format. This tool is ideal for ML uses since it solves the data quality problems of data lakes and the data access problems from data warehouses. Current work focuses on allowing a lakehouse to provide more effective analytics data with tools like caching and indexes.

<https://www.ibm.com/topics/data-lakehouse#:~:text=A%20data%20lakehouse%20typically%20consists,architectural%20pattern%20of%20data%20lakehouses.>
