# DevSecOps Project: Netflix Clone Deployment on Kubernetes using ArgoCD

## Project Overview

This project involves deploying a Netflix clone application on a Kubernetes cluster using ArgoCD for continuous deployment. The infrastructure is set up on AWS with two EC2 instances dedicated to different roles: one for CI/CD operations using Jenkins and Docker, and another for monitoring using Prometheus, Grafana, and Node Exporter.

## Infrastructure Setup

### EC2 Instances

1. **Jenkins and Docker Instance**: 
   - **Purpose**: Handles the CI/CD pipeline.
   - **Components**: Jenkins, Docker.

2. **Monitoring Instance**:
   - **Purpose**: Monitors the performance and health of the system.
   - **Components**: Prometheus, Grafana, Node Exporter.

## CI/CD Pipeline

The Jenkins pipeline includes the following stages:

1. **Git Checkout**: Clones the Netflix clone repository.
2. **Install Dependencies**: Installs all necessary dependencies for the application.
3. **SonarQube Analysis**: Performs static code analysis to ensure code quality.
4. **OWASP Dependency Check**: Scans for vulnerabilities in project dependencies.
5. **Trivy Scan**: Conducts a security scan of Docker images.
6. **Docker Deploy and Build Images**: Builds and deploys Docker images for the application.

## Monitoring Setup

The monitoring EC2 instance runs:

1. **Prometheus**: Collects metrics from Jenkins and Node Exporter.
2. **Grafana**: Visualizes the metrics collected by Prometheus.
3. **Node Exporter**: Exposes hardware and OS metrics of the EC2 instance.

## Deployment Process

1. **ArgoCD**: Automates the deployment of the Netflix clone application on the Kubernetes cluster.
2. **Kubernetes Cluster**: Hosts the Netflix clone application, ensuring scalability and reliability.

## Project Goals

- Implement a robust CI/CD pipeline with security checks to ensure code quality and security.
- Deploy a Netflix clone application on Kubernetes using best practices.
- Set up comprehensive monitoring to maintain the health and performance of the system.

This project demonstrates the integration of DevOps and security practices (DevSecOps) in deploying a complex application, ensuring both efficiency and security throughout the development and deployment processes.


![Screenshot from 2024-07-08 14-24-27](https://github.com/AtharvaNawathe/DevSecOps---Netflix-Clone/assets/63600324/1645a093-05ab-4174-8c0f-695b40c14bdc)
![Screenshot from 2024-07-08 14-24-18](https://github.com/AtharvaNawathe/DevSecOps---Netflix-Clone/assets/63600324/68503afa-407e-4c14-8fe2-c8997cb65cea)
![Screenshot from 2024-07-08 14-24-01](https://github.com/AtharvaNawathe/DevSecOps---Netflix-Clone/assets/63600324/e8891d4b-700f-491a-be24-ac5b5ee102c3)

