# Overview

Questions and answers for backend engineer interviews.

## Questions and Model Answers

**Question 1:**

What are eventual consistency and strong consistency in distributes systems?

**Answer 1:**

**Eventual consistency** is a term used in distributed systems that refers to the idea that all replicas of data will become consistent over time.

This means that immediate consistency is not guaranteed, so users may see stale data for a period. However, eventually, the data will be synchronized across all replicas.

This model is better suited for systems that prioritize availability over real-time consistency.

In contrast, **strong consistency** ensures that all data is up to date and that every read request returns the most recent write. This type of consistency is essential in systems such as financial systems, where having accurate information is crucial to prevent issues.
It can sacrifice availability during failures because data cannot be replicate and commit in every node.

**Question 2:**

What is microservice architecture, and explain benefits and drawbacks.

**Answer 2:**

Microservices is an architectural style that implements an application as a collection of small, independent services.
The benefits of microservices include scalability, flexibility, and manageability.

Scalability means that each microservice can be scaled and deployed individually based on demand. 
Flexibility allows teams to use different technologies for different services, while manageability is enhanced because smaller services are easier to understand and maintain. 
However, it's also important to consider the added complexity and challenges in communication and infrastructure that come with a microservices architecture.

