# Version1:Login Page Project

## Overview

This is a simple static webpage containing a basic login form. This project uses Docker to containerize a static HTML file served by an Nginx web server.

## Project Structure

- **index.html**: The main HTML file containing the login form.
- **Dockerfile**: The Dockerfile that sets up the Nginx web server to serve the `index.html` file.

## Getting Started

You can use the Docker image provided directly from a Docker registry without cloning the repository.

### Prerequisites

- [Docker](https://www.docker.com/) installed on your local machine.

### Using the Docker Image

1. **Pull the Docker image:**
    ```bash
    docker pull krakken14/docker-web-app:version1
    ```

2. **Run the Docker container:**
    ```bash
    docker run -d -p 80:80 krakken14/docker-web-app:version1
    ```

3. **Access the webpage:**
    Open your web browser and go to [http://localhost](http://localhost:80) to access the static web page.

## Dockerfile Details

If you're interested in the Dockerfile used to create this image, here it is:

```dockerfile
FROM nginx:alpine

WORKDIR /usr/share/nginx/html

COPY . /usr/share/nginx/html

EXPOSE 80
