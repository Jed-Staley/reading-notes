# Class 16 Reading Notes

## Introduction

This reading covers the basics of AWS EC2 instances, their use cases, the advantages of using ECS over other services, and an introduction to Elastic Beanstalk. It also explores the general differences between instance types and the concept of a compute cycle.

## Notes

### What is an EC2 Instance?

An EC2 Instance is a virtual server in Amazon's Elastic Compute Cloud (EC2) for running applications on the AWS infrastructure.

### Name 2 use cases for EC2

1. Hosting web applications and services.
2. Running scalable big data applications and analytics.

### Provide 1 reason to use ECS instead of a service such as Heroku, Digital Ocean, or Render.com

ECS allows for better integration with other AWS services, providing a more seamless and scalable environment for containerized applications.

### Where can we find EC2 on the AWS Console?

You can find EC2 in the AWS Management Console under the "Compute" section.

### Explain the general difference between T2 Micro and XL

The T2 Micro instance is a low-cost, baseline level instance with limited CPU performance, suitable for lightweight applications. In contrast, the XL instance is a high-performance instance with significantly more CPU, memory, and network resources, designed for demanding applications.

### Explain a “Compute Cycle” to a non-technical friend

A compute cycle is like the amount of work a computer does in one complete action or task. Imagine it as one spin of a wheel in a factory where each spin produces one finished product.

### What is Elastic Beanstalk?

Elastic Beanstalk is an AWS service for deploying and managing applications without worrying about the underlying infrastructure. It automatically handles the deployment, from capacity provisioning, load balancing, and auto-scaling to application health monitoring.

### Describe the relationship between EC2 and Elastic Beanstalk

Elastic Beanstalk uses EC2 instances to run the applications. It automates the process of setting up, operating, and scaling the EC2 instances required for the application.

### Name some benefits of using Elastic Beanstalk

- Simplified deployment and management.
- Automatic scaling and monitoring.
- Integration with various AWS services.
- Support for multiple programming languages and application frameworks.

## Reflection

### Looking ahead at this module’s course schedule, what do you look forward to learning?

I look forward to learning about advanced AWS services, best practices for deploying scalable applications, and how to optimize resource management for cost and performance efficiency.

### What are your learning goals after reading and reviewing the class README?

My learning goals include mastering the use of AWS EC2 for deploying and managing applications, understanding the benefits and use cases of Elastic Beanstalk, and gaining proficiency in cloud infrastructure management to build robust and scalable solutions.
