{\rtf1\ansi\ansicpg1252\cocoartf2709
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 # Phase 3 Report\
\
## Cross-Platform Comparison\
In this phase, the same analytical queries were implemented in Oracle SQL, Spark SQL, and PySpark. Oracle SQL and Spark SQL have very similar syntax, but Spark runs on a distributed system, allowing it to handle larger datasets. PySpark differs by using a DataFrame API instead of SQL, which makes it more flexible for building custom logic such as the matchup difficulty analysis.\
\
## Scalability Discussion\
As data size increases, traditional databases like Oracle may struggle because they operate on a single machine. Spark is designed for distributed processing, meaning it can split data across multiple nodes and process it in parallel. This allows Spark to efficiently handle very large datasets, such as millions or billions of rows.\
\
## What I Learned\
This project demonstrated how data flows from transactional systems (OLTP) to analytical systems (data warehouse) and then to scalable processing platforms like Spark. It also showed the differences between SQL-based analysis and programmatic analysis using PySpark.}
