# 3-Tier Application: Product Review System

## Overview
This repository contains a 3-tier web application, the Product Review System, where users can add products and leave reviews. The 3-tier architecture comprises a frontend, backend, and a database. The application is designed to run on AWS infrastructure with high availability and scalability in mind.

# Application CI/CD Architecture

This repository contains a containerized, multi-tier application consisting of a Frontend, Backend, and Database. The application is built using Docker and designed to be deployed using AWS Elastic Container Registry (ECR).

---

## Application Components

### Frontend
- Built with HTML, CSS, and JavaScript
- Provides the user interface
- Served using Nginx

### Backend
- RESTful API built with Python and Flask
- Handles request processing and business logic
- Interfaces with the MySQL database

### Database
- MySQL database
- Stores product and review data

---

## Deployment Steps for GitHub Repository

### AWS Console
1. Create an ECR repository in AWS for each application (Frontend, Backend, Database).

### Local Terminal
1. Authenticate Docker with AWS ECR.
2. Build Docker images for each application.
3. Tag and push Docker images to the ECR repositories.

Ensure that:
- You are logged into the correct AWS account.
- Your AWS user or role has permissions to push images to ECR.

---

## AWS ECR Authentication

Retrieve an authentication token and authenticate your Docker client using the AWS CLI:

```bash
aws ecr get-login-password --region us-east-1 | docker login \
--username AWS \
--password-stdin 585412048804.dkr.ecr.us-east-1.amazonaws.com

