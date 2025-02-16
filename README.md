# Learn-Docker
One of the simplest ways to see Docker in action
One of the simplest ways to see Docker in action is by running the built-in "hello-world" image. 

1. **Install Docker:**  
   Make sure you have Docker installed on your machine. If you haven’t installed it yet, download Docker Desktop from [docker.com](https://www.docker.com/products/docker-desktop) and follow the installation instructions for your operating system.

2. **Open a Terminal or Command Prompt:**  
   Once Docker is installed and running, open your terminal (or Command Prompt on Windows).

3. **Run the Hello World Container:**  
   In the terminal, type the following command and hit enter:
   ```bash
   docker run hello-world
   ```
   This command tells Docker to run a container based on the `hello-world` image.

4. **What Happens Next?**  
   - **Docker Checks Locally:** Docker first checks if the `hello-world` image is available on your system.
   - **Image Download:** If it’s not available, Docker downloads it from Docker Hub.
   - **Container Execution:** Once downloaded, Docker runs the container, and you’ll see output that starts with "Hello from Docker!" along with some details about your Docker installation.

5. **Understanding the Output:**  
   The output confirms that your Docker installation is working correctly and that Docker is able to run containers.

### Creating Your Own Hello World with a Dockerfile

If you want to take it a step further and create your own Docker container that prints "Hello World", here’s how you can do it:

1. **Create a New Directory:**  
   Create a new directory for your project and navigate into it:
   ```bash
   mkdir hello-docker
   cd hello-docker
   ```

2. **Create a Dockerfile:**  
   Inside this directory, create a file named `Dockerfile` (without any file extension) and add the following content:
   ```dockerfile
   # Use a lightweight base image
   FROM alpine:latest
   
   # Set the command to print "Hello, World!"
   CMD ["echo", "Hello, World!"]
   ```
   This Dockerfile uses the Alpine Linux image and sets the command to run when the container starts.

3. **Build the Docker Image:**  
   In your terminal, build your Docker image using the following command:
   ```bash
   docker build -t my-hello-world .
   ```
   The `-t my-hello-world` flag tags your image with the name `my-hello-world`.

4. **Run Your Custom Docker Container:**  
   Once the image is built, run your container with:
   ```bash
   docker run my-hello-world
   ```
   You should see the output:
   ```
   Hello, World!
   ```

### Summary

- **Using `docker run hello-world`:** A quick way to verify your Docker installation.
- **Creating a custom Dockerfile:** Allows you to build and run your own containerized "Hello World" application.

Feel free to ask more questions if you need further clarification or want to explore more Docker concepts!
