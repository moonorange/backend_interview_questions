# Overview

Questions and answers for backend engineer interviews.

## Questions and Model Answers

**Question 1:**

What is CAP theorem in distributed systems?

**Answer 1:**

The CAP theorem stands for **Consistency**, **Availability**, and **Partition Tolerance**.

- **Consistency** means that every read receives the most recent write, ensuring all replicas have up-to-date data.
- **Availability** means the system always responds to requests, even during network partitions, though the data might not always be the latest.
- **Partition Tolerance** means the system can continue to operate even if communication between parts of the system is interrupted.

The CAP theorem explains that in distributed systems, it's impossible to achieve all three components at the same time—there's always a trade-off. You can only guarantee two of the three.

For example, if you prioritize **Consistency**, the system must wait for all replicas to synchronize, meaning it might return errors or become unavailable during network partitions. On the other hand, if you prioritize **Availability**, the system will continue to respond to requests, but it may return outdated or inconsistent data because the replicas are not fully synchronized.

**Question 2:**

What are eventual consistency and strong consistency in distributes systems?

**Answer 2:**

**Eventual consistency** is a term used in distributed systems that refers to the idea that all replicas of data will become consistent over time.

This means that immediate consistency is not guaranteed, so users may see stale data for a period. However, eventually, the data will be synchronized across all replicas.

This model is better suited for systems that prioritize availability over real-time consistency.

In contrast, **strong consistency** ensures that all data is up to date and that every read request returns the most recent write. This type of consistency is essential in systems such as financial systems, where having accurate information is crucial to prevent issues.
It can sacrifice availability during failures because data cannot be replicate and commit in every node.

**Question 3 :**

What is microservice architecture, and explain benefits and drawbacks.

**Answer 3:**

Microservices is an architectural style that implements an application as a collection of small, independent services.
The benefits of microservices include scalability, flexibility, and manageability.

Scalability means that each microservice can be scaled and deployed individually based on demand.
Flexibility allows teams to use different technologies for different services, while manageability is enhanced because smaller services are easier to understand and maintain.
However, it's also important to consider the added complexity and challenges in communication and infrastructure that come with a microservices architecture.

**Question 4:**

What is the difference between SQL and NoSQL databases, and in what situations would you use one over the other?

**Answer 4:**

SQL databases, also known as relational databases, have a well-defined table structure with a strict schema. The relationships between tables are clearly defined, making them ideal for applications where ACID transactions and complex queries, such as JOINs, are needed. SQL databases are best suited for applications with structured data and clear relationships. Examples of SQL databases include MySQL and PostgreSQL.

On the other hand, NoSQL databases are schema-less, allowing for unstructured or semi-structured data. They are ideal for applications that deal with large amounts of data where the structure might evolve over time or where performance and scalability are prioritized over strict consistency. Examples include MongoDB (document-based), Cassandra (wide-column store), and Amazon DynamoDB (key-value store).

Key difference: SQL databases follow the ACID properties (Atomicity, Consistency, Isolation, Durability), while NoSQL databases tend to prioritize availability and partition tolerance.
