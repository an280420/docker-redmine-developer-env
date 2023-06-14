# docker-redmine-developer-env
Quick start redmine with developer environment.

Support Redmine 3.0-4.0 (Redmine 5. not support).

This repository contains a development environment for running Redmine in Docker. It includes a Docker Compose file and a Dockerfile to set up the necessary services and configurations.

## Prerequisites

- Docker: Install Docker on your system if you haven't already. You can find instructions [here](https://docs.docker.com/get-docker/).

## Getting Started

1. Clone this repository to your local machine:

```
git clone git@github.com:an280420/docker-redmine-developer-env.git
```
2. Navigate to the repository directory:
```
cd docker-redmine-developer-env
```

3. Customize the environment variables (if needed) in the `docker-compose.yml` file. The default configuration should work out of the box.
- Copy your plugins to ./storage/docker_redmine-plugins directory
- Copy your themes to ./storage/docker_redmine-themes directory

4. Build and run the Redmine development environment using Docker Compose:
```
docker-compose up -d
```
This will build the necessary Docker images and start the Redmine and MySQL services.

5. Access Redmine in your browser:

Open your web browser and visit `http://localhost:8080`. You should see the Redmine application.

6. Login to Redmine:

- Username: `admin`
- Password: `admin`

## Configuration

The `docker-compose.yml` file defines the services and their configurations. You can modify this file to suit your specific requirements. By default, it sets up the following services:

- `redmine`: Runs the Redmine application container with the specified volumes, ports, and environment variables.
- `db`: Runs the MySQL database container with the specified environment variables.

## Dockerfile

The included `Dockerfile` is used to build the Redmine application image. It is based on the official Redmine image and sets the environment to development mode. You can customize this file further if needed or choose a different Redmine version by uncommenting the appropriate `FROM` line.

## Contributing

Contributions to improve and enhance this development environment are welcome! If you find any issues or have suggestions, please open an issue or submit a pull request.
