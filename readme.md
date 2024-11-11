# HelloWorld - JavaScript Node.js

HelloWorld is a simple Node.js application designed to demonstrate a basic "Hello, World!" setup using Docker.

## Requirements

- Docker
- Node.js and npm (optional, only if you want to run the application without Docker)

## Installation and Execution

1. Clone this repository:

    ```bash
    git clone https://github.com/yourusername/helloworld.git
    cd helloworld
    ```

2. Build the Docker image:

    ```bash
    docker build -t helloworld-js .
    ```

3. Run the Docker container:

    ```bash
    docker run -p 4000:4000 helloworld-js
    ```

The application will be available at `http://localhost:4000`.

## Dockerfile

This project includes a `Dockerfile` that performs the following actions:

- Uses the Node.js 16 base image.
- Copies all application files to the container.
- Installs Node.js dependencies using `npm install`.
- Exposes port 4000 for accessing the application.
- Runs the application with `node /src/server.js`.

## Notes

Ensure you have the `server.js` file in the `src` folder with the application code. This will set up a basic Node.js server.
