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
- Docker (for containerized deployment)

## Local Setup

### Installation

1. Ensure you have Rust installed on your system. If not, you can download and install Rust from the official website: https://www.rust-lang.org/tools/install

2. Install the required `protobuf-compiler`. On Linux systems, you can use the following command:
      ```bash
      sudo apt install protobuf-compiler
      ```

### Running the Server and Client

1. Clone the project repository:
    ```bash
    git clone https://github.com/your-username/zkp-grpc-authentication.git
    ```

2. Navigate to the project directory:
      ```bash
      cd zkp-grpc-authentication
      ```

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

3. Build the project:

      ```bash
      cargo build --release
      ```
4. Start the server:

    ```bash
    cargo run --bin server --release
    ```
5. In a separate terminal instance, run the client:

    ```bash
    cargo run --bin client --release
    ```
6. Follow the prompts to enter the username and password (in hexadecimal format).

7. Use the provided password to log in and obtain the session ID.

## Docker Deployment
1. Building the Docker Image
To build the Docker image, use the following command:

    ```bash
    docker-compose build zkpserver
    ```
2. Running the Docker Container
Launch the Docker container with the following command:

    ```bash
    docker-compose run --rm zkpserver
    ```
3. Accessing the Running Container
List the active containers:

    ```bash
    docker container ls
    ```
4. Connect to the desired container using its CONTAINER ID:

    ```bash
    docker exec -it [CONTAINER ID] /bin/bash
    ```
5. Executing the Server and Client Inside the Container
Start the server:
    ```bash
    cargo run --bin server --release
    ```
6. In a separate terminal instance, run the client:
    ```bash
    cargo run --bin client --release
    ```
7. Follow the prompts to enter the username and password (in hexadecimal format).

8. Use the provided password to log in and obtain the session ID.

## Contributing
We welcome contributions to enhance the functionality and usability of this project. If you'd like to contribute, please follow these steps:

Fork the repository.
1. Create a new branch for your feature or bug fix.
2. Make your changes and commit them with descriptive commit messages.
3. Push your changes to your forked repository.
4. Submit a pull request to the main repository, clearly describing your changes and their benefits.
