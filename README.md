\# Spring Boot DevOps CI/CD Pipeline



This project demonstrates a complete DevOps pipeline using Spring Boot, Docker, Jenkins, and Kubernetes.



\## Architecture



Developer → GitHub → Jenkins → Docker → DockerHub → Kubernetes



\## CI/CD Workflow



1\. Developer pushes code to GitHub

2\. Jenkins pipeline is triggered

3\. Jenkins builds the Spring Boot JAR

4\. Docker image is created

5\. Image is pushed to DockerHub

6\. Jenkins deploys application to Kubernetes

7\. Kubernetes creates Pods and exposes Service



\## Project Structure



studentapp

├── src/                  # Spring Boot source code

├── Dockerfile            # Docker image build

├── Jenkinsfile           # Jenkins CI/CD pipeline

├── k8s/

│   ├── namespace.yaml

│   ├── deployment.yml

│   ├── service.yml

│   └── hpa.yml

└── pom.xml



\## Technologies Used



\- Java 17

\- Spring Boot

\- Maven

\- Docker

\- Jenkins

\- Kubernetes (Minikube)

\- DockerHub

\- GitHub



\## Kubernetes Deployment



Deployment creates multiple pods and manages replicas.



Service exposes the application via NodePort.



HPA automatically scales pods based on CPU usage.



\## Access Application



minikube service studentapp-service -n studentapp

