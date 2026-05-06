{\rtf1\ansi\ansicpg1252\cocoartf2709
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 # Phase 1 Report\
\
## Domain Description\
This project models a FIFA World Cup match tracking system. It stores data related to tournaments, stages, teams, matches, and detailed match statistics such as scoring, possession, and discipline.\
\
## Procedures and Functions\
The PL/SQL package implements key system operations:\
\
- `record_match_result` inserts match and team performance data while validating inputs and preventing duplicates.\
- `advance_team_to_stage` moves a team into a new stage by inserting a new match-team record.\
- `print_group_report` generates a summary of team performance within a group using an explicit cursor.\
\
Functions include:\
- `get_team_total_goals` calculates total goals scored by a team.\
- `get_goal_difference` computes goals scored minus goals conceded.\
- `get_discipline_score` calculates a weighted discipline score based on cards and fouls.\
\
## Design Decisions\
The schema was designed in 3NF to reduce redundancy and improve data integrity. Match statistics were split into separate tables (score, possession, defensive, etc.) to maintain a clean and normalized structure. Business logic was implemented in PL/SQL packages to separate data storage from system operations.}