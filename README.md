# Data Modeling with Apache Cassandra
This is the first project from Nanodegree Data Engineering from Udacity. The project aims to create an ETL (Extract, Transform and Load) pipeline for queries and analysis proposals in a startup called Sparkfy.

## Data
The data we use is available in two different repositories: `./event_data/` in `.csv` (Comma Separated Values) format.

## Event Data
The Event Data has the following layout:

|artist |auth     |firstName|gender|itemInSession|lastName|length   |level|location                         |method|page    |registration|sessionId|song        |status|ts         |userId|
|-------|---------|---------|------|-------------|--------|---------|-----|---------------------------------|------|--------|------------|---------|------------|------|-----------|------|
|       |Logged In|Kevin    |M     |0            |Arellano|         |free |Harrisburg-Carlisle, PA          |GET   |Home    |1.54001E+12 |514      |            |200   |1.54207E+12|66    |
|Fu     |Logged In|Kevin    |M     |1            |Arellano|280.05832|free |Harrisburg-Carlisle, PA          |PUT   |NextSong|1.54001E+12 |514      |Ja I Ty     |200   |1.54207E+12|66    |
|       |Logged In|Maia     |F     |0            |Burke   |         |free |Houston-The Woodlands-Sugar Land, TX|GET   |Home    |1.54068E+12 |510      |            |200   |1.54207E+12|51    |


It contains information about user's session in the application.

## Data Modeling
During the process 3 tables will be created by `Project_1B_ Project_Template.ipynb` Jupyter Notebook. The tables need to be modeling to fit the business need (SELECT queries) about the information we have.

## How run the project?
### Database (Apache Cassandra)
First of all we need create a Apache Cassandra instance using Docker.
It will create a container running Cassandra, which we are going to use in `Project_1B_ Project_Template.ipynb` to `CREATE`, `INSERT` and `DROP` tables.

Pull the Cassandra Docker Image:
```console
$ docker pull cassandra
```
Create a container called `db_cassandra_sparkfy`:
```console
$ docker run --name db_cassandra_sparkfy -p 9042:9042 -d cassandra
```

### Requirements
After that, clone this GIT repository into your local machine and install the requirements libraries using:
```console
$ pip install -r requirements.txt
```
