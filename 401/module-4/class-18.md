# Class 18 Reading Notes

## Introduction

This reading covers the essentials of Amazon API Gateway and DynamoDB, their use cases, and benefits within the AWS ecosystem. It also introduces Dynamoose as a modeling tool for DynamoDB.

## Notes

### What is Amazon API Gateway?

Amazon API Gateway is a managed service that allows developers to create, publish, maintain, monitor, and secure APIs at any scale.

### Why is Amazon API Gateway an important part of the Serverless ecosystem?

Amazon API Gateway is crucial in the Serverless ecosystem because it allows developers to create RESTful and WebSocket APIs that can trigger AWS Lambda functions, enabling fully serverless architectures without the need to manage any infrastructure.

### How does API Gateway integrate with other AWS services?

API Gateway integrates with various AWS services such as Lambda for executing backend code, IAM for access control, CloudWatch for monitoring, and DynamoDB for data storage.

### What are some benefits of using Amazon API Gateway?

- Simplified API management and deployment.
- Scalability to handle any number of API requests.
- Security features like authorization and throttling.
- Monitoring and logging through CloudWatch.

### What two API types might you choose from?

1. RESTful APIs
2. WebSocket APIs

### What is DynamoDB?

DynamoDB is a fully managed NoSQL database service provided by AWS that offers high performance, scalability, and reliability.

### Under what circumstances would you recommend DynamoDB over MongoDB?

DynamoDB is recommended over MongoDB when you need seamless integration with other AWS services, require high availability and scalability with minimal management, and prefer a fully managed service with built-in security and backup features.

### Explain to a non-technical friend how DynamoDB works

DynamoDB works like a giant digital filing cabinet where you can store and retrieve information quickly. It's designed to handle lots of data and many users at once, automatically managing everything behind the scenes to keep it fast and reliable.

### What is Dynamoose?

Dynamoose is a modeling tool for DynamoDB that provides a simple and consistent way to interact with DynamoDB, similar to how ORM (Object-Relational Mapping) tools work with SQL databases.

### What are some key features of Dynamoose?

- Schema-based data modeling.
- High-level API for interacting with DynamoDB.
- Support for validation, middleware, and hooks.
- Easy integration with existing Node.js applications.

## Reflection

### What are your learning goals after reading and reviewing the class README?

My learning goals include mastering the use of Amazon API Gateway for creating and managing APIs, understanding the capabilities and use cases of DynamoDB, and leveraging Dynamoose for efficient data modeling in serverless applications.
