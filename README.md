# 3-Tier Application: Product Review System

## Overview
This repository contains a 3-tier web application, the Product Review System, where users can add products and leave reviews. The 3-tier architecture comprises a frontend, backend, and a database. The application is designed to run on AWS infrastructure with high availability and scalability in mind.

- The Frontend application provides a user interface built with HTML, CSS, and JavaScript, served by an Nginx server. 

- The Backend is a RESTful API built with Python and Flask, which processes requests, performs operations, and interfaces with a MySQL database.

- The MySQL Database stores product and review data.


Steps to for GitHub Repo:

AWS Console: create image repo in AWS ECR for each application
Terminal: docker build ... for each app
        : login to AWS account where ECR was created. Make sure you (your user or role) have permissions to push image
        : docker login ...
        : docker tag and push ... in each app folder

