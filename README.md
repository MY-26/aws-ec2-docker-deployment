# aws-ec2-docker-deployment
Deploying a Dockerized Nginx web application on AWS EC2 Ubuntu with CloudWatch monitoring.
# AWS EC2 Docker Application Deployment

## Project Overview
This project demonstrates deploying a containerized Nginx web application on an AWS EC2 Ubuntu Linux instance using Docker.

## Architecture
User Browser -> AWS Security Group -> EC2 Ubuntu -> Docker Container -> Nginx Web Server

## Technologies Used
- AWS EC2
- Ubuntu Linux
- Docker
- Nginx
- AWS Security Groups
- Amazon CloudWatch
- Git and GitHub

## Implementation Steps
1. Launched an Ubuntu EC2 instance.
2. Configured SSH and HTTP security group rules.
3. Connected to the instance using SSH.
4. Installed Docker Engine.
5. Created a custom HTML web application.
6. Created a Dockerfile using the Nginx Alpine image.
7. Built a Docker image.
8. Deployed the application as a running container.
9. Verified application access through the EC2 public IP.
10. Reviewed EC2 monitoring metrics in CloudWatch.

## Docker Commands
```bash
sudo docker build -t mansi-cloud-demo:v1 .
sudo docker run -d --name mansi-webapp --restart unless-stopped -p 80:80 mansi-cloud-demo:v1
sudo docker ps
sudo docker logs mansi-webapp
```

## Monitoring
Reviewed EC2 CPU utilization, network traffic and instance status checks through CloudWatch basic monitoring.

## Learning Outcomes
- AWS EC2 provisioning
- Linux server administration
- Docker image creation and container deployment
- Network security group configuration
- Basic cloud infrastructure monitoring
- Application troubleshooting

## Cleanup
Terminate the EC2 instance and verify that unused EBS volumes and other billable resources have been removed.

## Author
Mansi Yeole
