# Web Server Using Docker on Microsoft Azure
<p align="center">
  <img src="https://img.shields.io/badge/Docker-Containerized-blue?logo=docker">
  <img src="https://img.shields.io/badge/Azure-Cloud-blue?logo=microsoftazure">
  <img src="https://img.shields.io/badge/Linux-Ubuntu-orange?logo=linux">
  <img src="https://img.shields.io/badge/Nginx-Web_Server-success">
  <img src="https://img.shields.io/badge/CodeAlpha-Internship-purple">
</p>

##  
**Author**: Mabel Omolaja (maybelomolaja@gmail.com)

---

## Project Overview

This project was completed as part of the CodeAlpha DevOps Internship.

The objective was to learn Docker containerization by deploying and managing a web server inside a Docker container. To achieve this, I provisioned a Linux Virtual Machine on Microsoft Azure, installed Docker, deployed an Nginx web server container, configured network access, and hosted a custom HTML webpage accessible through a public IP address.

The project provided hands-on experience with Docker, Linux, Azure cloud infrastructure, networking, troubleshooting, and container-based application deployment.

---

## Internship Objectives

The objectives of this task were to:

* Learn Docker containerization fundamentals
* Deploy and manage a web server inside Docker containers
* Understand Docker container lifecycle and management commands
* Monitor container health and troubleshoot deployment issues
* Explore container-based application deployment best practices

---

## Architecture

```text
Internet User
      ↓
Azure Public IP
      ↓
Azure Network Security Group (NSG)
      ↓
Ubuntu Virtual Machine
      ↓
Docker Engine
      ↓
Nginx Container
      ↓
Custom HTML Website
```

---

## Technologies Used

* Microsoft Azure Virtual Machine
* Docker
* Ubuntu Linux
* Nginx
* HTML
* GitHub
* Linux Command Line (Bash)

---

## Implementation Steps

### 1. Created an Azure Virtual Machine

* Provisioned an Ubuntu Linux VM in Microsoft Azure
* Retrieved the public IP address
* Connected securely using SSH

### 2. Installed Docker

```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
```

### 3. Verified Docker Installation

```bash
docker --version
docker ps
```

### 4. Deployed an Nginx Web Server Container

```bash
docker run -d --name mywebserver -p 80:80 nginx
```

### 5. Created a Custom Website

I developed a simple HTML webpage introducing myself and describing the internship project.

### 6. Configured Azure Networking

* Added an inbound NSG rule for HTTP traffic
* Allowed TCP traffic on port 80
* Verified that the website was reachable from the internet

### 7. Tested and Validated the Deployment

Used Docker commands to confirm the container was running and verified website accessibility through the Azure VM public IP address.

---

## Docker Commands Used

### View Running Containers

```bash
docker ps
```

### View Available Images

```bash
docker images
```

### Stop a Container

```bash
docker stop mywebserver
```

### Start a Container

```bash
docker start mywebserver
```

### Remove a Container

```bash
docker rm mywebserver
```

---

## Monitoring and Troubleshooting

During the project, I encountered and resolved several issues:

### Port 80 Already Allocated

**Issue**

Docker returned an error indicating that port 80 was already in use.

**Resolution**

Identified the existing container using Docker commands and adjusted the deployment accordingly.

### Website Not Loading

**Issue**

The website could not be accessed through the public IP address.

**Resolution**

Configured Azure Network Security Group rules to allow inbound HTTP traffic on port 80.

### Default Nginx Page Displayed

**Issue**

The default Nginx welcome page appeared instead of my custom webpage.

**Resolution**

Reviewed container configuration and verified the correct HTML file was being served.

---

## What I Learned

Through this project, I gained practical experience with:

* Docker containerization concepts
* Container lifecycle management
* Linux server administration
* Microsoft Azure Virtual Machines
* Network Security Group (NSG) configuration
* Web server deployment using Nginx
* Troubleshooting deployment and networking issues
* Basic DevOps workflows and cloud operations

---

## Key Outcomes

* Successfully deployed a web server inside a Docker container
* Hosted a custom webpage on a Microsoft Azure Virtual Machine
* Configured cloud networking to enable public access
* Gained hands-on experience with Docker and Azure
* Developed practical troubleshooting and debugging skills
---

## Conclusion

This project successfully met all the objectives of the CodeAlpha Web Server Using Docker task. By deploying a containerized Nginx web server on Microsoft Azure, I gained hands-on experience with Docker, Linux administration, cloud infrastructure, networking, and troubleshooting.

The project strengthened my understanding of container-based deployments and provided a practical foundation for further learning in cloud computing and DevOps engineering.
