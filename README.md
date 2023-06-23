# arrow-orc-parquet-clickhouse-polars
Git repo to complement the YouTube video:
ORC, Parque, Arrow
Database binaries for ELT
SQL Abstraction of files on disk or object storage
Polars as Pandas replacement

## Why?
- save money on managed cloud services like AWS Lambda, ECR, S3 (Replace Pandas for Polars)
- reduce disk I/O, faster analytics, reduce memory requirements
- simplify your tech stack (Leverage DB more for heavy lifting)
- support cross-technology data access (Arrow)

## What we'll cover:
- benefits of data storage in strongly typed columnar formats.
- Tradeoffs between Arrow, ORC, Parquet, and traditional file compression.
- Benefits to leveraging Clickhouse binaries for fast data processing and SQL abstraction.
- Benefits of Apache arrow as a serialization medium.
- Benefits of switching from Pandas to Polars for data science, analytics.

## What we'll do:
1. Use Clickhouse to create a SQL semantic layer over nested structured data
2. Use Clickhouse for fast transformation of raw data into efficient strongly typed formats
3. Use Polars as a replacement for Pandas for data science, analytics in Jupyter notebooks

## Where to got the source Data?
Download the US ASCII Daily historical file from Stooq.com, place in ./raw-data folder
https://stooq.com/db/h/
Unzip that in the ./raw-data folder

## Notes
Note: Docker-compose is setup for M1 Mac, drop/change platform to suit your hardware.

## Web UIs
Portainer for memory, cpu, I/O visualization:
http://localhost:8081
admin, M@rksP@ssword

Jypyter Notebooks:
http://localhost:8888
password: easy

## Useful Links
Polars: https://pola-rs.github.io/polars/py-polars/html/index.html
Clickhouse file table engine: https://clickhouse.com/docs/en/sql-reference/table-functions/file
Clickhouse file formats and data type conversions: https://clickhouse.com/docs/en/interfaces/formats#formats

## Adjacent topics
Other topics worth considering if this was of interest to you:
- Apache Iceberg as abstraction over data lake of file objects
    (If building a data lake with tons of ORC or Parquet objects, Iceberg creates a SQL-like abstraction over them)
- Use of DBT to build execution steps for a data pipeline
    (SQL from notebooks ran ad DBT steps, orchestrated by AirFlow, Airbytes, or Dagster)
- SQL interface in Polars using ConnectorX.
    https://pola-rs.github.io/polars/py-polars/html/reference/api/polars.read_database.html
    (Another Rust built projects for efficient zero-copy data transfer and support for tons of popular SQL engines)