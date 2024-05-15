# Scaling Websockets with Docker, Redis, HAProxy, and Node.js

This repository contains the code for a high-availability group chat application built using WebSockets, Docker, Redis, HAProxy, and Node.js. By leveraging Docker containers and the Pub-Sub architecture with Redis, this application ensures seamless bidirectional communication between clients.

## Prerequisites

Before running this application, ensure you have the following prerequisites installed:

- Node.js
- Docker
- Docker Compose

## How to Run

1. Build the Docker image:
    ```bash
    docker build -t wsapp .
    ```

2. Run the Docker containers using Docker Compose:
    ```bash
    docker-compose up
    ```

3. Open a browser console and execute the following JavaScript code to connect to the WebSocket server:
    ```javascript
    let ws = new WebSocket("ws://localhost:8080");
    ws.onmessage = message => console.log(`Received: ${message.data}`);
    ws.send("Hello! I'm a client");
    ```

4. Open multiple console windows to simulate multiple clients and observe the bidirectional communication in action.

## Technologies Used

- Docker: Containerization platform for packaging the application and its dependencies.
- Redis: In-memory data structure store used for implementing the Pub-Sub architecture.
- HAProxy: Load balancer for distributing WebSocket connections to multiple servers.
- Node.js: JavaScript runtime for executing server-side code.
- WebSocket: Protocol enabling bidirectional communication between clients and servers.

## Repository Structure

- **`src/`**: Contains the source code for the WebSocket server.
- **`docker-compose.yml`**: Configuration file for Docker Compose to orchestrate the deployment of containers.
- **`Dockerfile`**: Instructions for building the Docker image.
- **`README.md`**: Documentation providing instructions for running the application.

## References

For further details and insights into the implementation, refer to the following resources:

- GitHub Repository: [https://github.com/Mohamed-Kamal-Ayad/scaling-websockets](https://github.com/Mohamed-Kamal-Ayad/scaling-websockets)
- Video by Hussein Nasser: [Scaling Websockets - Pub/Sub, Redis, Docker, HAProxy, Node.js](https://www.youtube.com/watch?v=XgFzHXOk8IQ&ab_channel=HusseinNasser)

