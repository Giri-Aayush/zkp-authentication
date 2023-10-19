# ZKP gRPC Client/Server for Authentication

This project implements a gRPC server and client leveraging the Zero-Knowledge Proof (ZKP) Rust library for secure authentication. The integration of ZKP with gRPC ensures that users can be authenticated without revealing sensitive information, enhancing privacy and security. gRPC, a high-performance, universal RPC framework, is employed to handle the communication between the client and server.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Local Setup](#local-setup)
  - [Installation](#installation)
  - [Running the Server and Client](#running-the-server-and-client)
- [Docker Deployment](#docker-deployment)
  - [Building the Docker Image](#building-the-docker-image)
  - [Running the Docker Container](#running-the-docker-container)
  - [Accessing the Running Container](#accessing-the-running-container)
  - [Executing the Server and Client Inside the Container](#executing-the-server-and-client-inside-the-container)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

- Rust programming language
- `protobuf-compiler`

## Local Setup

### Installation

If you're on a Linux system, you can install the required `protobuf-compiler` using the following command:

```bash
sudo apt install protobuf-compiler
```

### Running the Server and Client

TODO: Provide steps for running the server and client locally if any.

## Docker Deployment

The application can be containerized using Docker, which ensures a consistent environment for deployment.

### Building the Docker Image

To build the Docker containers, use:

```bash
docker-compose build zkpserver
```

### Running the Docker Container

Launch the container with:

```bash
Copy code
docker-compose run --rm zkpserver
```

### Accessing the Running Container

To access the running container:

1. List the active containers:

```bash
docker container ls
```

2. Connect to the desired container using its CONTAINER ID:

```bash
docker exec -it [CONTAINER ID] /bin/bash
```

### Executing the Server and Client Inside the Container

1. Start the server:

```bash
cargo run --bin server --release
```

2. In a separate terminal instance, run the client:

```bash

cargo run --bin client --release
```

## Contributing

TODO: Provide guidelines on how contributors can help with the project, if applicable.
