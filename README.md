# **Sosa-Abarka-Jilmir**

This project is a blogging platform designed to be scalable, efficient, and user-friendly. It leverages modern technologies to ensure a seamless experience for both developers and end-users. The architecture is optimized for automated deployments in Docker and AWS-based environments.

## **Key Features**

### Blogging Platform:
- Management of posts and comments.
- Support for categories and tags.
- Modular design for easy extension and customization.

### Deployment Automation:
- CI/CD setup with GitHub Actions.
- Automated deployment to AWS EC2 instances.
- Docker Compose for container orchestration.

### Containerization:
- Dockerized configuration to ensure portability.
- Scripts for building, deploying, and restarting services.

## **Technologies Used**

- **Backend:** Spring Boot (Java)  
- **Containerization:** Docker and Docker Compose  
- **Deployment:** AWS EC2 with GitHub Actions  
- **Version Control:** Git  
- **Automation:** YAML workflows for CI/CD  

## **How the Automated Deployment Works**

This project includes a workflow file (`deploy.yml`) that manages automatic deployment whenever changes are pushed to the `main` branch:

1. **Repository Check:** Ensures the server already contains the Git repository.
2. **Cloning and Updating:** If the repository is missing, it clones it. If present, it fetches and pulls the latest changes.
3. **Service Restart:** Stops the current services, rebuilds containers, and restarts the entire environment using Docker Compose.
