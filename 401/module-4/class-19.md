# Class 19 Reading Notes

## Introduction

This reading covers the differences between AWS SQS and SNS, their use cases, and how they can be utilized in large-scale, distributed applications. It also explains the "fanout" pattern and push notifications using SNS.

## Notes

### What is the difference between SQS and SNS?

- **SQS (Simple Queue Service)**: A message queue service that allows messages to be stored and processed asynchronously by consumers.
- **SNS (Simple Notification Service)**: A pub/sub messaging service that sends messages to multiple subscribers or endpoints.

### What are some use cases for both SNS and SQS?

- **SNS Use Cases**:
  - Sending notifications to users via email, SMS, or mobile push notifications.
  - Distributing messages to multiple microservices or distributed systems.
  
- **SQS Use Cases**:
  - Decoupling and scaling microservices, distributed systems, and serverless applications.
  - Storing and processing background jobs or tasks asynchronously.

### Describe how to use SQS and SNS in a “fanout” pattern

In a "fanout" pattern, SNS is used to publish a message to a topic, and SQS queues are subscribed to this topic. When a message is published to the SNS topic, it is automatically delivered to all the subscribed SQS queues, allowing multiple systems to process the same message independently.

### Explain how “push notifications” work, using SNS

Push notifications using SNS involve creating an SNS topic and subscribing endpoints (such as mobile devices or email addresses) to this topic. When a message is published to the topic, SNS sends the message as a push notification to all the subscribed endpoints.

### How might a large scale, distributed application make use of a Queue system like SQS?

A large-scale, distributed application might use SQS to:

- Decouple components to improve fault tolerance and scalability.
- Manage and distribute workloads across multiple consumers.
- Ensure reliable message delivery and processing, even during high traffic periods or service failures.

## Reflection

### What are your learning goals after reading and reviewing the class README?

My learning goals include understanding the differences and use cases for AWS SQS and SNS, mastering the implementation of messaging patterns like "fanout," and effectively using these services to build scalable and resilient distributed applications.
