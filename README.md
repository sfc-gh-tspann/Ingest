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




#### Drivers

Drivers will differ based on the language, but the majority of speed is the same as HTTPS is the same.


* https://docs.snowflake.com/en/developer-guide/jdbc/jdbc

* 

