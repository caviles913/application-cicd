# 3-Tier Application: Product Review System

## Overview
This repository contains a 3-tier web application, the Product Review System, where users can add products and leave reviews. The 3-tier architecture comprises a frontend, backend, and a database. The application is designed to run on AWS infrastructure with high availability and scalability in mind.

- The Frontend application provides a user interface built with HTML, CSS, and JavaScript, served by an Nginx server. 

- The Backend is a RESTful API built with Python and Flask, which processes requests, performs operations, and interfaces with a MySQL database.

- The MySQL Database stores product and review data.


Steps to for GitHub Repo:

AWS Console: create image repo in AWS ECR for each application
Terminal: docker build ... for each app
        - login to AWS account where ECR was created. Make sure you (your user or role) have permissions to push image
        - docker login ...
        - docker tag and push ... in each app folder


Commands: 

1: Retrieve an authentication token and authenticate your Docker client to your registry. Use the AWS CLI:
aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 585412048804.dkr.ecr.us-east-1.amazonaws.com
Note: If you receive an error using the AWS CLI, make sure that you have the latest version of the AWS CLI and Docker installed.

2: Build your Docker image using the following command. For information on building a Docker file from scratch see the instructions here . You can skip this step if your image is already built:
docker build -t application-cicd .

3: After the build completes, tag your image so you can push the image to this repository:
docker tag application-cicd:latest 585412048804.dkr.ecr.us-east-1.amazonaws.com/application-cicd:latest

4: Run the following command to push this image to your newly created AWS repository:
docker push 585412048804.dkr.ecr.us-east-1.amazonaws.com/application-cicd:latest
