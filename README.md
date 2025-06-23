**Production-Grade DevSecOps Workflow for Flask App on AWS**

**Project Overview:**
Engineered and deployed a containerized Python-based Background Remover API on AWS using industry-grade DevSecOps practices and GitOps delivery.

Built a fully automated CI/CD pipeline with Jenkins, hardened the SDLC using security tools (SonarQube, Trivy, OWASP Dependency-Check, Docker Scout), 
and implemented observability using Prometheus and Grafana. Leveraged Docker and Kubernetes for orchestration and deployed to AWS EKS via Argo CD for declarative, 
version-controlled releases.

**Key Responsibilities & Technologies Used**

**1. Cloud Infrastructure Setup & Deployment (AWS, Docker & EKS)**
- Provisioned and configured AWS EC2 (Ubuntu 22.04) instances as Jenkins controllers and monitoring agents.
- Installed Docker engine for containerizing the Flask application using rembg, Flask, and Gunicorn.
- Built production-ready Docker images and pushed securely to DockerHub using Jenkins credentials.
- Created and configured an EKS Cluster using eksctl with autoscaling managed node groups for fault-tolerant deployments.
- Defined Kubernetes manifests (Deployment.yaml, Service.yaml) and exposed the app using a LoadBalancer service.
- Utilized Argo CD for GitOps-based deployment automation with version-controlled Git sync.

  
**2. Security Implementation (DevSecOps)**
-Integrated SonarQube into Jenkins for SAST (Static Application Security Testing) and enforced Quality Gates in the pipeline.
- Scanned Python dependency vulnerabilities using OWASP Dependency-Check.
- Incorporated Trivy to scan both source files and Docker images pre-deployment.
- Utilized Docker Scout for post-image build vulnerability analysis, exposure detection, and remediation insights.
- Ensured security policies were shift-lefted early in the CI stage for proactive threat mitigation.

**3.CI/CD Pipeline Automation (Jenkins)**
- Installed and configured Jenkins on the AWS EC2 instance as the CI/CD orchestrator.
- Created a declarative Jenkinsfile for automating the build, security scans, Docker image management, and deployment to EKS.
- Configured Jenkins with required tools: Docker,SonarQube Scanner, and OWASP Dependency-Check CLI.
- Integrated secure DockerHub and SonarQube credentials into Jenkins for authentication.
- Triggered Jenkins builds automatically via GitHub Webhooks on code commits.

  **4. Monitoring & Logging (Prometheus & Grafana)**
- Installed Prometheus on EC2 to collect infrastructure and application metrics.
- Deployed Node Exporter on both EC2 and EKS worker nodes to capture system-level metrics.
- Configured Prometheus scraping for Jenkins and Kubernetes endpoints.
- Integrated Grafana with Prometheus and imported dashboards for:

  ->Jenkins pipeline performance

  ->Node Exporter metrics (CPU, RAM, Disk)

  ->Kubernetes Pod health and resource usage

 **5. Kubernetes Deployment & Scaling**
- Created Kubernetes deployment and service manifests to deploy the app into EKS Pods.
- Exposed the application using LoadBalancer service for public access.
- Used Argo CD to continuously sync and deploy updates from GitHub to EKS (GitOps).
- Configured EKS-managed node groups for fault tolerance and scalability.

**6. Notification & Alerts**
- Configured Jenkins email notifications to alert on pipeline success/failure.
- Enabled Prometheus AlertManager for system-level alerting (high CPU usage, node down, etc.).
- Future-ready setup for Slack/email alert integration for proactive DevOps monitoring.


**Key Achievements**
- Successfully deployed a real-time Background Remover Flask app on AWS using a production-grade DevSecOps pipeline.
- Implemented shift-left security with early detection using SonarQube, Trivy, OWASP Dependency-Check, and Docker Scout.
- Achieved end-to-end automation for build, security validation, containerization, and deployment with Jenkins.
- Enhanced system observability using Prometheus and Grafana with prebuilt dashboards and custom metrics.
- Secured Docker registry transactions with authenticated pushes to DockerHub via Jenkins credentials.
- Ensured highly available, scalable deployments using AWS EKS with GitOps via Argo CD.
  

  **JENKINS :-**
  ![Screenshot 2025-06-23 024124](https://github.com/user-attachments/assets/aee3680f-9e3e-4282-af4f-26f544140b29)

  

 **SONARQUBE:-**
 ![Screenshot 2025-06-23 024223](https://github.com/user-attachments/assets/4d7482d4-1e1b-4c19-9388-9045723a8476)



**ARGOCD:-**
![Screenshot 2025-06-23 021657](https://github.com/user-attachments/assets/f40bf32a-f314-4503-a998-82277cb5950f)

**PREMOTHEUS :-**
![Screenshot 2025-06-23 024258](https://github.com/user-attachments/assets/b48635bf-2c6d-45b3-b008-6b308605cbf7)



**GRAFANA:-**
![Screenshot 2025-06-23 023738](https://github.com/user-attachments/assets/7633355b-5f37-4e78-a79c-a75b84b35921)


![Screenshot 2025-06-23 023630](https://github.com/user-attachments/assets/32497f8c-f925-4bc4-954f-a325536a185d)



**REAL-TIME OUTPUT – FLASK APP RUNNING ON AWS EKS (LB + AUTO-SCALING NODEGROUP)**

![Screenshot 2025-06-23 023158](https://github.com/user-attachments/assets/aae348e2-6597-4782-ae77-1ac1f3df7b86)

**Image Uploaded :-**
![Neymar](https://github.com/user-attachments/assets/1dd09b0a-32f5-4107-99d4-5ace2520daa7)

**Processed Result :-**
![image_rmbg (1)](https://github.com/user-attachments/assets/5dd9cfd2-9ba4-4366-8f31-2fa9be49298d)

  
