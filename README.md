# ZKP gRPC client/server for authentication

## Local Run

You will need to install the rust on your machine and also the `protobuf-compiler`, for Linux:

```bash
sudo apt install protobuf-compiler
```

## Docker

You can run the program with Docker. First build the containers:

```
$ docker-compose build zkpserver
```

Run the container:

```
$ docker-compose run --rm zkpserver
```

In the remote terminal that appears run the server:

```
root@e84736012f9a:/zkp-server# cargo run --bin server --release
```

Open a new terminal on your machine and connect to the container:

```
$ docker container ls
CONTAINER ID   IMAGE                  COMMAND   CREATED          STATUS          PORTS     NAMES
e84736012f9a   zkp-course-zkpserver   "bash"    20 minutes ago   Up 20 minutes             zkp-course_zkpserver_run_b1f3fa2cd94a

$ docker exec -it e84736012f9a /bin/bash
```

Run the client:

```
root@e84736012f9a:/zkp-server# cargo run --bin client --release
```

