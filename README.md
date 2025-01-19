**Web App Deployment to Amazon ECR**


This project demonstrates deploying a containerized web application to Amazon Elastic Container Registry (ECR) using Jenkins, Docker, SonarQube, Trivy, and AWS CLI.



**Features**

Automated CI/CD pipeline using Jenkins.
Code quality analysis with SonarQube.
Security vulnerability scanning with Trivy.
Dockerized web application.
Deployment to AWS ECR.
Tools & Technologies
Jenkins: To automate the CI/CD pipeline.
SonarQube: For static code analysis and quality gate checks.
Trivy: For security vulnerability scanning of the application.
Docker: To build and manage container images.
AWS ECR: To store and manage container images.
AWS CLI: To interact with AWS services programmatically.
CI/CD Pipeline Stages
Git Checkout:
Pull the source code from the Git repository.
SonarQube Analysis:
Analyze the source code for quality issues and enforce quality gates.
Quality Gate Check:
Halt the pipeline if the SonarQube quality gate fails.
NPM Install:
Install required Node.js dependencies.
Security Scan:
Run Trivy to scan the project for vulnerabilities.
Docker Build:
Build a Docker image of the application.
ECR Repository Management:
Create an Amazon ECR repository if it doesn’t exist.
ECR Login, Tagging, and Push:
Authenticate to ECR, tag the image with build numbers, and push it to ECR.
Cleanup:
Remove local Docker images to free up Jenkins workspace.
Prerequisites
Jenkins installed and configured with:
JDK, Node.js, and SonarQube Scanner tools.
Credentials for AWS CLI (access_keys and secret_keys).
AWS CLI configured with proper permissions.
SonarQube Server running and configured in Jenkins.
Docker installed on the Jenkins node.

**How to Run the Pipeline**

Clone this repository:
bash
Copy
Edit
git clone https://github.com/Pepuhove/Web App Deployment to Amazon ECR.git
cd wWeb App Deployment to Amazon ECR

Configure Jenkins with the provided Jenkinsfile.
Trigger the Jenkins job and monitor the pipeline stages.
Project Structure
bash
Copy
Edit


Web App Deployment to Amazon ECR/
├── Jenkinsfile         # CI/CD pipeline definition
├── Dockerfile          # Docker build instructions
├── package.json        # Node.js dependencies
├── src/                # Application source code
└── trivy-scan.txt      # Trivy scan report (generated after pipeline run)
Outcome

The web application is successfully built, scanned, and pushed to Amazon ECR as a Docker image. The image is tagged with the build number and latest.
