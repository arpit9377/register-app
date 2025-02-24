# Real-Time Jenkins CI/CD Pipeline Using Kubernetes

## 📌 Overview
This project implements a **real-time CI/CD pipeline** using **Jenkins, Docker, Kubernetes (EKS), and ArgoCD**. The pipeline automates the process of building, testing, securing, and deploying an application on an AWS **Elastic Kubernetes Service (EKS) cluster** using GitOps principles.

## 🎯 Features
- **Automated CI/CD workflow** using Jenkins
- **Static Code Analysis** with SonarQube
- **Docker Image Build & Push** to Docker Hub
- **Security Scanning** with Trivy
- **GitOps-based Deployment** on Kubernetes using ArgoCD
- **Slack Notifications** for build and deployment updates

## 🏗️ CI/CD Pipeline Workflow

### 1️⃣ **Developer Phase**
- A developer pushes code changes to the **GitHub Repository**.

### 2️⃣ **Jenkins CI Pipeline**
- Jenkins pulls the latest code.
- The application is built using **Maven**.
- **Static Code Analysis** is performed using **SonarQube**.
- A **Docker Image** is built and pushed to **Docker Hub**.
- The Docker image is scanned for vulnerabilities using **Trivy**.

### 3️⃣ **Kubernetes Deployment with ArgoCD**
- Jenkins updates the **Kubernetes manifest files**.
- ArgoCD deploys the latest version to **AWS EKS**.
- The deployment status is monitored and updated automatically.
- **Slack Notifications** are sent upon successful deployment.

## 🚀 Tech Stack
- **CI/CD**: Jenkins
- **Containerization**: Docker
- **Code Quality**: SonarQube
- **Security Scanning**: Trivy
- **Kubernetes Deployment**: ArgoCD
- **Cloud Provider**: AWS (EKS)
- **Version Control**: GitHub
- **Notifications**: Slack

## ⚡ Challenges Faced
- **Jenkins Kubernetes Integration**: Debugging RBAC and ServiceAccount issues.
- **ArgoCD Sync Issues**: Ensuring proper GitOps workflow.
- **Docker Security Scanning**: Managing outdated vulnerability databases.
- **Webhook Delays**: Optimizing GitHub webhook triggers for Jenkins.

## 📢 Credits & Inspiration
This project was inspired by the amazing tutorial from **[Virtual TechBox by Ashfaque Ahmed Shaikh](https://www.youtube.com/@VirtualTechBox)**. Huge thanks for the guidance! 🙌

## 📜 Setup & Installation
### **Prerequisites**
Ensure you have the following installed:
- Docker
- Kubernetes CLI (kubectl)
- AWS CLI
- ArgoCD CLI
- Jenkins
- SonarQube

### **Installation Steps**
1. **Clone the Repository**
   ```sh
   git clone https://github.com/your-username/repo-name.git
   cd repo-name
   ```

2. **Set Up Jenkins & Install Plugins**
   - Install required plugins: Git, Pipeline, Docker, SonarQube Scanner, Kubernetes CLI.
   - Configure Jenkins with necessary credentials for GitHub, Docker Hub, and AWS.

3. **Configure SonarQube**
   - Set up a SonarQube server and update Jenkins to perform static code analysis.

4. **Deploy to Kubernetes**
   - Set up an **AWS EKS cluster**.
   - Apply Kubernetes manifest files with ArgoCD.
   - Sync ArgoCD with the Git repository.

5. **Run the Pipeline**
   - Trigger the Jenkins pipeline and monitor the deployment.

## 📝 Conclusion
This project showcases how **Jenkins, Kubernetes, and ArgoCD** work together in a **real-time CI/CD setup**. It provides a robust foundation for automated application deployment with **security and quality checks** in place.

If you found this useful, give it a ⭐ and feel free to contribute! 🚀

