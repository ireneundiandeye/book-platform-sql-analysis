# Book Platform Market Analysis with SQL

## Overview

A startup is building a reading app aimed at book lovers and has acquired a database of books, authors, publishers, user ratings and text reviews. The goal of this project is to analyse that database with SQL to understand the market and support the design of the new product's value proposition.

All analysis is performed with SQL queries against a PostgreSQL database, run from a Jupyter notebook through SQLAlchemy and pandas.

## Data

The database contains five related tables. The `books` table holds each book's title, page count, publication date, author and publisher. The `authors` and `publishers` tables map IDs to names. The `ratings` table stores individual user ratings on a scale of 1 to 5, and the `reviews` table stores users' written reviews. The dataset covers 1,000 books.

## Questions and Findings

| Question | Result |
|---|---|
| How many books were released after 1 January 2000? | 819 books |
| How many reviews and what average rating does each book have? | Calculated for every book in the catalogue (see notebook) |
| Which publisher has released the most books longer than 50 pages? | Penguin Books, with 42 books |
| Which author has the highest average rating among books with at least 50 ratings? | [update after rerunning the corrected query] |
| How many text reviews, on average, do users who rated more than 50 books write? | About 24 reviews per user |

The results show that most of the catalogue consists of books published since 2000, that a small number of large publishers dominate full-length titles, and that the platform's most active raters are also substantial contributors of written reviews, which makes them a valuable group to engage when launching the product.

## Skills Demonstrated

This project uses multi-table joins, aggregation with `GROUP BY` and `HAVING`, subqueries for filtering on aggregated conditions, and the integration of SQL with Python for querying and presenting results.

## How to Run

Install the dependencies with `pip install -r requirements.txt`, then open `book_platform_sql_analysis.ipynb` in Jupyter. The database was provided as part of a data analytics training programme and requires connection credentials, which should be set as environment variables (`DB_USER`, `DB_PASSWORD`, `DB_HOST`, `DB_PORT`, `DB_NAME`) rather than written into the notebook.

## Tools

Python, pandas, SQLAlchemy, PostgreSQL and Jupyter Notebook.
