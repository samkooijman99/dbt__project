### Intro
Welcome to my personal dbt project regarding stocks. The goal of this project is to use as many tools from the data engineering toolkit as possible. Unfortunately, degiro has no API. Therefore, stock transactions are imported with a static csv downloadable from the degiro platform. These are hidden because of sensitive information. 

### Current tools:
- dbt
- docker
- metabase
- postgres
- using yfinance api to retrieve stock data
- github actions by checking sqlfluff

### Tools / features to come:
- terraform
- aws ec2 for hosting metabase possibly
- sandbox / production env
- airbyte

### Getting Started: 

Insert your DeGiro transactions csv in your `/seeds` folder.

Starting up your virtual env: `source env/bin/activate`

Building the docker image: `docker-compose build --no-cache`

How to fire up the docker containers: `docker compose up`

After, Metabase is available at `http://localhost:3000`

The postgres db is queryable after accessing your destination_db: `psql -h localhost -p 5433 -U postgres -d destination_db`
