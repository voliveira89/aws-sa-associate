---
description: 'FAQ: https://aws.amazon.com/ecs/faqs/'
---

# Elastic Container Service

**Amazon’s managed EC2 container service. Allow to manage Docker containers on a cluster of EC2 instances.**

* Containers are a method of operating system virtualization that allow you to run an application and its dependencies in resource-isolated processes
* Containers are created from a read-only template called an Image
* An Image is a read-only template with instructions for creating a Docker container
* **Amazon EC2 Container Registry \(ECR\)** - AWS Docker registry service \(stores images\)
* **Taks Definitions** are text files in JSON format that describe one or more containers that form your application
* A Task Definition is required to run Docker containers in Amazon ECS
* ECS service allows to run and maintain a specified number of instances of a task definition simultaneously in a ECS cluster
* Think services like auto scaling groups for ECS
* ECS cluster is a logical grouping of container instances that you can place tasks on

