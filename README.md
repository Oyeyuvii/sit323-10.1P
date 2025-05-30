SIT323 10.1P – Node.js Application Deployment with Docker and Kubernetes

Overview
--------
This project demonstrates the deployment of a Node.js application using Docker and Kubernetes.
It includes containerization of the application and the necessary Kubernetes configurations for deployment.

Project Structure
-----------------
- app.js: The main Node.js application file.
- Dockerfile: Contains instructions to build the Docker image for the application.
- deployment.yaml: Kubernetes Deployment configuration file.
- service.yaml: Kubernetes Service configuration file.
- .dockerignore: Specifies files and directories to ignore during Docker build.
- node_modules/: Directory containing Node.js dependencies.

Technologies Used
-----------------
- Node.js (JavaScript)
- Docker
- Kubernetes

Getting Started
---------------
1. Clone the Repository

   git clone https://github.com/Oyeyuvii/sit323-10.1P.git
   cd sit323-10.1P

2. Build the Docker Image

   docker build -t nodejs-app .

3. Deploy to Kubernetes

   kubectl apply -f deployment.yaml
   kubectl apply -f service.yaml

4. Access the Application

   Retrieve the external IP address of the service:

   kubectl get service

   Access the application via the obtained external IP.

Notes
-----
- Ensure that Docker and Kubernetes are installed and properly configured on your system.
- The node_modules directory is included, but it's recommended to run npm install to ensure all dependencies are up to date.
