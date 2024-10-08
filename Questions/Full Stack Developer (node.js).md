# Node.js Full Stack Developer Candidate Questions

## General Experience

### Describe a project where you built a full-stack application using Node.js and a front-end framework. What challenges did you encounter, and how did you overcome them?

### How do you ensure that your full-stack application remains maintainable as it scales in complexity and user base?

---

## Data Tier

### MongoDB

- How do you design a schema in MongoDB to handle a high volume of writes and scale horizontally?
- Can you explain the difference between **embedded documents** and **referenced documents** in MongoDB? When would you use one over the other?
- What strategies do you use for optimizing queries in MongoDB, especially with large datasets?
- What are **MongoDB indexes**, and how do you determine which fields should be indexed?

### PostgreSQL

- How would you design a relational database schema in PostgreSQL for an e-commerce application with millions of customers and orders?
- What are **transactions** in PostgreSQL, and how do you ensure data integrity using them?
- Describe the purpose of **PostgreSQL's JSONB** data type. How would you use it effectively in a full-stack application?
- How do you optimize complex joins and queries in PostgreSQL? What tools or techniques do you use to identify performance bottlenecks?

### Optional: MSSQL, Redis, Neo4j

- **MSSQL**: What are some strategies for optimizing performance in MSSQL, and how would you manage large, relational datasets?
- **Redis**: When would you use Redis in your stack, and how do you handle caching strategies and expiration policies for stored data?
- **Neo4j**: Describe a use case where a graph database like Neo4j would be more beneficial than a relational database.

---

## Application Tier

### Node.js

- What are some common performance bottlenecks you have encountered in a Node.js application? How did you address them?
- Describe how you handle **asynchronous programming** in Node.js. What techniques do you use to avoid callback hell?
- How would you implement error handling in a Node.js application to ensure robustness?
- Can you explain how you would use **Event Emitters** in Node.js?

### npm and Restify (Express.js derivative)

- How do you manage package dependencies using npm to ensure that your application remains secure and up-to-date?
- What are the differences between **Restify** and **Express.js**? Why would you choose Restify over Express.js for an API server?
- How would you design a **RESTful API** using Restify to handle high traffic and ensure scalability?
- Can you explain the **middleware** concept in Restify? Provide an example of how you would write custom middleware for request validation.

---

## Front-End (User Interface) Tier

### Angular.js

- How do you structure a large Angular.js application to ensure it remains maintainable?
- Describe your approach to state management in Angular.js.
- How do you handle **data binding** in Angular.js, and how do you optimize performance for large datasets?
- What is your strategy for unit testing Angular.js components?

### Optional: dotCMS

- Have you worked with **dotCMS** or other CMS frameworks? If so, how did you integrate content management with your Node.js backend?

---

## Software Development Lifecycle

### Unit Testing

- What testing frameworks do you prefer for Node.js applications, and why? How do you ensure adequate coverage for both unit and integration tests?
- How do you mock external dependencies in your tests for a Node.js API server?
- Can you explain how you would test asynchronous code and ensure consistent test results?

### Linting and SAST

- How do you use **linting tools** like ESLint in your development process to maintain code quality?
- What is **Static Application Security Testing (SAST)**, and how do you integrate it into your Node.js development pipeline?

---

## Asynchronous Code and Distributed Systems

### Asynchronous Programming

- Explain how **Promises**, **async/await**, and **callbacks** work in Node.js. How do you decide which to use in a given scenario?
- How do you handle concurrency in Node.js when working with databases or external services?

### Distributed Systems and Microservices

- How would you design a Node.js microservice to handle high availability and fault tolerance?
- Explain how you would handle **inter-service communication** in a microservices architecture. What tools or techniques would you use (e.g., message queues, REST, gRPC)?
- How do you manage **distributed data consistency** across services? Can you explain CAP theorem in this context?

### Docker and Deployment

- How do you containerize a Node.js application using Docker? What are some best practices to ensure the container runs efficiently in production?
- How do you manage multi-container applications in Docker (e.g., Node.js app with a PostgreSQL database)?
- What tools or techniques do you use to automate deployment and ensure continuous integration in a Dockerized Node.js environment?

---

## Stream Programming and Serverless Functions

### Event-Driven and Stream Processing

- Explain the concept of **event-driven programming** and how it differs from a traditional request-response flow.
- How would you set up a **stream processing** system using Node.js and AWS Lambda to handle real-time data ingestion?
- Describe the process of integrating a **Lambda function** triggered by events from **SQS**, **SNS**, or **Kinesis**. How do you handle retries and error handling in this setup?
- What are some challenges you've faced when building a serverless architecture with Lambda functions, and how did you overcome them?

---

## Additional Questions

- What logging strategies do you implement in a Node.js microservice architecture to ensure traceability and error tracking?
- How do you handle secrets and sensitive configuration data in your Node.js application, especially in a Dockerized environment?
