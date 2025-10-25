DevOps Task: Dockerized Flask App with Nginx Reverse Proxy and CI/CD Pipeline :
  - This file documents the setup, build, and usage instructions for a Flask application
    containerized with Docker, served behind an Nginx Reverse Proxy, managed by Docker Compose,
    and automated with a GitHub Actions CI/CD pipeline.

1. Project Overview and Setup
- Prerequisites:
 - Git: For cloning the repository
 - Docker: Docker Engine and Docker Compose .

3. Build and Run Instructions :
  - Cloning the Repository :
   ```bash
git clone https://github.com/maiekel-eltawab/flask-task.git

   ```

3. Building and Launching Services (Docker Compose):

Using the docker-compose.yml file, you can build Docker images and launch both the Flask and Nginx services with a single command:
   ```bash
docker compose up --build -d
   ```
Actions Performed:

 - Builds the Flask application image (using app/Dockerfile).

 - Builds the Nginx image (using the nginx.conf configuration file).

 - Runs both containers and connects them on an internal network.

 - Verification: After completion, you can check the status of the services: docker compose ps

4. Usage and Access:
  The application is accessed via the Nginx Reverse Proxy on port 80:
   Access the Application: Open your browser and navigate to the following address:
    ```bash
    http://localhost
    ```
    <img width="961" height="564" alt="Screenshot 2025-10-25 023718" src="https://github.com/user-attachments/assets/0318414c-d64b-472d-825e-77da67d6f960" />
    <img width="1274" height="661" alt="Screenshot 2025-10-25 035807" src="https://github.com/user-attachments/assets/2ba8e19a-d6f1-4cf1-98b3-d5a93c4adf17" />


     To Stop Services:
     ```bash
      docker compose down
     ```
5.  CI/CD Pipeline (GitHub Actions):
  
  - The main.yml: file is responsible for automating the build and push process for every code modification:

  - Automation: The workflow is triggered automatically upon code push.

  - Build and Push: It builds the Docker image for the application and then pushes it to the Docker Hub repository (maiekel259041/flask)
    
   <img width="1321" height="624" alt="Screenshot 2025-10-25 033738" src="https://github.com/user-attachments/assets/eda1be16-98a0-4668-b4fa-d3c40d00336b" />





