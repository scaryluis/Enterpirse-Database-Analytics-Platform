{\rtf1\ansi\ansicpg1252\cocoartf2709
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 # Phase 2 Report\
\
## Star Schema Overview\
The OLTP schema was transformed into a star schema to support analytical queries. The design includes a central fact table and several dimension tables.\
\
- Fact Table: `FACT_MATCH_TEAM_PERFORMANCE`\
  - Stores one row per team per match with all performance metrics.\
- Dimension Tables:\
  - `DIM_TEAM`\
  - `DIM_MATCH`\
  - `DIM_STAGE`\
  - `DIM_DATE`\
  - `DIM_TOURNAMENT`\
\
This structure simplifies queries and improves performance for analysis.\
\
## Dimension Descriptions\
- `DIM_TEAM`: contains team information such as name, region, and group.\
- `DIM_MATCH`: stores match-level data such as date and time.\
- `DIM_STAGE`: represents tournament stages (Group Stage, Final, etc.).\
- `DIM_DATE`: provides date breakdown for time-based analysis.\
- `DIM_TOURNAMENT`: contains tournament-level details.\
\
## Sample Query Results\
Analytical queries were performed on the warehouse, including:\
- Total goals by team\
- Goals by stage using ROLLUP\
- Ranking teams by performance using RANK\
- Multi-dimensional analysis using CUBE\
\
These queries demonstrate how the star schema enables efficient aggregation and insight generation.}