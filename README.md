
# Popeye

Introduction to Docker and Docker Compose, including Docker images and containers.

## About this project

This project introduce the use of Docker to deploy a simple web app with different microservices.
The goal is to make a simple poll app work that works in any environment.
All the code needed for the microservices to work is provided, we only need to focus on Docker.

## How to use

Start all the containers with Docker Compose

```sh
docker-compose up
```

Go to `localhost:8000` to see the vote webpage and try it

## App stack

- a SQL database to store the poll results (PostgreSQL)
- a Redis worker
- a Redis client to send the requests to the worker (written in Java using Jedis)
- a Python webpage to send the votes (Flask)
- a NodeJS webpage to see the results of the poll (Express)
