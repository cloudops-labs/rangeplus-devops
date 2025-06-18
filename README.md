# rangeplus-devops

# RangePlus – E-Commerce Microservices Platform

This project demonstrates the DevOps automation and deployment of a 12-microservice e-commerce platform called **RangePlus**. The infrastructure is containerized using Docker and deployed on **AWS ECS (Fargate)** with automated CI/CD pipelines using Jenkins. Each service is independently deployed and versioned. MongoDB Atlas is used as the centralized managed database, and Nginx is used as a reverse proxy to route service traffic.

---

## 🧱 Microservices

- Admin
- Auth
- Common
- Communication
- Customer
- Shipment
- File
- Opensearch
- Order
- Payment
- Product
- Shipping

Each microservice has its own `Dockerfile` and `Jenkinsfile`.

---

## ⚙️ Architecture Overview

- 🐳 Docker containers for each microservice  
- 🔁 Jenkins CI/CD pipelines per service  
- 🗃 MongoDB Atlas for cloud-managed data  
- 🐙 GitHub for SCM and trigger automation  
- 🛰 ECS Fargate for container hosting  
- 🌐 Nginx reverse proxy for internal routing

---

## 🛠️ Tech Stack

| Category      | Tools                        |
|---------------|------------------------------|
| Cloud         | AWS ECS (Fargate), ECR, IAM, VPC |
| CI/CD         | Jenkins, GitHub              |
| Containers    | Docker, Nginx                |
| Database      | MongoDB Atlas                |
| Other         | Shell scripting, Linux       |

---

## 🚀 CI/CD Pipeline Flow

1. Developer pushes to GitHub
2. Jenkins pulls code, builds Docker image
3. Image is pushed to AWS ECR
4. ECS service is updated using `aws ecs update-service`
5. Nginx routes requests to updated containers

Each service uses its own Jenkins pipeline and deployment script.

---

## 📂 Repository Structure

