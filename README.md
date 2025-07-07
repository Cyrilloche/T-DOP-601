# T-DOP-601 - POPEYE

## General Description

This project consists of containerizing and deploying a web polling application.
The application is composed of five components:

- ✓ Poll — a Python Flask web application that collects votes and pushes them to a Redis queue.

- ✓ Redis — a message queue that temporarily stores the votes sent by the Poll application, waiting to be processed.

- ✓ Worker — a Java application that consumes the votes from Redis and stores them in a PostgreSQL database.

- ✓ PostgreSQL — a relational database that persistently stores the votes processed by the Worker.

- ✓ Result — a Node.js web application that retrieves the votes from the database and displays them.

## Installation

### Installing Result Dependencies

Navigate to the result directory and install the Node.js dependencies:

```shell
npm install
```

### Environment Variables

Copy the .env.example file and rename it to .env.
Edit the .env file to configure your environment variables as needed.

## Running the Application

Make sure you have configured the .env file, then run the following command to start all services:

```shell
docker compose up -d
```
