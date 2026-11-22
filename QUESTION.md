

## **Level 3 – Asynchronous Node.js**

### **10. Asynchronous Programming**

- 10.1 What is synchronous execution?
- 10.2 What is asynchronous execution?
- 10.3 What is blocking I/O?
- 10.4 What is non-blocking I/O?
- 10.5 What is callback-based programming?
- 10.6 What is callback hell?
- 10.7 What is a Promise?
- 10.8 What are Promise states?
- 10.9 What is Promise chaining?
- 10.10 What is `async/await`?
- 10.11 What is the difference between callbacks and Promises?
- 10.12 What is the difference between Promise and async/await?
- 10.13 What is `Promise.all()`?
- 10.14 What is `Promise.allSettled()`?
- 10.15 What is `Promise.race()`?
- 10.16 What is `Promise.any()`?
- 10.17 How do you handle asynchronous errors?
- 10.18 What happens if you forget to use `await`?
- 10.19 How do you execute multiple operations sequentially?
- 10.20 How do you execute multiple operations in parallel?

### **11. Event Loop and Thread Pool**

- 11.1 What is the Node.js event loop?
- 11.2 How does the event loop work?
- 11.3 What is the call stack?
- 11.4 What is the callback queue?
- 11.5 What is the microtask queue?
- 11.6 What is the timers phase?
- 11.7 What is the poll phase?
- 11.8 What is the check phase?
- 11.9 What is the close callbacks phase?
- 11.10 What is libuv?
- 11.11 What is the libuv thread pool?
- 11.12 What is the default thread pool size?
- 11.13 What is `process.nextTick()`?
- 11.14 What is the difference between `process.nextTick()` and Promise callbacks?
- 11.15 Which operations use the thread pool?
- 11.16 Does every asynchronous operation use the thread pool?
- 11.17 How can CPU-intensive operations block the event loop?
- 11.18 How do you prevent event loop blocking?


### **12. Error Handling in Node.js**

- 12.1 What are errors in Node.js?
- 12.2 What is a synchronous error?
- 12.3 What is an asynchronous error?
- 12.4 What is `try...catch`?
- 12.5 What is `throw new Error()`?
- 12.6 What is a custom error class?
- 12.7 What is an operational error?
- 12.8 What is a programming error?
- 12.9 What is `uncaughtException`?
- 12.10 What is `unhandledRejection`?
- 12.11 What is the difference between `throw` and `next(err)` in Express?
- 12.12 How do you create a centralized error handler?
- 12.13 How do you log application errors?
- 12.14 How should an application handle unexpected fatal errors?
- 12.15 Why should an application not continue blindly after an uncaught exception?

## **Level 4 – Express.js Backend Development**

### **13. Express.js Fundamentals**

- 13.1 What is Express.js?
- 13.2 Why do we use Express with Node.js?
- 13.3 What is the difference between Node.js and Express.js?
- 13.4 How do you install Express?
- 13.5 How do you create an Express server?
- 13.6 What is `app.listen()`?
- 13.7 What is routing?
- 13.8 What is `app.get()`?
- 13.9 What is `app.post()`?
- 13.10 What is `app.put()`?
- 13.11 What is `app.patch()`?
- 13.12 What is `app.delete()`?
- 13.13 What is `req.params`?
- 13.14 What is `req.query`?
- 13.15 What is `req.body`?
- 13.16 What is `req.headers`?
- 13.17 What is `res.json()`?
- 13.18 What is `res.send()`?
- 13.19 What is `res.status()`?
- 13.20 What is the difference between `res.send()` and `res.json()`?
- 13.21 What is route chaining?
- 13.22 What is `express.Router()`?
- 13.23 What is route modularization?
- 13.24 What is a REST API?
- 13.25 What are REST API best practices?

### **14. Express Middleware**

- 14.1 What is middleware?
- 14.2 Why do we use middleware?
- 14.3 How does middleware work?
- 14.4 What are the parameters of middleware?
- 14.5 What is `next()`?
- 14.6 What happens if we don't call `next()` or send a response?
- 14.7 What is application-level middleware?
- 14.8 What is router-level middleware?
- 14.9 What is built-in middleware?
- 14.10 What is third-party middleware?
- 14.11 What is error-handling middleware?
- 14.12 What is the difference between middleware and controller?
- 14.13 What is middleware execution order?
- 14.14 How do you create authentication middleware?
- 14.15 How do you create role-based authorization middleware?
- 14.16 How do you handle async middleware errors?
- 14.17 What is `express.json()`?
- 14.18 What is `express.urlencoded()`?
- 14.19 What is CORS middleware?
- 14.20 What is Helmet?

**Coding practice:**

- Create request logging middleware.
- Create JWT authentication middleware.
- Create admin authorization middleware.
- Create request validation middleware.
- Create centralized error middleware.

### **15. Node.js Project Architecture**

- 15.1 How should we structure a Node.js project?
- 15.2 What is MVC architecture?
- 15.3 What is the Model layer?
- 15.4 What is the View layer?
- 15.5 What is the Controller layer?
- 15.6 What is the Service layer?
- 15.7 What is the Repository pattern?
- 15.8 What is the difference between controller and service?
- 15.9 What is the difference between service and repository?
- 15.10 Why should we separate business logic from controllers?
- 15.11 What is dependency injection?
- 15.12 What is a reusable utility function?
- 15.13 What is configuration management?
- 15.14 How do you manage environment variables?
- 15.15 What is the purpose of a centralized database connection?
- 15.16 How do you handle multiple environments (development, staging, production)?
- 15.17 How do you organize routes, controllers, services, models, and middleware?
- 15.18 What is a monolithic architecture?
- 15.19 What is a modular monolith?
- 15.20 What is clean architecture?


### **16. Authentication and Authorization**

- 16.1 What is authentication?
- 16.2 What is authorization?
- 16.3 What is the difference between authentication and authorization?
- 16.4 What is JWT?
- 16.5 What are the three parts of JWT?
- 16.6 What is a JWT payload?
- 16.7 What is a JWT signature?
- 16.8 What is `jwt.sign()`?
- 16.9 What is `jwt.verify()`?
- 16.10 What is `jwt.decode()`?
- 16.11 What is the difference between verify and decode?
- 16.12 What is an access token?
- 16.13 What is a refresh token?
- 16.14 What is the difference between access and refresh tokens?
- 16.15 What is token expiration?
- 16.16 How do you implement token refresh?
- 16.17 What is role-based access control (RBAC)?
- 16.18 What is permission-based access control?
- 16.19 How do you protect private APIs?
- 16.20 Where should authentication tokens be stored?
- 16.21 What is an HttpOnly cookie?
- 16.22 What are Secure and SameSite cookie attributes?
- 16.23 What is session-based authentication?
- 16.24 What is the difference between JWT and session authentication?
- 16.25 How do you implement logout and token revocation?

### **17. Database Integration**

- 17.1 How do you connect Node.js with MongoDB?
- 17.2 What is Mongoose?
- 17.3 What is a schema?
- 17.4 What is a model?
- 17.5 What is a document?
- 17.6 What is CRUD?
- 17.7 What is `find()`?
- 17.8 What is `findOne()`?
- 17.9 What is `findById()`?
- 17.10 What is `create()`?
- 17.11 What is `save()`?
- 17.12 What is `updateOne()`?
- 17.13 What is `findByIdAndUpdate()`?
- 17.14 What is `deleteOne()`?
- 17.15 What is `findByIdAndDelete()`?
- 17.16 What is MongoDB aggregation?
- 17.17 What is `$match`?
- 17.18 What is `$group`?
- 17.19 What is `$lookup`?
- 17.20 What is population in Mongoose?
- 17.21 What is indexing?
- 17.22 What is the difference between SQL and NoSQL?
- 17.23 What is database connection pooling?
- 17.24 What is a database transaction?
- 17.25 How do you handle database connection failures?

### **18. API Validation and Security**

- 18.1 What is request validation?
- 18.2 Why should we validate incoming API data?
- 18.3 What is Joi?
- 18.4 What is Zod?
- 18.5 What is the difference between Joi and Zod?
- 18.6 What is sanitization?
- 18.7 What is CORS?
- 18.8 What is XSS?
- 18.9 What is CSRF?
- 18.10 What is SQL injection?
- 18.11 What is NoSQL injection?
- 18.12 What is rate limiting?
- 18.13 What is Helmet?
- 18.14 What is password hashing?
- 18.15 What is bcrypt?
- 18.16 What is the difference between hashing and encryption?
- 18.17 Why should passwords never be stored as plain text?
- 18.18 What is HTTPS?
- 18.19 How do you protect sensitive environment variables?
- 18.20 How do you validate uploaded files?
- 18.21 What is request size limiting?
- 18.22 How do you prevent brute-force login attempts?

## **Level 5 – Advanced Node.js Development**

### **19. Performance and Scalability**

- 19.1 What is Node.js performance optimization?
- 19.2 What is clustering?
- 19.3 What is the Node.js Cluster module?
- 19.4 What are worker threads?
- 19.5 What is the difference between Cluster and Worker Threads?
- 19.6 What is child process?
- 19.7 What is the difference between `spawn()` and `exec()`?
- 19.8 What is horizontal scaling?
- 19.9 What is vertical scaling?
- 19.10 What is load balancing?
- 19.11 What is caching?
- 19.12 What is Redis?
- 19.13 Why do we use Redis with Node.js?
- 19.14 What is database query optimization?
- 19.15 What is pagination?
- 19.16 What is cursor-based pagination?
- 19.17 What is debouncing in backend applications?
- 19.18 What is rate limiting?
- 19.19 How do you handle 10,000 concurrent requests?
- 19.20 How do you identify memory leaks?
- 19.21 How do you monitor event loop delay?
- 19.22 How do you optimize CPU-intensive operations?

### **20. Background Jobs and Queues**

- 20.1 What is a background job?
- 20.2 Why do we need background processing?
- 20.3 What is a job queue?
- 20.4 What is Bull or BullMQ?
- 20.5 What is Redis used for in queues?
- 20.6 What is a producer?
- 20.7 What is a consumer or worker?
- 20.8 What is job scheduling?
- 20.9 What is retry logic?
- 20.10 What is exponential backoff?
- 20.11 What is a failed job?
- 20.12 What is a dead-letter queue?
- 20.13 What is a delayed job?
- 20.14 What is a recurring job?
- 20.15 What is job concurrency?
- 20.16 How do you prevent duplicate job processing?
- 20.17 How do you handle failed email notifications?
- 20.18 How do you process payment notifications asynchronously?

### **21. Real-Time Communication**

- 21.1 What is WebSocket?
- 21.2 What is Socket.IO?
- 21.3 What is the difference between WebSocket and HTTP?
- 21.4 What is the difference between WebSocket and Socket.IO?
- 21.5 What is a Socket.IO server?
- 21.6 What is `io.on("connection")`?
- 21.7 What is `socket.emit()`?
- 21.8 What is `io.emit()`?
- 21.9 What is `socket.broadcast.emit()`?
- 21.10 What are rooms in Socket.IO?
- 21.11 What are namespaces?
- 21.12 What is a private chat?
- 21.13 How do you implement group chat?
- 21.14 How do you track online users?
- 21.15 How do you authenticate Socket.IO connections?
- 21.16 How do you handle reconnection?
- 21.17 How do you scale Socket.IO across multiple servers?
- 21.18 What is the Redis adapter?

### **22. Testing and Debugging**

- 22.1 What is unit testing?
- 22.2 What is integration testing?
- 22.3 What is end-to-end testing?
- 22.4 What is Jest?
- 22.5 What is Mocha?
- 22.6 What is Supertest?
- 22.7 What is mocking?
- 22.8 What is a test case?
- 22.9 What is code coverage?
- 22.10 What is debugging in Node.js?
- 22.11 How do you debug using VS Code?
- 22.12 How do you test API endpoints?
- 22.13 How do you mock a database connection?
- 22.14 How do you test error scenarios?
- 22.15 How do you test authentication middleware?
- 22.16 What is the difference between unit and integration tests?

### **23. Deployment and Production**

- 23.1 What is PM2?
- 23.2 Why do we use PM2?
- 23.3 What is a process manager?
- 23.4 How do you start a Node.js application using PM2?
- 23.5 What is PM2 cluster mode?
- 23.6 What is Nginx?
- 23.7 What is a reverse proxy?
- 23.8 How do you configure Nginx with Node.js?
- 23.9 What is SSL?
- 23.10 What is a production environment?
- 23.11 What is CI/CD?
- 23.12 What is Docker?
- 23.13 What is a Dockerfile?
- 23.14 What is a Docker container?
- 23.15 How do you deploy a Node.js application on AWS EC2?
- 23.16 How do you manage environment variables in production?
- 23.17 How do you implement application logging?
- 23.18 What is log rotation?
- 23.19 How do you monitor server health?
- 23.20 How do you perform zero-downtime deployment?

### **24. Microservices and System Design**

- 24.1 What are microservices?
- 24.2 What is the difference between monolithic and microservices architecture?
- 24.3 When should you use microservices?
- 24.4 What is API Gateway?
- 24.5 What is service-to-service communication?
- 24.6 What is synchronous communication?
- 24.7 What is asynchronous communication?
- 24.8 What is message queue communication?
- 24.9 What is RabbitMQ?
- 24.10 What is Kafka?
- 24.11 What is service discovery?
- 24.12 What is circuit breaker pattern?
- 24.13 What is retry pattern?
- 24.14 What is idempotency?
- 24.15 What is distributed tracing?
- 24.16 What is eventual consistency?
- 24.17 What is the Saga pattern?
- 24.18 How do you handle failures between services?
- 24.19 How do you design a scalable notification service?
- 24.20 How do you design a payment processing system?

### **25. Real-World Backend Scenarios**

These questions are important for a 4+ years Node.js developer.

- 25.1 How would you design a user registration and login API?
- 25.2 How would you prevent duplicate user registrations?
- 25.3 How would you implement forgot-password functionality?
- 25.4 How would you implement refresh-token rotation?
- 25.5 How would you handle 10,000 transactions daily?
- 25.6 How would you process 100,000 database records?
- 25.7 How would you handle multiple payment requests simultaneously?
- 25.8 How would you prevent duplicate payments?
- 25.9 How would you implement transaction audit logs?
- 25.10 How would you design a multi-branch finance application?
- 25.11 How would you implement role-based access for different branches?
- 25.12 How would you design an API with pagination, filtering, and sorting?
- 25.13 How would you handle large Excel or CSV imports?
- 25.14 How would you send thousands of emails efficiently?
- 25.15 How would you schedule recurring background jobs?
- 25.16 How would you prevent API abuse?
- 25.17 How would you handle third-party API failures?
- 25.18 How would you implement API request logging?
- 25.19 How would you handle database disconnections?
- 25.20 How would you reduce API response time?
- 25.21 How would you prevent memory leaks in production?
- 25.22 How would you handle multiple users updating the same record?
- 25.23 How would you design a notification system?
- 25.24 How would you design a real-time chat application?
- 25.25 How would you debug an API that works locally but fails in production?

## **How to master Node.js like a professional**

Don't study all 25 sections randomly. Follow this practical sequence:

| Week | Focus                                           |
| ---- | ----------------------------------------------- |
| 1    | Node.js fundamentals, modules, NPM              |
| 2    | File system, events, buffers, streams           |
| 3    | Async programming, Promises, event loop         |
| 4    | HTTP, Express, middleware, REST APIs            |
| 5    | Project architecture, JWT, security             |
| 6    | MongoDB, Mongoose, validation                   |
| 7    | Redis, queues, Socket.IO                        |
| 8    | Performance, testing, deployment, system design |


**My recommendation:** Give extra attention to these concepts:

- Event Loop and Thread Pool
- Callbacks, Promises and Async/Await
- Middleware and Request Lifecycle
- Controller vs Service vs Repository
- JWT, Cookies and RBAC
- MongoDB Aggregation and Indexing
- Redis and BullMQ
- PM2, Clustering and Worker Threads
