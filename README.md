# Signalia

## Overview

This repository is a PoC for a framework designed to provide an enjoyable experience for both Kafka consumers and producers. The goal is to refresh core messaging concepts while delivering a modern, developer-friendly approach to building event-driven applications.

**Note:** The framework currently only contains an initial project structure (a skeleton). Development is just starting, and functionality will be added over time.

The project is split into two main parts:
- **Framework**: A set of abstractions and utilities to simplify working with Kafka, making it easier to implement robust consumer and producer logic.
- **Local Kafka Setup**: Simple instructions and configuration (see `docker-compose.yaml`) to run Kafka locally, enabling quick testing and exploration of the framework’s features.

We hope you find this project useful and inspiring as you build scalable, event-driven systems!

## Local Kafka Setup

This project provides a multi-node Apache Kafka cluster setup using Docker Compose, including a Kafka UI for management and monitoring.

### Requirements

- [Docker](https://www.docker.com/) **or** [Podman](https://podman.io/) (must be installed and running)
- [Docker Compose](https://docs.docker.com/compose/) (if using Docker)

### Services

- **controller**: Kafka controller for KRaft mode
- **broker**: Kafka broker
- **kafka-ui**: Web UI for managing and monitoring Kafka

### How to Run

1. Clone this repository.
2. Open a terminal in the project directory.
3. Start the cluster:

   ```sh
   docker compose up -d
   ```
   Or, if you are using Podman:
   ```sh
   podman compose up -d
   ```

4. Access the Kafka UI at [http://localhost:8080](http://localhost:8080).

   The UI allows you to manage topics, consumers, producers, and monitor your Kafka cluster.

### Stopping the Cluster

To stop and remove the containers:

```sh
docker compose down
```
Or with Podman:
```sh
podman compose down
```

### Notes

- The broker is accessible on port **29092** on localhost.
- Make sure Docker or Podman is running before starting the cluster.
- The Kafka UI is available at [http://localhost:8080](http://localhost:8080) after the containers are up.