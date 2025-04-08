### Snowflake connection methods (REST, Python, JDBC, ODBC)  and Uses

General Best Practices
[https://www.snowflake.com/en/blog/best-practices-for-data-ingestion/](https://www.snowflake.com/en/blog/best-practices-for-data-ingestion/)

Snowpipe Streaming
[https://www.snowflake.com/en/blog/data-ingestion-best-practices-part-three/](https://www.snowflake.com/en/blog/data-ingestion-best-practices-part-three/)

Snowflake Connector for Apache Kafka
[https://www.snowflake.com/en/blog/best-practices-for-data-ingestion-part-2/](https://www.snowflake.com/en/blog/best-practices-for-data-ingestion-part-2/)


All data going over HTTPS all more or less perform at similar rate limits.


Single Thread -> Single Connection -> Single Snowflake account -> per warehouse-> ~60 queries per second


Fastest Way to Send Data to Snowflake

* PUT INTO a Stage
* COPY INTO a Table

[https://www.snowflake.com/en/blog/best-practices-for-data-ingestion/](https://www.snowflake.com/en/blog/best-practices-for-data-ingestion/)


DevOps / Administration / Automation

* REST API - for DDL, administration, monitoring, management

[https://docs.snowflake.com/en/developer-guide/snowflake-rest-api/snowflake-rest-api](https://docs.snowflake.com/en/developer-guide/snowflake-rest-api/snowflake-rest-api)

* SQL REST API - for adminstration, kick off stored procedures, do not use for ingest.

[https://docs.snowflake.com/en/developer-guide/sql-api/index ](https://docs.snowflake.com/en/developer-guide/sql-api/index )

Good use for REST API is to trigger Snowpipe to read files from stages.

![image](https://github.com/user-attachments/assets/2fab2b44-4787-4f45-8d3b-11a08aff52b9)


#### Check Your Network Speed

https://docs.snowflake.com/en/user-guide/snowcd



#### Drivers

Drivers will differ based on the language, but the majority of speed is the same as HTTPS is the same.

https://docs.snowflake.com/en/developer-guide/driver-connections



* https://docs.snowflake.com/en/developer-guide/jdbc/jdbc

* https://docs.snowflake.com/en/developer-guide/golang/go-driver
  
* https://docs.snowflake.com/en/developer-guide/dotnet/dotnet-driver

* https://docs.snowflake.com/en/developer-guide/node-js/nodejs-driver
  
* https://docs.snowflake.com/en/developer-guide/odbc/odbc

* https://docs.snowflake.com/en/developer-guide/php-pdo/php-pdo-driver

* https://docs.snowflake.com/en/developer-guide/python-connector/python-connector


**Download your tools**

https://docs.snowflake.com/en/user-guide/snowflake-client-repository



#### Libraries -- Snowpark 

* https://quickstarts.snowflake.com/guide/data_engineering_pipelines_with_snowpark_python/index.html#0
  
* https://docs.snowflake.com/en/developer-guide/snowpark/java/index

* https://docs.snowflake.com/en/developer-guide/snowpark/scala/index

  

#### Libraries -- Snowflake Native App

* https://docs.snowflake.com/en/developer-guide/native-apps/native-apps-about



#### Libraries -- External Functions

* https://docs.snowflake.com/en/sql-reference/external-functions

  

#### Libraries -- Apache Spark, Apache Flink, Apache NiFi


* https://docs.snowflake.com/en/user-guide/spark-connector-overview
  
* https://github.com/deltastreaminc/flink-connector-snowflake
  
* Apache NiFi via JDBC, Cloudera custom processor, Snowflake custom processor



#### Suggestions

For fast data ingestion into Snowflake, using Snowpipe with gzipped CSV files (or other compressed formats) is generally considered the fastest and most efficient method, especially for batch loading. 

* https://www.snowflake.com/content/snowflake-site/global/en/blog/how-to-load-terabytes-into-snowflake-speeds-feeds-and-techniques.html
* https://www.snowflake.com/en/engineering-blog/loading-terabytes-into-snowflake-speeds-feeds-techniques/
* https://www.snowflake.com/en/solutions/data-ingestion/
* https://quickstarts.snowflake.com/guide/CDC_SnowpipeStreaming_DynamicTables/
* https://quickstarts.snowflake.com/guide/connectors_github_python/
* https://estuary.dev/blog/snowflake-data-ingestion/
* https://quickstarts.snowflake.com/guide/a_comprehensive_guide_to_ingesting_data_into_snowflake/index.html#11
* https://select.dev/posts/snowflake-data-loading-overview

  
