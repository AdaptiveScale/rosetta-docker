# Quick Start Guide for Rosetta Docker Compose Setup

## Overview
This guide will help you quickly set up and run a multi-container application using Docker Compose. The setup includes the following services:

- **rosetta-app** (Port: 8080)
- **rosetta-db (PostgreSQL)**
- **mysql** (Port: 3306)
- **postgres (PostgreSQL)** (Port: 5432)
- **mssql (SQL Server)** (Port: 1433)
- **cdap** (Port: 11011)
- **cdap-marketplace** (Port: 5000)
- **jupyter** (Port: 10000)

## Prerequisites
- Docker installed on your machine
- Docker Compose installed on your machine

## Step-by-Step Instructions

### Clone the Repository or Download the `docker-compose.yml` File ###

Ensure you have the `docker-compose.yml` file in your working directory.

### Run Docker Compose ###

Open a terminal, navigate to the directory containing the `docker-compose.yml` file, and run:
```bash
docker-compose up -d
```

### Access the Services ###

- **rosetta-app**: [http://localhost:8080](http://localhost:8080)
- **rosetta-db (PostgreSQL)**: Accessible on port 5432
- **mysql**: Accessible on port 3306
- **postgres (PostgreSQL)**: Accessible on port 5432
- **mssql (SQL Server)**: Accessible on port 1433
- **cdap**: [http://localhost:11011](http://localhost:11011)
- **cdap-marketplace**: [http://localhost:5000](http://localhost:5000)
- **jupyter**: [http://localhost:10000](http://localhost:10000)

### Default Credentials ###

Here are the default usernames and passwords for each service:

- **rosetta-app**
    - Environment variables set in `docker-compose.yml`
    - Username: `admin`
    - Password: `admin`

- **rosetta-db (PostgreSQL)**
    - Username: `postgres`
    - Password: `123456`
    - Database: `rosetta`

- **mysql**
    - Default credentials as per the `restsql/mysql-sakila` image
    - Username: `root`
    - Password: `sakila`

- **postgres (PostgreSQL)**
    - Username: `postgres`
    - Password: `sakila`

- **mssql (SQL Server)**
    - Username: `sa`
    - Password: `123abcD!`

- **cdap**
    - No default credentials required for the sandbox environment

- **cdap-marketplace**
    - No default credentials required

- **jupyter**
    - Token: When you start the container, a token is generated. Use the URL displayed in the terminal to access Jupyter Notebook.

### Stopping the Containers ###

To stop all running containers, execute:
```bash
docker-compose down
```
