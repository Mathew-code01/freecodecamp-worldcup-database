# World Cup Database Project

## Overview
This project is a relational database solution designed to organize and analyze FIFA World Cup tournament data. It features a custom-built PostgreSQL schema, automated data ingestion via Shell scripting, and a suite of analytical queries to extract tournament statistics.

This project was completed as part of the freeCodeCamp Relational Database Certification.

## Technical Stack
- **Database:** PostgreSQL
- **Automation:** Bash Scripting (Shell)
- **Data Ingestion:** CSV-to-SQL pipeline
- **Tools:** `psql`, `pg_dump`

## Project Structure
- `worldcup.sql`: A comprehensive SQL dump of the production database schema and populated data.
- `insert_data.sh`: A robust automation script that parses `games.csv`, handles relational team mappings, and populates the database while maintaining data integrity.
- `queries.sh`: A suite of analytical scripts that perform complex joins, aggregations, and filtering to generate tournament insights.

## Key Features
- **Relational Schema:** Efficiently normalized `teams` and `games` tables with Foreign Key constraints to prevent data redundancy.
- **Automated Ingestion:** The `insert_data.sh` script dynamically identifies unique teams and generates valid relational IDs, ensuring zero hard-coded entries.
- **Analytical Insights:** Executes precise SQL queries to extract data such as:
    - Tournament champions and year-over-year performance.
    - Aggregated scoring statistics (sum and averages).
    - Team-specific round analysis.

## Usage
To restore the database from the provided dump:
```bash
psql -U <username> -d worldcup < worldcup.sql
