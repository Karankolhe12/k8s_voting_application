# AWS Adventure: Deploying a Three-Tier Web Architecture on Kubernetes

## Project Overview

Welcome to my exciting journey through Project 2 of the #90dayOfCloudOps Challenge, where I ventured into deploying a Three-Tier Web Architecture on an Amazon Web Services (AWS) Kubernetes cluster. This project has been a thrilling exploration of the world of cloud computing, guided by the expertise of my mentor, Nasiullha Chaudhari.

## Table of Contents

- [Introduction](#introduction)
- [Project Steps](#project-steps)
- [Getting Started](#getting-started)
- [GitHub Repository](#github-repository)
- [DevOps Community](#devops-community)

## Introduction

This project showcases the deployment of a Three-Tier Web Architecture on AWS using Kubernetes. It includes the following key steps:

## Project Steps

### 1. Code Acquisition
Our adventure began by obtaining the source code from a mystical GitHub repository.

### 2. Creating the EKS Cluster
To create an Amazon EKS cluster, we used the AWS Management Console, configured cluster settings, and launched worker nodes with the Amazon EBS CSI driver.

### 4. Launching the EC2 Instance
With eager anticipation, I launched the EC2 instance, laying the foundation for our magical web application and installed and configured AWS CLI and kubectl.

### 5. Creating the Stateful Manifest for Deploying MongoDB
MongoDB is deployed as a StatefulSet with 3 replicas, utilizing PersistentVolumes and PersistentVolumeClaims for durable data storage in Kubernetes.

### 6. Creating the ClusterIP Service for MongoDB Database
We created a ClusterIP service YAML manifest to expose the MongoDB StatefulSet, ensuring that it exposes the MongoDB port (default 27017).

### 7. Creating the Table in MongoDB Database
Configured a MongoDB replica set with one primary and two secondary nodes for redundancy. In the primary node, we created a database and table, ensuring data consistency across nodes.

### 8. Creating the Deployment Manifest for API
We crafted a Kubernetes Deployment for a 4-replica API, setting database connection variables and implementing a liveness probe for health monitoring.

### 9. Creating the Load Balancer Service for API
A Kubernetes Service manifest of type LoadBalancer was generated, directing it to select the API Deployment using appropriate labels.

### 10. Creating the Deployment Manifest for Web-Tier (Frontend)
A Kubernetes Deployment for a 4-replica frontend was created, setting environment variables with the API load balancer's DNS and establishing a liveness probe for health checks.

### 11. Creating the Load Balancer Service for Frontend
We crafted a Kubernetes Service manifest of type LoadBalancer to expose the frontend Deployment externally, automatically provisioning a Load Balancer.

## Getting Started

To explore and contribute to this project, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://lnkd.in/gUgfMv7G
