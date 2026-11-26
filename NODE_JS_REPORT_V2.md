
<!-- Page top -->
<div id="top"></div>

<!-- Back to Top button -->
<a href="#top" id="backToTop">⬆ Top</a>

<style>

html {
    scroll-behavior: smooth;
}

#backToTop {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background: #007bff;
    color: white;
    padding: 4px 6px;
    border-radius: 6px;
    text-decoration: none;
    font-size: 14px;
    z-index: 9999;
}

.answer-heading {
    color: green;
    text-align: center;
    cursor: pointer;
    scroll-margin-top: 20px;
}

.answer-heading:hover {
    color: darkgreen;
}

</style>

<script>
document.addEventListener("DOMContentLoaded", function () {
    const headings = document.querySelectorAll("h2.answer-heading");
    headings.forEach(function (heading) {
        heading.addEventListener("click", function () {
            const questionsList = document.getElementById("questions-list");
            if (questionsList) {
                questionsList.scrollIntoView({
                    behavior: "smooth",
                    block: "start"
                });
            }
        });
    });
});
</script>

<!-- I'll explain each question using:

- 📌 **Definition** – Simple English.
- 🔑 **Key Points** – Technical keywords.
- 💻 **Syntax & Example** – Practical code.
- ⚙️ **How it works** – Step-by-step explanation.
- 🎯 **Interview Answer** – Simple answer to speak in interviews. -->



### **1. Introduction to Node.js**

- [1.1 What is Node.js?](#1.1)
- [1.2 Why do we use Node.js?](#1.2)
- [1.3 Is Node.js a programming language or runtime environment?](#1.3)
- [1.4 What is the V8 JavaScript engine?](#1.4)
- [1.5 How does Node.js execute JavaScript?](#1.5)
- [1.6 What is the difference between JavaScript and Node.js?](#1.6)
- [1.7 What is the difference between Node.js and a browser?](#1.7)
- [1.8 What are the advantages of Node.js?](#1.8)
- [1.9 What are the disadvantages of Node.js?](#1.9)
- [1.10 What is single-threaded architecture?](#1.10)
- [1.11 Is Node.js really single-threaded?](#1.11)
- [1.12 What is non-blocking I/O?](#1.12)
- [1.13 What is event-driven architecture?](#1.13)
- [1.14 What is asynchronous programming?](#1.14)
- [1.15 What types of applications can we build using Node.js?](#1.15)
- [1.16 Why is Node.js suitable for REST APIs?](#1.16)
- [1.17 When should we avoid Node.js?](#1.17)
- [1.18 What are V8, libuv, and the Node.js runtime?](#1.18)




### **2. Node.js Installation and Project Setup**

- 2.1 How do you install Node.js?
- 2.2 What is NPM?
- 2.3 What is the difference between Node.js and NPM?
- 2.4 What is NPX?
- 2.5 What is the difference between NPM and NPX?
- 2.6 What is `package.json`?
- 2.7 What is `package-lock.json`?
- 2.8 What is `node_modules`?
- 2.9 How do you initialize a Node.js project?
- 2.10 What is `npm init`?
- 2.11 What is the difference between `npm install` and `npm ci`?
- 2.12 What are dependencies?
- 2.13 What are devDependencies?
- 2.14 What are peerDependencies?
- 2.15 What are optionalDependencies?
- 2.16 How do you install a specific package version?
- 2.17 How do you uninstall a package?
- 2.18 How do you update dependencies?
- 2.19 What are NPM scripts?
- 2.20 What is semantic versioning (major, minor, patch)?



### **3. Node.js Global Objects**

- [3.1 What are global objects in Node.js?](#3.1)
- [3.2 What is `global`?](#3.2)
- [3.3 What is `process`?](#3.3)
- [3.4 What is `__dirname`?](#3.4)
- [3.5 What is `__filename`?](#3.5)
- [3.6 What is `console`?](#3.6)
- [3.7 What is `Buffer`?](#3.7)
- [3.8 What is `setTimeout()`?](#3.8)
- [3.9 What is `setInterval()`?](#3.9)
- [3.10 What is `setImmediate()`?](#3.10)
- [3.11 What is `process.env`?](#3.11)
- [3.12 What is `process.argv`?](#3.12)
- [3.13 What is `process.exit()`?](#3.13)
- [3.14 What is the difference between `global` and `window`?](#3.14)
- [3.15 Are `__dirname` and `__filename` available in ES Modules?](#3.15)




### **4. Modules and Module Systems**

- 4.1 What is a module?
- 4.2 Why do we use modules?
- 4.3 What is CommonJS?
- 4.4 What is ES Module?
- 4.5 What is `require()`?
- 4.6 What is `module.exports`?
- 4.7 What is `exports`?
- 4.8 What is the difference between `exports` and `module.exports`?
- 4.9 What is `import`?
- 4.10 What is `export`?
- 4.11 What is the difference between named export and default export?
- 4.12 What is the difference between CommonJS and ES Modules?
- 4.13 What is module caching?
- 4.14 What happens when we import the same module multiple times?
- 4.15 What is a circular dependency?
- 4.16 What is dynamic import?
- 4.17 What is the purpose of `"type": "module"` in package.json?

**Coding practice:**

- Create a separate math module.
- Export and import multiple functions.
- Create a reusable database connection module.
- Create a custom logger module.
- Build a project using CommonJS.
- Convert the same project into ES Modules.

## **Level 2 – Core Node.js Concepts**

### **5. File System (fs)**

- 5.1 What is the File System module?
- 5.2 What is the difference between `fs` and `fs/promises`?
- 5.3 What is `readFile()`?
- 5.4 What is `writeFile()`?
- 5.5 What is `appendFile()`?
- 5.6 What is `unlink()`?
- 5.7 What is `mkdir()`?
- 5.8 What is `readdir()`?
- 5.9 What is `stat()`?
- 5.10 What is the difference between synchronous and asynchronous file operations?
- 5.11 What is `readFileSync()`?
- 5.12 Why should we avoid synchronous file operations in request handlers?
- 5.13 How do you upload and store files?
- 5.14 How do you check whether a file exists?
- 5.15 How do you handle file system errors?

**Coding practice:**

- Create a text file.
- Read data from a file.
- Update file contents.
- Append log messages.
- Delete a file.
- Create a folder dynamically.
- Build a simple file upload storage system.

### **6. Path and OS Modules**

- 6.1 What is the Path module?
- 6.2 What is `path.join()`?
- 6.3 What is `path.resolve()`?
- 6.4 What is the difference between `join()` and `resolve()`?
- 6.5 What is `path.basename()`?
- 6.6 What is `path.dirname()`?
- 6.7 What is `path.extname()`?
- 6.8 What is the OS module?
- 6.9 How do you get operating system information?
- 6.10 How do you get the CPU architecture?
- 6.11 How do you check free memory?
- 6.12 How do you get the hostname?
- 6.13 What is a cross-platform file path?




### **7. Events and EventEmitter**

- [7.1 What is event-driven programming?](#7.1)
- [7.2 What is an event?](#7.2)
- [7.3 What is EventEmitter?](#7.3)
- [7.4 What is the `events` module?](#7.4)
- [7.5 What is `emit()`?](#7.5)
- [7.6 What is `on()`?](#7.6)
- [7.7 What is `once()`?](#7.7)
- [7.8 What is `removeListener()`?](#7.8)
- [7.9 What is `removeAllListeners()`?](#7.9)
- [7.10 What is the difference between `on()` and `once()`?](#7.10)
- [7.11 How do you create custom events?](#7.11)
- [7.12 What is the special `error` event?](#7.12)
- [7.13 What happens if an error event has no listener?](#7.13)
- 7.14 What is event-based communication between modules?


**Coding practice:**

- Create a custom event.
- Emit an event after user registration.
- Listen for payment success.
- Build an order notification event system.


### **8. Buffers and Streams**

- 8.1 What is a Buffer?
- 8.2 Why do we use Buffers?
- 8.3 What is binary data?
- 8.4 How do you create a Buffer?
- 8.5 What is `Buffer.from()`?
- 8.6 What is `Buffer.alloc()`?
- 8.7 What is the difference between `alloc()` and `from()`?
- 8.8 What is a Stream?
- 8.9 Why do we use streams?
- 8.10 What are the four types of streams?
- 8.11 What is a Readable stream?
- 8.12 What is a Writable stream?
- 8.13 What is a Duplex stream?
- 8.14 What is a Transform stream?
- 8.15 What is `pipe()`?
- 8.16 What is `pipeline()`?
- 8.17 What is backpressure?
- 8.18 What is the difference between Buffer and Stream?
- 8.19 How do you process large files efficiently?
- 8.20 How do you handle stream errors?

**Coding practice:**

- Read a large file using streams.
- Write data using writable streams.
- Copy one file to another using `pipe()`.
- Compress a file using a transform stream.
- Process a large CSV file without loading it entirely into memory.




### **9. HTTP Module and Web Server**

- [9.1 What is the HTTP module?](#9.1)
- [9.2 How do you create an HTTP server?](#9.2)
- [9.3 What is `http.createServer()`?](#9.3)
- [9.4 What is a request object?](#9.4)
- [9.5 What is a response object?](#9.5)
- [9.6 What is `req.method`?](#9.6)
- [9.7 What is `req.url`?](#9.7)
- [9.8 What is `req.headers`?](#9.8)
- [9.9 What is `res.write()`?](#9.9)
- [9.10 What is `res.end()`?](#9.10)
- [9.11 What is `res.setHeader()`?](#9.11)
- [9.12 What is the difference between HTTP and HTTPS?](#9.12)
- [9.13 What are HTTP status codes?](#9.13)
- [9.14 What is the difference between GET, POST, PUT, PATCH, and DELETE?](#9.14)
- [9.15 What are request headers and response headers?](#9.15)
- [9.16 What is the request-response lifecycle?](#9.16)
- [9.17 How do you parse JSON request bodies without Express?](#9.17)
- 9.18 How do you handle HTTP errors?

**Coding practice:**

- Create a basic HTTP server.
- Create GET and POST routes.
- Accept JSON data.
- Return appropriate status codes.
- Build a small REST API without Express.

## **Level 3 – Asynchronous Node.js**

### **10. Asynchronous Programming**

- [10.1 What is synchronous execution?](#10.1)
- [10.2 What is asynchronous execution?](#10.2)
- [10.3 What is blocking I/O?](#10.3)
- [10.4 What is non-blocking I/O?](#10.4)
- [10.5 What is callback-based programming?](#10.5)
- [10.6 What is callback hell?](#10.6)
- [10.7 What is a Promise?](#10.7)
- [10.8 What are Promise states?](#10.8)
- [10.9 What is Promise chaining?](#10.9)
- [10.10 What is `async/await`?](#10.10)
- [10.11 What is the difference between callbacks and Promises?](#10.11)
- [10.12 What is the difference between Promise and async/await?](#10.12)
- [10.13 What is `Promise.all()`?](#10.13)
- [10.14 What is `Promise.allSettled()`?](#10.14)
- [10.15 What is `Promise.race()`?](#10.15)
- [10.16 What is `Promise.any()`?](#10.16)
- [10.17 How do you handle asynchronous errors?](#10.17)
- [10.18 What happens if you forget to use `await`?](#10.18)
- [10.19 How do you execute multiple operations sequentially?](#10.19)
- [10.20 How do you execute multiple operations in parallel?](#10.20)


### **11. Event Loop and Thread Pool**

- [11.1 What is the Node.js event loop?](#11.1)
- [11.2 How does the event loop work?](#11.2)
- [11.3 What is the call stack?](#11.3)
- [11.4 What is the callback queue?](#11.4)
- [11.5 What is the microtask queue?](#11.5)
- [11.6 What is the timers phase?](#11.6)
- [11.7 What is the poll phase?](#11.7)
- [11.8 What is the check phase?](#11.8)
- [11.9 What is the close callbacks phase?](#11.9)
- [11.10 What is libuv?](#11.10)
- [11.11 What is the libuv thread pool?](#11.11)
- [11.12 What is the default thread pool size?](#11.12)
- [11.13 What is `process.nextTick()`?](#11.13)
- [11.14 What is the difference between `process.nextTick()` and Promise callbacks?](#11.14)
- [11.15 Which operations use the thread pool?](#11.15)
- [11.16 Does every asynchronous operation use the thread pool?](#11.16)
- [11.17 How can CPU-intensive operations block the event loop?](#11.17)
- [11.18 How do you prevent event loop blocking?](#11.18)
- [11.19 Quick Revision – Important Concepts](#11.19)
- [11.20 Important Event Loop Phase Order](#11.20)



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
- 
**Coding practice:**

- Create request logging middleware.
- Create JWT authentication middleware.
- Create admin authorization middleware.
- Create request validation middleware.
- Create centralized error middleware.
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




### **15. Node.js Project Architecture**

- [15.1 How should we structure a Node.js project?](#15.1)
- [15.2 What is MVC architecture?](#15.2)
- [15.3 What is the Model layer?](#15.3)
- [15.4 What is the View layer?](#15.4)
- [15.5 What is the Controller layer?](#15.5)
- [15.6 What is the Service layer?](#15.6)
- [15.7 What is the Repository pattern?](#15.7)
- [15.8 What is the difference between controller and service?](#15.8)
- [15.9 What is the difference between service and repository?](#15.9)
- [15.10 Why should we separate business logic from controllers?](#15.10)
- [15.11 What is dependency injection?](#15.11)
- [15.12 What is a reusable utility function?](#15.12)
- [15.13 What is configuration management?](#15.13)
- [15.14 How do you manage environment variables?](#15.14)
- [15.15 What is the purpose of a centralized database connection?](#15.15)
- [15.16 How do you handle multiple environments (development, staging, production)?](#15.16)
- [15.17 How do you organize routes, controllers, services, models, and middleware?](#15.17)
- [15.18 What is a monolithic architecture?](#15.18)
- [15.19 What is a modular monolith?](#15.19)
- [15.20 What is clean architecture?](#15.20)





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
- [18.21 What is request size limiting?](#18.21)
- [18.22 How do you prevent brute-force login attempts?](#18.22)



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


<h2  class="answer-heading" id="1.1">1.1 What is Node.js?</h2>

📌 **Definition:**

Node.js is an **open-source, cross-platform JavaScript runtime environment** that allows us to execute JavaScript outside the browser, mainly on the server side.

It is built on Google's **V8 JavaScript Engine**.

🔑 **Key Points:**

- JavaScript Runtime Environment
- Built on V8 Engine
- Open Source
- Cross Platform
- Server-side Development
- Asynchronous and Non-blocking I/O
- Event-driven Architecture

💻 **Example:**

```js
// app.js
console.log("Hello from Node.js");
```

Run the file using:

```js
node app.js
```

Output:

```js
Hello from Node.js
```

🎯 **Interview Answer:**

Node.js is an open-source, cross-platform JavaScript runtime environment built on Google's V8 engine. It allows us to execute JavaScript outside the browser and build scalable server-side applications using asynchronous and non-blocking I/O.

<h2  class="answer-heading" id="1.2">1.2 Why do we use Node.js?</h2>


📌 **Definition:**

We use Node.js to build fast, scalable, and efficient server-side applications using JavaScript.

It is especially useful for applications that handle multiple concurrent requests.

🔑 **Key Points:**

1. **High Performance** – Uses the V8 engine to execute JavaScript.
2. **Non-blocking I/O** – Handles I/O operations without blocking the main thread.
3. **Event-driven Architecture** – Uses events to handle asynchronous operations.
4. **Scalability** – Supports multiple concurrent connections.
5. **Single Language** – We can use JavaScript for both frontend and backend.
6. **NPM Ecosystem** – Provides thousands of reusable packages.
7. **Real-time Applications** – Supports WebSockets and Socket.IO.

💻 **Example:**

Using Node.js, we can create an API to fetch user information.

```js
const http = require("http");

const server = http.createServer((req, res) => {
    res.writeHead(200, {
        "Content-Type": "application/json"
    });

    res.end(JSON.stringify({
        message: "User data fetched successfully"
    }));
});

server.listen(3000);
```

🎯 **Interview Answer:**

We use Node.js to build fast and scalable backend applications. Its non-blocking I/O, asynchronous programming, event-driven architecture, and NPM ecosystem make it suitable for APIs and real-time applications.

<h2  class="answer-heading" id="1.3">1.3 Is Node.js a programming language or runtime environment?</h2>


📌 **Definition:**

Node.js is a **runtime environment**, not a programming language.

JavaScript is the programming language, and Node.js provides the environment required to execute JavaScript outside the browser.

🔑 **Key Points:**

- JavaScript → Programming Language
- Node.js → Runtime Environment
- V8 → JavaScript Engine
- Libuv → Handles asynchronous I/O and event loop functionality.

💻 **Example:**

```js
console.log("Hello World");
```

Here:

- `console.log()` → JavaScript functionality.
- `node app.js` → Executes JavaScript using Node.js.

🎯 **Interview Answer:**

Node.js is not a programming language. It is a JavaScript runtime environment that allows us to execute JavaScript outside the browser using the V8 engine.

<h2  class="answer-heading" id="1.4">1.4 What is the V8 JavaScript Engine?</h2>


📌 **Definition:**

V8 is an open-source JavaScript engine developed by Google. It converts JavaScript code into machine code and executes it.

Node.js uses the V8 engine to execute JavaScript.

🔑 **Key Points:**

- Developed by Google.
- Written mainly in C++.
- Open Source.
- Uses Just-In-Time (JIT) compilation.
- Converts JavaScript into machine code.
- Provides garbage collection and memory management.

💻 **Example:**

```js
const a = 10;
const b = 20;

console.log(a + b);
```

When Node.js executes this code, the V8 engine processes the JavaScript and executes it.

🎯 **Interview Answer:**

V8 is Google's open-source JavaScript engine. It uses Just-In-Time compilation to convert JavaScript into machine code and execute it efficiently. Node.js uses V8 to execute JavaScript code.

<h2  class="answer-heading" id="1.5">1.5 How does Node.js execute JavaScript?</h2>


📌 **Definition:**

Node.js executes JavaScript using the V8 engine. It uses Libuv to handle asynchronous I/O operations and the event loop to manage asynchronous callbacks.

🔑 **Execution Flow:**

**JavaScript Code**

app.js

**V8 Engine**

Compiles and executes JavaScript

**Node.js APIs + Libuv**

Handles asynchronous operations

**Event Loop**

Coordinates callbacks and asynchronous tasks

🔑 **Key Points:**

1. Node.js receives JavaScript code.
2. V8 compiles and executes JavaScript.
3. Synchronous code executes on the main JavaScript thread.
4. Asynchronous I/O operations are handled using Node.js APIs and operating-system facilities or Libuv's thread pool, depending on the operation.
5. When asynchronous operations complete, their callbacks are scheduled.
6. The event loop coordinates when callbacks execute.

💻 **Example:**

```js
console.log("Start");

setTimeout(() => {
    console.log("Timer Completed");
}, 1000);

console.log("End");
```

Output:

```js
Start
End
Timer Completed
```

**Why?**

- `Start` executes first.
- `setTimeout()` schedules a timer.
- `End` executes without waiting for the timer.
- After the timer expires, its callback executes.

🎯 **Interview Answer:**

Node.js uses the V8 engine to execute JavaScript. It uses Libuv and the event loop to manage asynchronous operations. This allows Node.js to handle I/O operations without blocking the main JavaScript thread.

<h2  class="answer-heading" id="1.6">1.6 What is the difference between JavaScript and Node.js?</h2>


📌 **Definition:**

JavaScript is a programming language, whereas Node.js is a runtime environment used to execute JavaScript outside the browser.

| JavaScript                                                         | Node.js                                       |
| ------------------------------------------------------------------ | --------------------------------------------- |
| Programming language                                               | Runtime environment                           |
| Used for frontend and backend development                          | Mainly used for backend development           |
| Runs in browsers and other JS runtimes                             | Runs outside the browser                      |
| Browser provides DOM APIs                                          | Provides Node.js APIs                         |
| Uses browser APIs like `localStorage`                              | Provides APIs like `fs` and `http`            |
| Cannot directly access server files in normal browser environments | Can access server files using filesystem APIs |

💻 **Example:**

JavaScript in browser:

```js
document.getElementById("title");
```

Node.js:

```js
const fs = require("fs");

fs.readFile("data.txt", "utf8", (err, data) => {
    console.log(data);
});
```

🎯 **Interview Answer:**

JavaScript is a programming language, while Node.js is a runtime environment. JavaScript is commonly used for frontend development, and Node.js allows us to use JavaScript for backend development.

<h2  class="answer-heading" id="1.7">1.7 What is the difference between Node.js and a browser?</h2>


📌 **Definition:**

A browser is an environment used to display and interact with web pages, whereas Node.js is a runtime environment used to execute JavaScript outside the browser.

| Browser                                  | Node.js                                  |
| ---------------------------------------- | ---------------------------------------- |
| Runs JavaScript in a browser environment | Runs JavaScript outside the browser      |
| Provides DOM APIs                        | Provides server-side APIs                |
| Supports `window` and `document`         | Supports `global` and `process`          |
| Uses `fetch()` and browser APIs          | Provides `fs`, `http`, `path`, etc.      |
| Used for frontend development            | Mainly used for backend development      |
| Restricted access to local files         | Can access files through filesystem APIs |

💻 **Example:**

Browser:

```js
console.log(window.location.href);
```

Node.js:

```js
console.log(process.version);
```

🎯 **Interview Answer:**

The main difference is that browsers provide APIs like DOM, window, and document for frontend development, whereas Node.js provides APIs like filesystem, HTTP, and process for server-side development. Both can execute JavaScript.

<h2  class="answer-heading" id="1.8">1.8 What are the advantages of Node.js?</h2>


📌 **Definition:**

Node.js provides several advantages for developing scalable and high-performance applications.

🔑 **Key Points:**

1. **High Performance** – Uses the V8 engine.
2. **Non-blocking I/O** – Does not block the main thread while waiting for asynchronous I/O.
3. **Scalability** – Handles multiple concurrent connections.
4. **Single Language** – JavaScript for frontend and backend.
5. **NPM Ecosystem** – Large collection of reusable packages.
6. **Real-time Support** – Supports WebSockets and Socket.IO.
7. **Microservices** – Suitable for building lightweight services.
8. **Cross Platform** – Runs on Windows, Linux, and macOS.

🎯 **Interview Answer:**

The main advantages of Node.js are high performance, non-blocking I/O, scalability, a large NPM ecosystem, cross-platform support, and the ability to use JavaScript for both frontend and backend development.

<h2  class="answer-heading" id="1.9">1.9 What are the disadvantages of Node.js?</h2>


📌 **Definition:**

Node.js has some limitations, especially when handling CPU-intensive operations and applications that require heavy synchronous processing.

🔑 **Key Points:**

1. **CPU-intensive Tasks** – Heavy computations can block the main JavaScript thread.
2. **Single JavaScript Thread** – JavaScript callbacks generally execute on one main thread per event loop.
3. **Callback Complexity** – Nested callbacks can make code difficult to maintain (Callback Hell).
4. **Memory Management** – Large applications need proper memory optimization.
5. **Database Limitations** – Poorly optimized queries can affect performance.
6. **Package Security** – Third-party NPM packages may contain vulnerabilities.

💻 **Example:**

```js
console.log("Start");

// CPU-intensive operation
let total = 0;

for (let i = 0; i < 1000000000; i++) {
    total += i;
}

console.log("Calculation completed");
console.log("End");
```

**Problem:** The CPU-intensive loop blocks the main JavaScript thread until it finishes.

🎯 **Interview Answer:**

The main disadvantages of Node.js are CPU-intensive tasks can block the event loop, JavaScript execution is single-threaded by default, and managing complex asynchronous operations can sometimes be challenging. We can overcome CPU-intensive limitations using Worker Threads or separate services.

<h2  class="answer-heading" id="1.10">1.10 What is single-threaded architecture?</h2>


📌 **Definition:**

Single-threaded architecture means the application executes JavaScript code using one main thread.

In Node.js, JavaScript callbacks normally execute on a single main thread, which is managed by the event loop.

🔑 **Key Points:**

- Main Thread
- Call Stack
- Event Loop
- Callback Queue
- Non-blocking I/O
- Asynchronous Operations

💻 **Example:**

```js
console.log("Task 1");
console.log("Task 2");
console.log("Task 3");
```

Output:

```js
Task 1
Task 2
Task 3
```

All three statements execute sequentially on the main JavaScript thread.

🎯 **Interview Answer:**

Single-threaded architecture means JavaScript code executes on one main thread using a single call stack. Node.js uses an event loop and asynchronous I/O to handle multiple operations efficiently without creating a separate JavaScript thread for every request.

<h2  class="answer-heading" id="1.11">1.11 Is Node.js really single-threaded?</h2>


Important interview question

📌 **Definition:**

No. Node.js is not completely single-threaded.

JavaScript execution normally happens on a single main thread, but Node.js uses additional threads and operating-system facilities to handle certain background operations.

🔑 **Key Points:**

- Main JavaScript Thread
- Event Loop
- Libuv Thread Pool
- Worker Threads
- Operating System
- Asynchronous I/O

💻 **Example:**

```js
const crypto = require("crypto");

console.log("Start");

crypto.pbkdf2(
    "password",
    "salt",
    100000,
    64,
    "sha512",
    (err, key) => {
        console.log("Background task completed");
    }
);

console.log("End");
```

Output:

```js
Start
End
Background task completed
```

**How does it work?**

1. Main thread starts executing JavaScript.
2. `crypto.pbkdf2()` performs its expensive operation using Libuv's thread pool.
3. Main thread continues executing other JavaScript.
4. Once the background operation completes, its callback is scheduled.
5. The event loop executes the callback when appropriate.

🎯 **Interview Answer:**

Node.js is single-threaded for JavaScript execution by default, but internally it uses Libuv's thread pool, operating-system asynchronous I/O, and Worker Threads to perform background operations. So, Node.js is not completely single-threaded.

<h2  class="answer-heading" id="1.12">1.12 What is non-blocking I/O?</h2>


📌 **Definition:**

Non-blocking I/O means Node.js can start an Input/Output operation, such as reading a file or fetching database data, without blocking the main JavaScript thread while waiting for the operation to complete.

🔑 **Key Points:**

- I/O → Input/Output
- Non-blocking
- Asynchronous Operations
- Callback
- Promise
- Event Loop
- Concurrency

💻 **Example:**

```js
const fs = require("fs");

console.log("Start");

fs.readFile("data.txt", "utf8", (err, data) => {
    if (err) {
        console.log(err);
        return;
    }

    console.log(data);
});

console.log("End");
```

Output:

```js
Start
End
File data
```

**How does it work?**

- Node.js starts reading the file.
- It does not wait for the file operation to finish.
- The main thread continues executing the next statement.
- After the file is read, the callback executes.

🎯 **Interview Answer:**

Non-blocking I/O means Node.js does not block the main JavaScript thread while waiting for I/O operations. It can continue executing other tasks and handle the completed operation through callbacks, promises, and the event loop.

<h2  class="answer-heading" id="1.13">1.13 What is event-driven architecture?</h2>


📌 **Definition:**

Event-driven architecture is a programming approach where the application responds to events such as user actions, incoming requests, or completed asynchronous operations.

Node.js uses an event-driven architecture to manage asynchronous operations.

🔑 **Key Points:**

- Event
- Event Emitter
- Event Listener
- Event Handler
- Event Loop
- Callback

💻 **Example:**

```js
const EventEmitter = require("events");

const eventEmitter = new EventEmitter();

// Event Listener
eventEmitter.on("userLogin", (username) => {
    console.log(`${username} logged in`);
});

// Trigger Event
eventEmitter.emit("userLogin", "Gopi");
```

Output:

```js
Gopi logged in
```

**How does it work?**

1. Create an EventEmitter.
2. Register an event listener using `.on()`.
3. Trigger an event using `.emit()`.
4. The registered listener executes.

🎯 **Interview Answer:**

Event-driven architecture is a programming approach where application behavior is triggered by events. Node.js uses EventEmitter, event listeners, and the event loop to manage event-based and asynchronous operations.

<h2  class="answer-heading" id="1.14">1.14 What is asynchronous programming?</h2>


📌 **Definition:**

Asynchronous programming allows an application to start an operation and continue executing other code without waiting for that operation to finish.

In Node.js, we commonly use callbacks, Promises, and async/await for asynchronous programming.

🔑 **Key Points:**

1. Callbacks
2. Promises
3. Async/Await
4. Non-blocking Operations
5. Event Loop
6. Concurrency

💻 **Example:**

```js
console.log("Start");

async function getUser() {
    const user = await Promise.resolve("Gopi");

    console.log(user);
}

getUser();

console.log("End");
```

Output:

```js
Start
End
Gopi
```

**How does it work?**

- `getUser()` starts executing.
- `await` pauses that async function until the Promise settles.
- The main JavaScript thread continues executing.
- After the Promise resolves, the remaining async function code continues.

🎯 **Interview Answer:**

Asynchronous programming allows us to execute operations without blocking the main thread while waiting for them to complete. In Node.js, we use callbacks, Promises, and async/await to handle asynchronous operations.

<h2  class="answer-heading" id="1.15">1.15 What types of applications can we build using Node.js?</h2>


📌 **Definition:**

Node.js can be used to build different types of backend and real-time applications.

🔑 **Key Points with Practical Examples:**


<img 
  src="https://images.openai.com/static-rsc-4/Fitu48g3eEesRgpO_pab1Kh5K5-IbRpKZQ_vWiV1XlM4XcAdW1YVz3zOZDSdqEocq0pdHA3w98KUYN5m4VDjCBJKCMU3KImPXH535navK0djZTPVyaVla9dkPJmUCbSrnfRmusejn1ovJ_snTMlGOBerxbN1C1F2Px9Y4ncVO24?purpose=inline"
  width="300"
  height="180"
  alt="Movie Stream Dashboard"
/>

**1. REST APIs**

Backend services for React, Angular, and mobile applications.


<img 
  src="https://images.openai.com/static-rsc-4/tQxsN2NpioepTiF17zm2nOz64e_btuuwCQDOpvcgf-YMUeVZ2tNrnBYj7l7IZyONq6pM6RX4lN4mIOMs_IojGuBoXNWcSsBWwccRi1JPZP9F5OJUO2snigeELUJaHNFRxRdIULlqVVe95pXwVryH70M-OZppYg5yp1kOlxeDh6o?purpose=inline"
  width="300"
  height="180"
  alt="Movie Stream Dashboard"
/>

**2. Real-time Applications**

Chat applications, live notifications, and messaging using Socket.IO.


<img 
  src="https://images.openai.com/static-rsc-4/ADNKgwx6KgFwKglH4RRRf6RTnMtuN7JIK2AwfaDHIn92-Vmh5_jIj9Shg1_1p6umNdRJdCZF0M3vkdOirommHBYxpxAkHlYgxPT-mviWukOiSE4cggxawH44Xg8zH15iENn76rwuqIsU-8s99RNUYHjDswEdUr-QTsZLG0ZNkBc?purpose=inline"
  width="300"
  height="180"
  alt="Movie Stream Dashboard"
/>


**3. E-commerce Applications**

Product management, orders, payments, and inventory.

<img 
  src="https://images.openai.com/static-rsc-4/ZQlH3k34GjP3tf-CMJHDeIPEgxN6mU_61MhGT6H50WUk3MfBvTjlYQNj1Rp08-xg9OlLrxz5NDpWTxx7Xow-CGqZuGRRMKmS9Gs4wymHNY0FE_HlS0QtMvbAMogdg0lilLJwSB68-6WGXr_yhv2MLMmEZLomMetKgfMY5n51NVw?purpose=inline"
  width="300"
  height="180"
  alt="Movie Stream Dashboard"
/>



**4. Microservices**

Independent backend services communicating through APIs and messaging.

<img 
  src="https://images.openai.com/static-rsc-4/91-ONLPkEl1xr7l9-DsvzTpPgRSyaY_TT294TScfJU7LpcrhCQ_yH29O8fUuFtLi4iN99Te6EAeRQL2M9YnlE1KpNjmuR6ZQSnkqcbBjWtuT__Qwl6UKxe0LonZDi-VbBxkLq1sT3NUq6950MQwAlqXBWoSiynzq9OCYLydFCz0?purpose=inline"
  width="300"
  height="180"
  alt="Movie Stream Dashboard"
/>


**5. Streaming Applications**

Data streaming and media delivery services.


<img 
  src="https://images.openai.com/static-rsc-4/KyGaw8n_1yvljUxYsfNh830E1EzjyPz6E11Ri5xF9uTtf3h53SU9PNronvDMM-X7pVdMCIL_YSmjpLF1XHSamL65jRJ3sdVxF0ifevOAXxQQDitZvDkBt1bMNRPQEdvfHgT9TZXpOorStakYdAcVlRPohWOzkuBMldy7ypnmNEo?purpose=inline"
  width="300"
  height="180"
  alt="Movie Stream Dashboard"
/>

**6. IoT Applications**

Device communication, sensor monitoring, and real-time dashboards.

Other applications include:

- Authentication systems
- Payment integration services
- Web applications
- Background job processing
- Notification systems
- GraphQL APIs

🎯 **Interview Answer:**

Using Node.js, we can build REST APIs, real-time chat applications, e-commerce platforms, microservices, streaming applications, authentication systems, and IoT applications.

<h2  class="answer-heading" id="1.16">1.16 Why is Node.js suitable for REST APIs?</h2>


📌 **Definition:**

Node.js is suitable for REST APIs because it supports asynchronous processing, non-blocking I/O, and handles multiple concurrent HTTP requests efficiently.

🔑 **Key Points:**

1. **Non-blocking I/O** – Handles requests without waiting for I/O operations.
2. **Scalability** – Supports multiple concurrent connections.
3. **JSON Support** – Works naturally with JSON data.
4. **Fast Development** – Provides frameworks like Express.js and NestJS.
5. **Database Integration** – Supports MongoDB, MySQL, PostgreSQL, and Redis.
6. **Middleware Support** – Makes authentication, validation, and error handling easier.
7. **RESTful Architecture** – Supports HTTP methods such as GET, POST, PUT, PATCH, and DELETE.

💻 **Example using Express.js:**

```js
const express = require("express");

const app = express();

app.use(express.json());

app.get("/users", (req, res) => {
    res.status(200).json({
        message: "Users fetched successfully",
        users: []
    });
});

app.listen(3000, () => {
    console.log("Server running on port 3000");
});
```

🎯 **Interview Answer:**

Node.js is suitable for REST APIs because of its non-blocking I/O, asynchronous processing, JSON support, and scalability. Frameworks like Express.js and NestJS make API development easier and faster.

<h2  class="answer-heading" id="1.17">1.17 When should we avoid Node.js?</h2>


📌 **Definition:**

We should avoid using Node.js when the application mainly performs heavy CPU-intensive operations that can block the main JavaScript thread.

🔑 **Key Points:**

1. **Heavy CPU Computation** – Complex mathematical calculations.
2. **Large Image Processing** – CPU-heavy image manipulation.
3. **Video Encoding** – Resource-intensive video processing.
4. **Machine Learning Training** – Heavy model training workloads.
5. **Scientific Computing** – Complex numerical computations.

**Important:** Node.js can still be used in these applications if we move CPU-intensive work to Worker Threads, native modules, or separate services.

🎯 **Interview Answer:**

We should avoid using Node.js for applications that mainly perform heavy CPU-intensive operations because they can block the event loop and affect performance. However, we can handle these operations using Worker Threads or separate microservices.

<h2  class="answer-heading" id="1.18">1.18 What are V8, Libuv, and the Node.js runtime?</h2>


Very important interview question

📌 **Definition:**

V8, Libuv, and the Node.js runtime are three important components that work together to execute JavaScript and handle asynchronous operations.

### **1. V8 Engine**

**Definition:** V8 is Google's JavaScript engine that compiles and executes JavaScript code.

**Responsibilities:**

- JavaScript execution
- JIT compilation
- Memory management
- Garbage collection

### **2. Libuv**

**Definition:** Libuv is a C library used by Node.js to provide asynchronous I/O operations, an event loop, and a thread pool.

**Responsibilities:**

- Event loop implementation
- Thread pool
- Asynchronous file system operations
- DNS operations
- Certain cryptographic operations
- Operating-system I/O integration

### **3. Node.js Runtime**

**Definition:** Node.js runtime provides the complete environment required to execute JavaScript outside the browser.

**Responsibilities:**

- Provides built-in modules such as `fs`, `http`, and `path`.
- Integrates V8 and Libuv.
- Provides Node.js APIs.
- Manages runtime execution.





<h2  class="answer-heading" id="3.1">3.1 What are global objects in Node.js?</h2>

📌 **Definition:**

Global objects are built-in objects and functions that are available throughout a Node.js application without requiring an explicit import.

We can access them from different files and modules depending on the global object's scope.

🔑 **Key Points:**

- Built-in Objects
- Global Scope
- No Import Required
- Runtime Environment
- Available Across Modules (depending on the object)

**Examples of Node.js global objects:**

| Global Object    | Purpose                                         |
| ---------------- | ----------------------------------------------- |
| `global`         | Global namespace                                |
| `process`        | Current Node.js process information             |
| `console`        | Display messages                                |
| `Buffer`         | Handle binary data                              |
| `setTimeout()`   | Execute code after a delay                      |
| `setInterval()`  | Execute code repeatedly                         |
| `setImmediate()` | Schedule code for the next event-loop iteration |

💻 **Example:**

```js
console.log("Hello Node.js");

console.log(process.version);

console.log(global);
```

🎯 **Interview Answer:**

Global objects are built-in objects and functions provided by the Node.js runtime. They can be accessed without importing them explicitly. Examples include global, process, console, Buffer, and timer functions.

<h2  class="answer-heading" id="3.2">3.2 What is `global`?</h2>

📌 **Definition:**

`global` is the global namespace object in Node.js. Properties and variables attached to it can be accessed across different modules.

🔑 **Key Points:**

- Global Namespace
- Global Properties
- Cross-module Access
- No Import Required

💻 **Syntax:**

```js
global.variableName = value;
```

💻 **Example:**

```js
// file1.js

global.username = "Gopi";
```

```js
// file2.js

console.log(global.username);
```

**Output:**

```js
Gopi
```

**Important:** Avoid creating unnecessary global variables because they can cause naming conflicts and make applications difficult to maintain.

🎯 **Interview Answer:**

Global is the global namespace object in Node.js. We can attach properties to it and access those properties from different modules without importing them.

<h2  class="answer-heading" id="3.3">3.3 What is `process`?</h2>

📌 **Definition:**

`process` is a global object in Node.js that provides information and control over the currently running Node.js process.

A process represents an executing instance of a program.

🔑 **Key Points:**

- Process Information
- Environment Variables
- Command-line Arguments
- Process ID
- Memory Usage
- Exit Status
- Runtime Control

**Important process properties and methods:**

| Property / Method       | Purpose                           |
| ----------------------- | --------------------------------- |
| `process.pid`           | Returns process ID                |
| `process.version`       | Returns Node.js version           |
| `process.platform`      | Returns operating system platform |
| `process.cwd()`         | Returns current working directory |
| `process.env`           | Access environment variables      |
| `process.argv`          | Access command-line arguments     |
| `process.memoryUsage()` | Returns memory usage              |
| `process.exit()`        | Terminates the process            |

💻 **Example:**

```js
console.log("Process ID:", process.pid);

console.log("Node Version:", process.version);

console.log("Platform:", process.platform);

console.log("Current Directory:", process.cwd());
```

🎯 **Interview Answer:**

Process is a global Node.js object that provides information and control over the currently running application. We use it to access environment variables, command-line arguments, process ID, memory usage, and runtime information.

<h2  class="answer-heading" id="3.4">3.4 What is `__dirname`?</h2>

📌 **Definition:**

`__dirname` is a CommonJS module variable that returns the absolute directory path of the current JavaScript file.

🔑 **Key Points:**

- CommonJS
- Current Directory
- Absolute Path
- File Location

💻 **Example:**

Suppose your project structure is:

```js
my-project/
│
├── app.js
│
└── files/
    └── data.txt
```

**app.js**

```js
console.log(__dirname);
```

**Output (example):**

```js
/home/gopi/my-project
```

**Practical Usage:**

We commonly use `__dirname` to create reliable file paths.

```js
const path = require("path");

const filePath = path.join(__dirname, "files", "data.txt");

console.log(filePath);
```

**Output:**

```js
/home/gopi/my-project/files/data.txt
```

🎯 **Interview Answer:**

`__dirname` is a CommonJS module variable that returns the absolute directory path of the current JavaScript file. It is commonly used to construct file paths using the path module.

<h2  class="answer-heading" id="3.5">3.5 What is `__filename`?</h2>

📌 **Definition:**

`__filename` is a CommonJS module variable that returns the absolute path, including the filename, of the current JavaScript file.

🔑 **Key Points:**

- CommonJS
- Absolute File Path
- Current File Name
- File Location

💻 **Example:**

```js
console.log(__filename);
```

**Output (example):**

```js
/home/gopi/my-project/app.js
```

**Practical Usage:**

```js
const path = require("path");

console.log("File Name:", path.basename(__filename));

console.log("Directory:", path.dirname(__filename));
```

**Output:**

```js
File Name: app.js
Directory: /home/gopi/my-project
```

🎯 **Interview Answer:**

`__filename` is a CommonJS module variable that returns the absolute path of the current JavaScript file, including its filename.

<h2  class="answer-heading" id="3.6">3.6 What is `console`?</h2>

📌 **Definition:**

`console` is a global object in Node.js that provides methods to display messages, debug applications, and monitor program execution.

🔑 **Key Points:**

- Debugging
- Logging
- Error Messages
- Output Monitoring

**Important console methods:**

| Method              | Purpose                          |
| ------------------- | -------------------------------- |
| `console.log()`     | Display normal messages          |
| `console.error()`   | Display error messages           |
| `console.warn()`    | Display warning messages         |
| `console.info()`    | Display informational messages   |
| `console.table()`   | Display data in table format     |
| `console.time()`    | Start a timer                    |
| `console.timeEnd()` | End a timer and display duration |
| `console.clear()`   | Clear the console                |

💻 **Example:**

```js
console.log("Application started");

console.info("User logged in");

console.warn("Storage is almost full");

console.error("Database connection failed");

const users = [
    { id: 1, name: "Gopi" },
    { id: 2, name: "Arun" }
];

console.table(users);
```

🎯 **Interview Answer:**

Console is a global object in Node.js used for logging, debugging, and monitoring application execution. It provides methods like log, error, warn, info, and table.

<h2  class="answer-heading" id="3.7">3.7 What is `Buffer`?</h2>

📌 **Definition:**

Buffer is a global class in Node.js used to handle binary data directly in memory.

It is commonly used when working with files, images, videos, network communication, and streams.

🔑 **Key Points:**

- Binary Data
- Memory Management
- UTF-8 Encoding
- File Handling
- Network Communication
- Streams

💻 **Syntax:**

```js
Buffer.from(data, encoding);

Buffer.alloc(size);
```

💻 **Example:**

```js
// Convert string into Buffer

const buffer = Buffer.from("Hello Node.js");

console.log(buffer);

// Convert Buffer into string

console.log(buffer.toString());
```

**Output:**

```js
<Buffer 48 65 6c 6c 6f 20 4e 6f 64 65 2e 6a 73>

Hello Node.js
```

**Other Buffer methods:**

```js
// Create an empty Buffer of 10 bytes
const buffer1 = Buffer.alloc(10);

// Convert string into Buffer
const buffer2 = Buffer.from("Gopi");

// Convert Buffer into string
console.log(buffer2.toString());

// Get Buffer length
console.log(buffer2.length);
```

🎯 **Interview Answer:**

Buffer is a global class in Node.js used to handle binary data in memory. It is commonly used for file handling, image processing, network communication, and streams.

<h2  class="answer-heading" id="3.8">3.8 What is `setTimeout()`?</h2>

📌 **Definition:**

`setTimeout()` is a timer function that executes a callback function once after a specified delay.

🔑 **Key Points:**

- Timer Function
- Callback Function
- Delay in Milliseconds
- Executes Once
- Asynchronous Scheduling

💻 **Syntax:**

```js
setTimeout(callbackFunction, delayInMilliseconds);
```

💻 **Example:**

```js
console.log("Start");

setTimeout(() => {
    console.log("Hello Gopi");
}, 2000);

console.log("End");
```

**Output:**

```js
Start
End
Hello Gopi
```

**Explanation:**

- `2000` means 2 seconds.
- The callback is scheduled after the specified delay.
- Other JavaScript code can execute without waiting for the timer.
- The callback executes when the timer expires and the event loop can process it.

**Clear a timeout:**

```js
const timer = setTimeout(() => {
    console.log("Hello");
}, 3000);

// Cancel the timer
clearTimeout(timer);
```

🎯 **Interview Answer:**

setTimeout is a timer function used to execute a callback once after a specified delay in milliseconds. It does not block the main JavaScript thread.

<h2  class="answer-heading" id="3.9">3.9 What is `setInterval()`?</h2>

📌 **Definition:**

`setInterval()` is a timer function that repeatedly executes a callback function after a specified time interval until it is stopped.

🔑 **Key Points:**

- Repeated Execution
- Timer Function
- Callback Function
- Milliseconds
- `clearInterval()`

💻 **Syntax:**

```js
setInterval(callbackFunction, intervalInMilliseconds);
```

💻 **Example:**

```js
let count = 1;

const timer = setInterval(() => {
    console.log("Count:", count);

    count++;

    if (count > 5) {
        clearInterval(timer);
    }
}, 1000);
```

**Output:**

```js
Count: 1
Count: 2
Count: 3
Count: 4
Count: 5
```

**Explanation:**

- `1000` means approximately 1 second.
- The callback executes repeatedly.
- `clearInterval()` stops the repeated execution.

🎯 **Interview Answer:**

setInterval is a timer function that repeatedly executes a callback after a specified interval. We use clearInterval to stop its execution.

<h2  class="answer-heading" id="3.10">3.10 What is `setImmediate()`?</h2>

📌 **Definition:**

`setImmediate()` is a Node.js timer function that schedules a callback to execute in the **check phase of the event loop**, after the poll phase.

🔑 **Key Points:**

- Node.js Specific
- Event Loop
- Check Phase
- Callback Scheduling
- `clearImmediate()`

💻 **Syntax:**

```js
setImmediate(callbackFunction);
```

💻 **Example:**

```js
console.log("Start");

setImmediate(() => {
    console.log("Immediate Callback");
});

console.log("End");
```

**Output:**

```js
Start
End
Immediate Callback
```

**Explanation:**

1. `Start` executes first.
2. `setImmediate()` schedules its callback.
3. `End` executes.
4. The callback executes in the check phase of the event loop.

**Important:** Don't assume `setImmediate()` always executes before `setTimeout(fn, 0)` when both are scheduled from the main module. Their relative order can be non-deterministic.

🎯 **Interview Answer:**

setImmediate is a Node.js timer function that schedules a callback to execute in the check phase of the event loop. It is commonly used to schedule work for a later event-loop iteration.

<h2  class="answer-heading" id="3.11">3.11 What is `process.env`?</h2>

📌 **Definition:**

`process.env` is an object that provides access to environment variables available to the running Node.js process.

We use it to store and access application configuration such as database credentials, API keys, and server ports.

🔑 **Key Points:**

- Environment Variables
- Application Configuration
- Database Credentials
- API Keys
- Deployment Configuration
- Security

💻 **Syntax:**

```js
process.env.VARIABLE_NAME;
```

💻 **Example:**

**.env file**

```js
PORT=3000
DB_HOST=localhost
DB_USER=root
```

**app.js**

```js
require("dotenv").config();

const port = process.env.PORT;

const databaseHost = process.env.DB_HOST;

console.log(port);

console.log(databaseHost);
```

**Output:**

```js
3000
localhost
```

**Important Key Points:**

- `process.env` reads environment variables.
- `.env` is a file used to store local environment configuration.
- `dotenv` loads `.env` values into `process.env`.
- Never expose sensitive credentials in GitHub.
- Environment variable values are generally strings.

🎯 **Interview Answer:**

process.env is used to access environment variables in Node.js. We use it to manage configuration such as database credentials, API keys, and server ports without hardcoding them in the application.

<h2  class="answer-heading" id="3.12">3.12 What is `process.argv`?</h2>

📌 **Definition:**

`process.argv` is an array that contains command-line arguments passed when starting a Node.js application.

🔑 **Key Points:**

- Command-line Arguments
- Array
- Runtime Input
- User Input

**Array Structure:**

| Index             | Description             |
| ----------------- | ----------------------- |
| `process.argv[0]` | Node.js executable path |
| `process.argv[1]` | JavaScript file path    |
| `process.argv[2]` | First custom argument   |
| `process.argv[3]` | Second custom argument  |

💻 **Example:**

**app.js**

```js
const name = process.argv[2];

const age = process.argv[3];

console.log("Name:", name);

console.log("Age:", age);
```

**Run:**

```js
node app.js Gopi 26
```

**Output:**

```js
Name: Gopi
Age: 26
```

🎯 **Interview Answer:**

process.argv is an array used to access command-line arguments passed when running a Node.js application. It is useful for accepting dynamic input from the terminal.

<h2  class="answer-heading" id="3.13">3.13 What is `process.exit()`?</h2>

📌 **Definition:**

`process.exit()` is a method used to terminate the currently running Node.js process immediately.

🔑 **Key Points:**

- Process Termination
- Exit Code
- Runtime Control
- Error Handling

**Common Exit Codes:**

| Exit Code   | Meaning                                             |
| ----------- | --------------------------------------------------- |
| `0`         | Successful execution                                |
| `1`         | General application error                           |
| Other codes | Application-specific or system-related exit reasons |

💻 **Syntax:**

```js
process.exit(exitCode);
```

💻 **Example:**

```js
const isDatabaseConnected = false;

if (!isDatabaseConnected) {
    console.log("Database connection failed");

    process.exit(1);
}

console.log("Application started");
```

**Output:**

```js
Database connection failed
```

**Explanation:**

- If the database connection fails, the process terminates.
- Exit code `1` indicates an unsuccessful termination.
- The remaining code will not execute.

**Important:** `process.exit()` terminates immediately and may interrupt pending asynchronous operations or output. In production applications, prefer graceful shutdown where possible.

🎯 **Interview Answer:**

process.exit() is used to terminate a running Node.js process. Exit code 0 indicates success, while a non-zero exit code generally indicates an error or unsuccessful execution.

<h2  class="answer-heading" id="3.14">3.14 What is the difference between `global` and `window`?</h2>

📌 **Definition:**

`global` is the global object in Node.js, whereas `window` is the global object representing the browser window in web browsers.

🔑 **Key Points:**

| `global`                           | `window`                   |
| ---------------------------------- | -------------------------- |
| Available in Node.js               | Available in browsers      |
| Represents Node.js global scope    | Represents browser window  |
| Provides Node.js global properties | Provides browser APIs      |
| No DOM APIs by default             | Provides DOM access        |
| Example: `global.process`          | Example: `window.document` |

💻 **Example:**

**Node.js:**

```js
console.log(global);

console.log(global.process.version);
```

**Browser:**

```js
console.log(window);

console.log(window.location.href);

console.log(window.document.title);
```

**Important:**

In modern JavaScript, `globalThis` provides a standard way to access the global object across different JavaScript environments.

```js
console.log(globalThis);
```

- Node.js → `globalThis` refers to the Node.js global object.
- Browser → `globalThis` refers to the browser's global object (`window`).

🎯 **Interview Answer:**

Global is the global object in Node.js, whereas window is the global object in browsers. Node.js provides server-side APIs, while window provides browser APIs such as DOM and location.

<h2  class="answer-heading" id="3.15">3.15 Are `__dirname` and `__filename` available in ES Modules?</h2>

Important interview question

📌 **Definition:**

No. `__dirname` and `__filename` are not available directly in ES Modules because they are CommonJS module variables.

In ES Modules, we can use `import.meta.url` with Node.js URL and path utilities to get the current file and directory paths.

🔑 **Key Points:**

- CommonJS
- ES Modules (ESM)
- `__dirname`
- `__filename`
- `import.meta.url`
- `fileURLToPath()`
- `dirname()`

### **CommonJS Example**

```js
// app.js (CommonJS)

console.log(__dirname);

console.log(__filename);
```

### **ES Modules Example**

```js
// app.mjs

import path from "node:path";
import { fileURLToPath } from "node:url";

const __filename = fileURLToPath(import.meta.url);

const __dirname = path.dirname(__filename);

console.log("File:", __filename);

console.log("Directory:", __dirname);
```

**Explanation:**

1. `import.meta.url` gives the current module's URL.
2. `fileURLToPath()` converts the file URL into a filesystem path.
3. `path.dirname()` extracts the directory path.

**Output (example):**

```js
File: /home/gopi/project/app.mjs

Directory: /home/gopi/project
```

🎯 **Interview Answer:**

No, `__dirname` and `__filename` are not directly available in ES Modules. They are CommonJS variables. In ES Modules, we use `import.meta.url`, `fileURLToPath()`, and `path.dirname()` to get the equivalent file and directory paths.



<h2  class="answer-heading" id="7.1">7.1 What is event-driven programming?</h2>

📌 **Definition:**

Event-driven programming is a programming approach where the application executes specific functions when an event occurs.

Instead of executing everything in a fixed sequence, the application waits for events and responds when they happen.

🔑 **Key Points:**

- Event-driven Architecture
- Events
- Event Listeners
- Event Handlers
- EventEmitter
- Callback Functions

💻 **Example:**

```js
const EventEmitter = require("events");

const eventEmitter = new EventEmitter();

// Listen for an event
eventEmitter.on("userLogin", () => {
    console.log("User logged in successfully");
});

// Trigger the event
eventEmitter.emit("userLogin");
```

**Output:**

```js
User logged in successfully
```

⚙️ **How it works:**

1. Create an EventEmitter object.
2. Register an event listener using `on()`.
3. Trigger the event using `emit()`.
4. The registered callback function executes.

🎯 **Interview Answer:**

Event-driven programming is a programming approach where functions are executed in response to events. Node.js uses EventEmitter, event listeners, and callbacks to implement event-driven programming.

<h2  class="answer-heading" id="7.2">7.2 What is an event?</h2>

📌 **Definition:**

An event is an action or occurrence that happens in an application and can trigger a specific function.

For example, user login, payment success, file upload completion, and database connection events.

🔑 **Key Points:**

- Event Occurrence
- Event Name
- Event Listener
- Event Handler
- Callback Function

💻 **Example:**

```js
const EventEmitter = require("events");

const eventEmitter = new EventEmitter();

// Event Listener
eventEmitter.on("paymentSuccess", () => {
    console.log("Payment completed successfully");
});

// Event Trigger
eventEmitter.emit("paymentSuccess");
```

**Output:**

```js
Payment completed successfully
```

**Real-world examples:**

| Event            | When it happens          |
| ---------------- | ------------------------ |
| `userLogin`      | User logs in             |
| `paymentSuccess` | Payment is completed     |
| `orderPlaced`    | Customer places an order |
| `fileUploaded`   | File upload completes    |
| `userRegistered` | New user registers       |

🎯 **Interview Answer:**

An event is an action or occurrence in an application that can trigger a specific function. Examples include user login, payment success, and file upload completion.

<h2  class="answer-heading" id="7.3">7.3 What is EventEmitter?</h2>

📌 **Definition:**

EventEmitter is a class provided by the Node.js `events` module. It allows us to create, listen to, and trigger custom events.

🔑 **Key Points:**

- EventEmitter Class
- Events
- Event Listeners
- `emit()`
- `on()`
- `once()`
- Custom Events

🎯 **Interview Answer:**

EventEmitter is a class from the Node.js events module used to create and handle custom events. It allows different parts of an application to communicate using event listeners and emitters.

<h2  class="answer-heading" id="7.4">7.4 What is the `events` module?</h2>

📌 **Definition:**

The `events` module is a built-in Node.js module that provides functionality for working with events using the EventEmitter class.

We don't need to install it separately because it comes with Node.js.

🔑 **Key Points:**

- Built-in Module
- EventEmitter
- Custom Events
- Event Listeners
- Event Handling

💻 **Syntax:**

```js
const EventEmitter = require("events");
```

Using ES Modules:

```js
import { EventEmitter } from "node:events";
```

💻 **Example:**

```js
const EventEmitter = require("events");

const eventEmitter = new EventEmitter();

eventEmitter.on("message", () => {
    console.log("New message received");
});

eventEmitter.emit("message");
```

**Output:**

```js
New message received
```

🎯 **Interview Answer:**

The events module is a built-in Node.js module that provides the EventEmitter class. We use it to create custom events, register listeners, and trigger event-based communication.

<h2  class="answer-heading" id="7.5">7.5 What is `emit()`?</h2>

📌 **Definition:**

`emit()` is a method of the EventEmitter class used to trigger or fire an event.

We can also pass data (arguments) to the event listeners when triggering an event.

🔑 **Key Points:**

- Event Triggering
- Event Name
- Event Arguments
- Event Listener
- EventEmitter

💻 **Syntax:**

```js
eventEmitter.emit(eventName, argument1, argument2);
```

💻 **Example:**

```js
const EventEmitter = require("events");

const eventEmitter = new EventEmitter();

// Register event listener
eventEmitter.on("userRegistered", (name, email) => {
    console.log("Name:", name);
    console.log("Email:", email);
});

// Trigger event with data
eventEmitter.emit(
    "userRegistered",
    "Gopi",
    "gopi@gmail.com"
);
```

**Output:**

```js
Name: Gopi
Email: gopi@gmail.com
```

⚙️ **How it works:**

1. `on()` registers the event listener.
2. `emit()` triggers the event.
3. The supplied arguments are passed to the listener.
4. The listener executes.

🎯 **Interview Answer:**

`emit()` is an EventEmitter method used to trigger an event. We can pass additional arguments to send data to the registered event listeners.

<h2  class="answer-heading" id="7.6">7.6 What is `on()`?</h2>

📌 **Definition:**

`on()` is a method of the EventEmitter class used to register an event listener.

Whenever the specified event is emitted, the registered callback function executes.

🔑 **Key Points:**

- Event Listener
- Event Registration
- Callback Function
- Multiple Executions
- Event Name

💻 **Syntax:**

```js
eventEmitter.on(eventName, callbackFunction);
```

💻 **Example:**

```js
const EventEmitter = require("events");

const eventEmitter = new EventEmitter();

// Register listener
eventEmitter.on("userLogin", (username) => {
    console.log(`${username} logged in`);
});

// Trigger event
eventEmitter.emit("userLogin", "Gopi");

eventEmitter.emit("userLogin", "Arun");

eventEmitter.emit("userLogin", "Raj");
```

**Output:**

```js
Gopi logged in
Arun logged in
Raj logged in
```

⚙️ **How it works:**

- `on()` registers the callback.
- Every time `userLogin` is emitted, the callback executes.
- The listener remains registered until it is removed.

🎯 **Interview Answer:**

`on()` is used to register an event listener in Node.js. The callback function executes every time the specified event is emitted.

<h2  class="answer-heading" id="7.7">7.7 What is `once()`?</h2>

📌 **Definition:**

`once()` is a method of the EventEmitter class used to register an event listener that executes only one time.

After the first execution, Node.js automatically removes that listener.

🔑 **Key Points:**

- One-time Listener
- Event Registration
- Automatic Removal
- Callback Function
- Single Execution

💻 **Syntax:**

```js
eventEmitter.once(eventName, callbackFunction);
```

💻 **Example:**

```js
const EventEmitter = require("events");

const eventEmitter = new EventEmitter();

// Register one-time listener
eventEmitter.once("userLogin", (username) => {
    console.log(`${username} logged in`);
});

// Trigger event multiple times
eventEmitter.emit("userLogin", "Gopi");

eventEmitter.emit("userLogin", "Arun");

eventEmitter.emit("userLogin", "Raj");
```

**Output:**

```js
Gopi logged in
```

⚙️ **How it works:**

1. `once()` registers the listener.
2. First `emit()` triggers the callback.
3. Node.js automatically removes the listener.
4. Subsequent events do not execute that listener.

🎯 **Interview Answer:**

`once()` registers an event listener that executes only once. After its first execution, Node.js automatically removes the listener.

<h2  class="answer-heading" id="7.8">7.8 What is `removeListener()`?</h2>

📌 **Definition:**

`removeListener()` is a method of the EventEmitter class used to remove a previously registered event listener.

We need to provide the same event name and callback function that were used to register the listener.

🔑 **Key Points:**

- Remove Event Listener
- Event Name
- Callback Reference
- Listener Management
- Memory Management

💻 **Syntax:**

```js
eventEmitter.removeListener(eventName, callbackFunction);
```

💻 **Example:**

```js
const EventEmitter = require("events");

const eventEmitter = new EventEmitter();

// Create listener function
function userLogin(username) {
    console.log(`${username} logged in`);
}

// Register listener
eventEmitter.on("login", userLogin);

// Trigger event
eventEmitter.emit("login", "Gopi");

// Remove listener
eventEmitter.removeListener("login", userLogin);

// Trigger again
eventEmitter.emit("login", "Arun");
```

**Output:**

```js
Gopi logged in
```

⚙️ **How it works:**

1. Create a callback function.
2. Register it using `on()`.
3. Execute it using `emit()`.
4. Remove it using `removeListener()`.
5. Future events will not execute that removed listener.

**Important:** `off()` is an alias for `removeListener()`.

```js
eventEmitter.off("login", userLogin);
```

🎯 **Interview Answer:**

`removeListener()` is used to remove a specific event listener from an EventEmitter. We need to provide the event name and the original callback function reference.

<h2  class="answer-heading" id="7.9">7.9 What is `removeAllListeners()`?</h2>

📌 **Definition:**

`removeAllListeners()` is a method of the EventEmitter class used to remove all registered listeners for a specific event or for all events.

🔑 **Key Points:**

- Remove All Listeners
- Event Cleanup
- Listener Management
- Memory Management
- Optional Event Name

💻 **Syntax:**

```js
// Remove listeners for a specific event
eventEmitter.removeAllListeners(eventName);

// Remove listeners for all events
eventEmitter.removeAllListeners();
```

💻 **Example:**

```js
const EventEmitter = require("events");

const eventEmitter = new EventEmitter();

// Register first event
eventEmitter.on("login", () => {
    console.log("Login event triggered");
});

// Register second event
eventEmitter.on("logout", () => {
    console.log("Logout event triggered");
});

// Remove all listeners for login
eventEmitter.removeAllListeners("login");

// Trigger both events
eventEmitter.emit("login");

eventEmitter.emit("logout");
```

**Output:**

```js
Logout event triggered
```

⚙️ **How it works:**

- `login` listener is removed.
- `logout` listener remains registered.
- When `login` is emitted, nothing happens.
- When `logout` is emitted, its callback executes.

**Important:** Use `removeAllListeners()` carefully. It can remove listeners registered by other parts of your application if they share the same EventEmitter instance.

🎯 **Interview Answer:**

`removeAllListeners()` removes all registered listeners for a particular event or all events from an EventEmitter instance. It is useful for event cleanup, but should be used carefully.

<h2  class="answer-heading" id="7.10">7.10 What is the difference between `on()` and `once()`?</h2>

📌 **Definition:**

Both methods are used to register event listeners, but the main difference is how many times the listener can execute.

🔑 **Difference Table:**

| `on()`                                   | `once()`                                     |
| ---------------------------------------- | -------------------------------------------- |
| Registers a regular listener             | Registers a one-time listener                |
| Executes every time the event is emitted | Executes only once                           |
| Remains registered                       | Automatically removes itself after execution |
| Used for repeated events                 | Used for one-time events                     |

💻 **Example:**

```js
const EventEmitter = require("events");

const eventEmitter = new EventEmitter();

// Regular listener
eventEmitter.on("regularEvent", () => {
    console.log("ON executed");
});

// One-time listener
eventEmitter.once("oneTimeEvent", () => {
    console.log("ONCE executed");
});

// Trigger regular event twice
eventEmitter.emit("regularEvent");
eventEmitter.emit("regularEvent");

// Trigger one-time event twice
eventEmitter.emit("oneTimeEvent");
eventEmitter.emit("oneTimeEvent");
```

**Output:**

```js
ON executed
ON executed
ONCE executed
```

⚙️ **How it works:**

- `on()` executes its callback every time the event is triggered.
- `once()` executes its callback only on the first event.
- The `once()` listener is automatically removed after execution.

🎯 **Interview Answer:**

The main difference is that `on()` executes its callback every time an event is emitted, whereas `once()` executes the callback only once and automatically removes the listener.

<h2  class="answer-heading" id="7.11">7.11 How do you create custom events?</h2>

📌 **Definition:**

We can create custom events in Node.js using the EventEmitter class from the built-in `events` module.

We register a listener using `on()` and trigger the custom event using `emit()`.

🔑 **Key Points:**

- EventEmitter
- Custom Event
- `on()`
- `emit()`
- Callback Function
- Event Arguments

💻 **Syntax:**

```js
const EventEmitter = require("events");

const eventEmitter = new EventEmitter();

// Register custom event
eventEmitter.on("eventName", callbackFunction);

// Trigger custom event
eventEmitter.emit("eventName", data);
```

💻 **Real-world Example: Order Management**

```js
const EventEmitter = require("events");

const eventEmitter = new EventEmitter();

// Listen for order placed event
eventEmitter.on("orderPlaced", (order) => {

    console.log("Order ID:", order.id);

    console.log("Customer:", order.customer);

    console.log("Amount:", order.amount);

});

// Trigger custom event
eventEmitter.emit("orderPlaced", {
    id: 101,
    customer: "Gopi",
    amount: 2500
});
```

**Output:**

```js
Order ID: 101
Customer: Gopi
Amount: 2500
```

⚙️ **How it works:**

1. Import the EventEmitter class.
2. Create an EventEmitter instance.
3. Create a custom event called `orderPlaced`.
4. Register a listener using `on()`.
5. Trigger the event using `emit()`.
6. Pass order information to the listener.

🎯 **Interview Answer:**

We can create custom events using the EventEmitter class from the events module. We register listeners using `on()` and trigger custom events using `emit()`. We can also pass data through event arguments.

<h2  class="answer-heading" id="7.12">7.12 What is the special `error` event?</h2>

Important interview question

📌 **Definition:**

The `error` event is a special event in Node.js EventEmitter used to handle errors emitted by an EventEmitter instance.

Unlike normal custom events, an `error` event has special behavior when no listener is registered.

🔑 **Key Points:**

- Special Event
- Error Handling
- EventEmitter
- Error Object
- Error Listener
- Unhandled Error

💻 **Example:**

```js
const EventEmitter = require("events");

const eventEmitter = new EventEmitter();

// Register error listener
eventEmitter.on("error", (err) => {
    console.log("Error handled:", err.message);
});

// Trigger error event
eventEmitter.emit("error", new Error("Database connection failed"));
```

**Output:**

```js
Error handled: Database connection failed
```

⚙️ **How it works:**

1. Register an `error` listener.
2. Create an Error object.
3. Trigger the `error` event using `emit()`.
4. The registered listener receives the error.
5. The error is handled inside the callback.

🎯 **Interview Answer:**

The error event is a special EventEmitter event used to handle errors. We can register an error listener to receive and handle Error objects. If an error event is emitted without a listener, Node.js throws the error.

<h2  class="answer-heading" id="7.13">7.13 What happens if an error event has no listener?</h2>

📌 **Definition:**

If an EventEmitter emits an `error` event without a registered error listener, Node.js throws the error as an uncaught exception and the application normally terminates.

🔑 **Key Points:**

- Unhandled Error
- Uncaught Exception
- Application Termination
- Error Listener
- Exception Handling

💻 **Example:**

```js
const EventEmitter = require("events");

const eventEmitter = new EventEmitter();

// No error listener registered

eventEmitter.emit(
    "error",
    new Error("Something went wrong")
);

console.log("Application continues");
```

**Expected behavior:**

```js
Error: Something went wrong
```

The application terminates due to the unhandled error. The final `console.log()` will not execute.

**Correct Approach:**

```js
const EventEmitter = require("events");

const eventEmitter = new EventEmitter();

// Register error listener
eventEmitter.on("error", (err) => {
    console.error("Handled error:", err.message);
});

// Emit error
eventEmitter.emit(
    "error",
    new Error("Database connection failed")
);

console.log("Application continues");
```

**Output:**

```js
Handled error: Database connection failed
Application continues
```

⚙️ **Important Technical Point:**

- An unhandled EventEmitter `error` event throws synchronously from `emit()`.
- Registering an error listener prevents this specific unhandled-error behavior.
- It does not automatically handle every other asynchronous error in your application.

🎯 **Interview Answer:**

If an error event is emitted without a registered error listener, Node.js throws it as an uncaught exception, which normally terminates the application. Therefore, we should register proper error listeners.



## **Important EventEmitter Methods – Syntax Reference**

Keep this code for quick interview revision.

```js
const EventEmitter = require("events");

const eventEmitter = new EventEmitter();

// 1. Register listener
eventEmitter.on("eventName", callbackFunction);

// 2. Register one-time listener
eventEmitter.once("eventName", callbackFunction);

// 3. Trigger event
eventEmitter.emit("eventName", data);

// 4. Remove specific listener
eventEmitter.removeListener("eventName", callbackFunction);

// 5. Alternative to removeListener
eventEmitter.off("eventName", callbackFunction);

// 6. Remove all listeners for an event
eventEmitter.removeAllListeners("eventName");

// 7. Remove all listeners
eventEmitter.removeAllListeners();

// 8. Handle errors
eventEmitter.on("error", (err) => {
    console.log(err.message);
});
```


<h2  class="answer-heading" id="9.1">9.1 What is the HTTP module?</h2>


📌 **Definition:**

The HTTP module is a built-in Node.js module used to create HTTP servers and communicate with clients using the HTTP protocol.

It allows us to receive HTTP requests and send HTTP responses without using external frameworks like Express.js.

🔑 **Key Points:**

- Built-in Module
- HTTP Protocol
- Client-Server Communication
- Request and Response
- HTTP Server
- REST API


🎯 **Interview Answer:**

The HTTP module is a built-in Node.js module used to create HTTP servers and handle client requests and server responses. We can build REST APIs using this module without installing any external package.

<h2  class="answer-heading" id="9.2">9.2 How do you create an HTTP server?</h2>


📌 **Definition:**

We can create an HTTP server in Node.js using the `http.createServer()` method and start it using the `listen()` method.

🔑 **Key Points:**

- HTTP Module
- `createServer()`
- Request Callback
- Request Object
- Response Object
- `listen()`
- Port Number

💻 **Syntax:**

```js
const http = require("node:http");

const server = http.createServer((req, res) => {
    // Handle request
    // Send response
});

server.listen(port, callback);
```

💻 **Example:**

```js
const http = require("node:http");

const server = http.createServer((req, res) => {

    res.writeHead(200, {
        "Content-Type": "text/plain"
    });

    res.end("Welcome to Node.js Server");

});

server.listen(3000, () => {
    console.log("Server running on port 3000");
});
```

**How it works:**

1. Import the HTTP module.
2. Create a server using `http.createServer()`.
3. Receive requests through `req`.
4. Send responses through `res`.
5. Start the server using `server.listen()`.
6. The server listens for incoming requests on port `3000`.

🎯 **Interview Answer:**

We can create an HTTP server using the `http.createServer()` method. It provides request and response objects to handle client communication. We use `server.listen()` to start the server on a specific port.

<h2  class="answer-heading" id="9.3">9.3 What is `http.createServer()`?</h2>


📌 **Definition:**

`http.createServer()` is a method provided by the Node.js HTTP module that creates a new HTTP server.

It accepts a callback function that executes whenever the server receives an incoming request.

🔑 **Key Points:**

- HTTP Server Creation
- Request Listener
- Callback Function
- Request Object (`req`)
- Response Object (`res`)


🎯 **Interview Answer:**

`http.createServer()` is a method used to create an HTTP server. It accepts a callback function with request and response objects, allowing us to handle incoming client requests and send responses.

<h2  class="answer-heading" id="9.4">9.4 What is a request object?</h2>


📌 **Definition:**

The request object (`req`) contains information sent by the client to the Node.js server.

It provides details such as the HTTP method, requested URL, headers, and request body.

🔑 **Key Points:**

- Incoming Request
- HTTP Method
- Request URL
- Request Headers
- Request Body
- Client Information

**Important request properties:**

| Property          | Purpose                                |
| ----------------- | -------------------------------------- |
| `req.method`      | Returns HTTP method                    |
| `req.url`         | Returns requested URL                  |
| `req.headers`     | Returns request headers                |
| `req.httpVersion` | Returns HTTP version                   |
| `req.socket`      | Provides underlying socket information |

💻 **Example:**

```js
const http = require("node:http");

const server = http.createServer((req, res) => {

    console.log("Method:", req.method);

    console.log("URL:", req.url);

    console.log("Headers:", req.headers);

    res.end("Request received");

});

server.listen(3000);
```

**Example output when visiting&#x20;**`/users`**:**

```js
Method: GET
URL: /users
Headers: {
  host: 'localhost:3000',
  connection: 'keep-alive'
}
```

🎯 **Interview Answer:**

The request object represents the incoming HTTP request from the client. It contains information such as the request method, URL, headers, and body.

<h2  class="answer-heading" id="9.5">9.5 What is a response object?</h2>


📌 **Definition:**

The response object (`res`) is used by the Node.js server to send an HTTP response back to the client.

It allows us to set status codes, response headers, and response data.

🔑 **Key Points:**

- HTTP Response
- Status Code
- Response Headers
- Response Body
- `res.write()`
- `res.end()`
- `res.setHeader()`

💻 **Example:**

```js
const http = require("node:http");

const server = http.createServer((req, res) => {

    res.statusCode = 200;

    res.setHeader("Content-Type", "text/plain");

    res.end("Welcome Gopi");

});

server.listen(3000);
```

**Explanation:**

1. `res.statusCode = 200` sets the HTTP status.
2. `res.setHeader()` sets the response header.
3. `res.end()` sends the response and completes it.

🎯 **Interview Answer:**

The response object is used to send data from the server to the client. It allows us to set HTTP status codes, response headers, and response body content.

<h2  class="answer-heading" id="9.6">9.6 What is `req.method`?</h2>


📌 **Definition:**

`req.method` is a property of the request object that returns the HTTP method used by the client.

It helps the server identify what type of operation the client wants to perform.

🔑 **Key Points:**

- HTTP Methods
- GET
- POST
- PUT
- PATCH
- DELETE
- Request Handling

💻 **Example:**

```js
const http = require("node:http");

const server = http.createServer((req, res) => {

    console.log(req.method);

    if (req.method === "GET") {
        res.end("Fetching data");
    }

    else if (req.method === "POST") {
        res.end("Creating data");
    }

    else {
        res.end("Method not supported");
    }

});

server.listen(3000);
```

**Example:**

When the client sends a GET request:

```js
GET
Fetching data
```

When the client sends a POST request:

```js
POST
Creating data
```

🎯 **Interview Answer:**

`req.method` is a request object property that returns the HTTP method used by the client, such as GET, POST, PUT, PATCH, or DELETE. We use it to handle different types of requests.

<h2  class="answer-heading" id="9.7">9.7 What is `req.url`?</h2>


📌 **Definition:**

`req.url` is a property of the request object that returns the requested URL path, including the query string, as received by the server.

It helps identify which resource or API endpoint the client wants to access.

🔑 **Key Points:**

- Request URL
- API Endpoint
- URL Path
- Query Parameters
- Route Handling

💻 **Example:**

```js
const http = require("node:http");

const server = http.createServer((req, res) => {

    console.log(req.url);

    if (req.url === "/users") {
        res.end("Users API");
    }

    else if (req.url === "/products") {
        res.end("Products API");
    }

    else {
        res.end("Route not found");
    }

});

server.listen(3000);
```

**Example URLs:**

```js
http://localhost:3000/users
http://localhost:3000/products
```

**Output:**

```js
/users
/products
```

**Practical Example – Query Parameters:**

```js
const http = require("node:http");

const server = http.createServer((req, res) => {

    const url = new URL(req.url, "http://localhost:3000");

    const name = url.searchParams.get("name");

    res.end(`Hello ${name}`);

});

server.listen(3000);
```

Request:

```js
http://localhost:3000/users?name=Gopi
```

Output:

```js
Hello Gopi
```

🎯 **Interview Answer:**

`req.url` returns the requested URL path and query string. We use it to identify API endpoints and extract query parameters from incoming requests.

<h2  class="answer-heading" id="9.8">9.8 What is `req.headers`?</h2>


📌 **Definition:**

`req.headers` is a property of the request object that contains all HTTP headers sent by the client to the server.

Headers provide additional information about the request, such as content type, authorization token, accepted response format, and client details.

🔑 **Key Points:**

- Request Headers
- Content-Type
- Authorization
- Accept
- User-Agent
- Host
- Authentication

**Important request headers:**

| Header          | Purpose                                   |
| --------------- | ----------------------------------------- |
| `content-type`  | Describes request body format             |
| `authorization` | Sends authentication credentials or token |
| `accept`        | Specifies acceptable response formats     |
| `user-agent`    | Identifies the client                     |
| `host`          | Specifies the target host                 |

💻 **Example:**

```js
const http = require("node:http");

const server = http.createServer((req, res) => {

    console.log("Content Type:", req.headers["content-type"]);

    console.log("Authorization:", req.headers.authorization);

    console.log("User Agent:", req.headers["user-agent"]);

    res.end("Headers received");

});

server.listen(3000);
```

**Example request headers:**

```js
Content-Type: application/json
Authorization: Bearer abc123
```

**Important:** Node.js normalizes incoming header names to lowercase in `req.headers`.

🎯 **Interview Answer:**

`req.headers` is a property that contains HTTP headers sent by the client. We use it to access information such as content type, authorization token, accepted response format, and client details.

<h2  class="answer-heading" id="9.9">9.9 What is `res.write()`?</h2>


📌 **Definition:**

`res.write()` is a response method used to send data chunks to the client without ending the response immediately.

We can call it multiple times to send multiple chunks of data.

🔑 **Key Points:**

- Response Data
- Data Chunks
- Streaming
- HTTP Response
- Response Body

💻 **Syntax:**

```js
res.write(data);
```

💻 **Example:**

```js
const http = require("node:http");

const server = http.createServer((req, res) => {

    res.write("Hello ");

    res.write("Gopi ");

    res.write("Welcome to Node.js");

    res.end();

});

server.listen(3000);
```

**Output in browser:**

```js
Hello Gopi Welcome to Node.js
```

⚙️ **How it works:**

1. First `res.write()` sends the first chunk.
2. Second `res.write()` sends another chunk.
3. Third `res.write()` sends the final data chunk.
4. `res.end()` finishes the response.

**Real-world usage:** Streaming large files, sending continuous data, and handling streaming responses.

🎯 **Interview Answer:**

`res.write()` is used to send response data in chunks to the client. It does not finish the response, so we use `res.end()` to complete it.

<h2  class="answer-heading" id="9.10">9.10 What is `res.end()`?</h2>


📌 **Definition:**

`res.end()` is a response method used to finish the HTTP response and indicate that the server has completed sending data to the client.

We can also send the final response data directly through `res.end()`.

🔑 **Key Points:**

- End Response
- Complete HTTP Response
- Response Body
- Final Data Chunk
- Response Completion

💻 **Syntax:**

```js
res.end();
res.end(data);
```

💻 **Example:**

```js
const http = require("node:http");

const server = http.createServer((req, res) => {
    res.write("Hello ");
    res.write("Gopi");
    res.end(" Welcome!");

});

server.listen(3000);
```

**Output:**

```js
Hello Gopi Welcome!
```

⚙️ **How it works:**

- `res.write()` sends response chunks.
- `res.end()` sends the final optional data.
- The HTTP response is completed.
- We should not write additional response data after ending it.

🎯 **Interview Answer:**

`res.end()` is used to complete an HTTP response. It can also send the final response data to the client. After calling it, the response is finished.

<h2  class="answer-heading" id="9.11">9.11 What is `res.setHeader()`?</h2>


📌 **Definition:**

`res.setHeader()` is a response method used to set HTTP response headers before sending the response.

It provides additional information about the response, such as content type, caching rules, and security policies.

🔑 **Key Points:**

- Response Headers
- Content-Type
- Cache-Control
- Security Headers
- HTTP Response

💻 **Syntax:**

```js
res.setHeader(headerName, headerValue);
```

💻 **Example:**

```js
const http = require("node:http");

const server = http.createServer((req, res) => {

    res.setHeader("Content-Type", "application/json");

    res.setHeader("Cache-Control", "no-store");

    const user = {
        id: 1,
        name: "Gopi"
    };

    res.end(JSON.stringify(user));

});

server.listen(3000);
```

**Response:**

```js
{
    "id": 1,
    "name": "Gopi"
}
```

**Important:** `res.setHeader()` should be called before the response headers are sent. After headers are sent, changing them is not allowed.

🎯 **Interview Answer:**

`res.setHeader()` is used to set HTTP response headers before sending the response. For example, we use it to specify Content-Type, Cache-Control, and other response-related information.

<h2  class="answer-heading" id="9.12">9.12 What is the difference between HTTP and HTTPS?</h2>


📌 **Definition:**

HTTP stands for Hypertext Transfer Protocol, while HTTPS stands for Hypertext Transfer Protocol Secure.

HTTPS is the secure version of HTTP. It uses TLS encryption to protect communication between the client and server.

🔑 **Key Points:**

- HTTP – Hypertext Transfer Protocol
- HTTPS – Hypertext Transfer Protocol Secure
- TLS – Transport Layer Security
- SSL – Secure Sockets Layer (legacy term)
- Encryption
- Authentication
- Data Integrity
- Digital Certificate

**Difference Table:**

| HTTP                                | HTTPS                             |
| ----------------------------------- | --------------------------------- |
| Not encrypted by itself             | Uses TLS encryption               |
| Data can be intercepted more easily | Protects data during transmission |
| Uses port 80 by default             | Uses port 443 by default          |
| No TLS certificate required         | Requires a valid TLS certificate  |
| Less secure                         | More secure                       |

💻 **Node.js Example:**

**HTTP Server:**

```js
const http = require("node:http");

const server = http.createServer((req, res) => {

    res.end("HTTP Server");

});

server.listen(3000);
```

**HTTPS Server:**

```js
const https = require("node:https");
const fs = require("node:fs");

const options = {
    key: fs.readFileSync("private-key.pem"),
    cert: fs.readFileSync("certificate.pem")
};

const server = https.createServer(options, (req, res) => {
    res.end("HTTPS Server");
});

server.listen(443);
```

🎯 **Interview Answer:**

HTTP is a protocol used for communication between clients and servers. HTTPS is the secure version of HTTP that uses TLS encryption to protect data during transmission. HTTP commonly uses port 80, while HTTPS uses port 443.

<h2  class="answer-heading" id="9.13">9.13 What are HTTP status codes?</h2>


📌 **Definition:**

HTTP status codes are three-digit numbers returned by the server to indicate the result of a client's HTTP request.

They tell the client whether the request was successful, redirected, failed because of a client error, or failed because of a server error.

🔑 **Key Points:**

- HTTP Response
- Status Code
- Client Error
- Server Error
- Success Response
- Redirection

### Important HTTP Status Code Categories

| Category | Meaning       |
| -------- | ------------- |
| 1xx      | Informational |
| 2xx      | Success       |
| 3xx      | Redirection   |
| 4xx      | Client Error  |
| 5xx      | Server Error  |

### Important Status Codes

| Code | Name                  | Usage                              |
| ---- | --------------------- | ---------------------------------- |
| 200  | OK                    | Request successful                 |
| 201  | Created               | Resource successfully created      |
| 202  | Accepted              | Request accepted for processing    |
| 204  | No Content            | Successful response without body   |
| 301  | Moved Permanently     | Permanent redirection              |
| 302  | Found                 | Temporary redirection              |
| 304  | Not Modified          | Cached resource can be reused      |
| 400  | Bad Request           | Invalid request                    |
| 401  | Unauthorized          | Authentication required or invalid |
| 403  | Forbidden             | Access denied                      |
| 404  | Not Found             | Resource not found                 |
| 405  | Method Not Allowed    | HTTP method not supported          |
| 409  | Conflict              | Resource conflict                  |
| 422  | Unprocessable Content | Validation error                   |
| 429  | Too Many Requests     | Rate limit exceeded                |
| 500  | Internal Server Error | Unexpected server error            |
| 502  | Bad Gateway           | Invalid upstream response          |
| 503  | Service Unavailable   | Server temporarily unavailable     |
| 504  | Gateway Timeout       | Upstream server timeout            |

💻 **Example:**

```js
const http = require("node:http");

const server = http.createServer((req, res) => {

    if (req.url === "/users") {

        res.statusCode = 200;

        res.end("Users fetched successfully");

    } else {

        res.statusCode = 404;

        res.end("User route not found");

    }

});

server.listen(3000);
```

**Explanation:**

- `/users` returns status code `200`.
- Unknown routes return status code `404`.

🎯 **Interview Answer:**

HTTP status codes are three-digit numbers used by the server to communicate the result of an HTTP request. They are categorized into informational, success, redirection, client error, and server error responses.

<h2  class="answer-heading" id="9.14">9.14 What is the difference between GET, POST, PUT, PATCH, and DELETE?</h2>


📌 **Definition:**

GET, POST, PUT, PATCH, and DELETE are HTTP methods used to perform different operations on server resources.

🔑 **Key Points:**

- GET – Retrieve Data
- POST – Create new data
- PUT – Replace existing data
- PATCH – Partially Update Data
- DELETE – Delete data    
- REST API
- HTTP Methods


### Real-world Example

Imagine we have this user:

```js
{
    "id": 1,
    "name": "Gopi",
    "email": "gopi@gmail.com",
    "age": 26
}
```

**1. GET – Fetch User**

```js
GET /users/1
```

Purpose: Retrieve user information.

**2. POST – Create User**

```js
POST /users
```

Request body:

```js
{
    "name": "Arun",
    "email": "arun@gmail.com",
    "age": 25
}
```

Purpose: Create a new user.

**3. PUT – Replace User**

```js
PUT /users/1
```

Request body:

```js
{
    "name": "Gopi Raj",
    "email": "gopi@gmail.com",
    "age": 27
}
```

Purpose: Replace the existing user representation with the supplied data.

**4. PATCH – Partially Update User**

```js
PATCH /users/1
```

Request body:

```js
{
    "age": 27
}
```

Purpose: Update only the age field.

**5. DELETE – Remove User**

```js
DELETE /users/1
```

Purpose: Delete the user with ID 1.


<h2  class="answer-heading" id="9.15">9.15 What are request headers and response headers?</h2>


📌 **Definition:**

Request headers are additional information sent by the client to the server, whereas response headers are additional information sent by the server back to the client.

Both are used to provide metadata about HTTP communication.

🔑 **Key Points:**

- Request Metadata
- Response Metadata
- Content-Type
- Authorization
- Accept
- Cache-Control
- Set-Cookie

### Difference Table

| Request Headers               | Response Headers             |
| ----------------------------- | ---------------------------- |
| Sent by the client            | Sent by the server           |
| Describe the incoming request | Describe the server response |
| Access using `req.headers`    | Set using `res.setHeader()`  |
| Contains Authorization        | Can contain Set-Cookie       |
| Contains Accept               | Contains Content-Type        |

### Common Request Headers

| Header          | Purpose                    |
| --------------- | -------------------------- |
| `Content-Type`  | Format of request body     |
| `Authorization` | Authentication credentials |
| `Accept`        | Expected response format   |
| `User-Agent`    | Client information         |
| `Host`          | Target server hostname     |

### Common Response Headers

| Header                        | Purpose                              |
| ----------------------------- | ------------------------------------ |
| `Content-Type`                | Format of response body              |
| `Cache-Control`               | Caching instructions                 |
| `Set-Cookie`                  | Sends cookies to browser             |
| `Access-Control-Allow-Origin` | Controls allowed cross-origin access |
| `Content-Length`              | Response body size in bytes          |

💻 **Example:**

```js
const http = require("node:http");

const server = http.createServer((req, res) => {

    // Read request headers
    const contentType = req.headers["content-type"];

    const authorization = req.headers.authorization;

    console.log("Request Content-Type:", contentType);

    console.log("Authorization:", authorization);

    // Set response headers
    res.setHeader("Content-Type", "application/json");

    res.setHeader("Cache-Control", "no-store");

    // Send response
    res.end(JSON.stringify({
        message: "Request received successfully"
    }));

});

server.listen(3000);
```

🎯 **Interview Answer:**

Request headers are sent from the client to the server and contain information such as authorization and content type. Response headers are sent from the server to the client and contain information such as response content type, caching instructions, and cookies.

<h2  class="answer-heading" id="9.16">9.16 What is the request-response lifecycle?</h2>


📌 **Definition:**

The request-response lifecycle describes the complete process of communication between a client and a server, starting when the client sends an HTTP request and ending when the server sends an HTTP response.


🎯 **Interview Answer:**

The request-response lifecycle starts when a client sends an HTTP request to the server. Node.js receives and processes the request, performs the required business logic or database operations, and sends an HTTP response containing a status code, headers, and response data.

<h2  class="answer-heading" id="9.17">9.17 How do you parse JSON request bodies without Express?</h2>


Important practical interview question

📌 **Definition:**

In Node.js, we can parse JSON request bodies without Express by using the request object's data stream.

We listen to the `data` event to collect incoming chunks and the `end` event to parse the complete JSON data using `JSON.parse()`.

🔑 **Key Points:**

- Request Body
- Data Stream
- `req.on("data")`
- `req.on("end")`
- `JSON.parse()`
- JSON Parsing
- Error Handling

### **Syntax**

```js
let body = "";

req.on("data", (chunk) => {
    body += chunk;
});

req.on("end", () => {
    const data = JSON.parse(body);
});
```

### **Practical Example**

**app.js**

```js
const http = require("node:http");

const server = http.createServer((req, res) => {

    if (req.method === "POST" && req.url === "/users") {

        let body = "";

        // Collect incoming data chunks
        req.on("data", (chunk) => {
            body += chunk;
        });

        // Process complete request body
        req.on("end", () => {

            try {

                // Convert JSON string into JavaScript object
                const user = JSON.parse(body);

                console.log(user);

                res.writeHead(201, {
                    "Content-Type": "application/json"
                });

                res.end(JSON.stringify({
                    message: "User created successfully",
                    user: user
                }));

            } catch (error) {

                res.writeHead(400, {
                    "Content-Type": "application/json"
                });

                res.end(JSON.stringify({
                    message: "Invalid JSON data"
                }));

            }

        });

    } else {

        res.writeHead(404, {
            "Content-Type": "application/json"
        });

        res.end(JSON.stringify({
            message: "Route not found"
        }));

    }

});

server.listen(3000, () => {
    console.log("Server running on port 3000");
});
```

### **⚙️ How does it work?**

1. `req.on("data")` receives incoming request body chunks.
2. `body += chunk` collects the chunks into one string.
3. `req.on("end")` executes after the complete request body has been received.
4. `JSON.parse(body)` converts the JSON string into a JavaScript object.
5. `try...catch` handles invalid JSON.
6. `res.end()` sends the API response.

## **9.18 How do you handle HTTP errors?**

📌 **Definition:**

HTTP error handling means identifying errors during request processing and sending appropriate HTTP status codes and error messages to the client.

In Node.js, we can handle errors using conditional checks, try-catch blocks, and centralized error-handling functions.

<h2  class="answer-heading" id="10.1">10.1 What is synchronous execution?</h2>


📌 **Definition:**

Synchronous execution means executing code one line at a time. Each operation must finish before the next operation starts.

💻 **Example:**

```js
console.log("Task 1");
console.log("Task 2");
console.log("Task 3");
```

**Output:**

```js
Task 1
Task 2
Task 3
```

⚙️ **How it works:**

1. Executes Task 1.
2. After Task 1 finishes, executes Task 2.
3. After Task 2 finishes, executes Task 3.

🎯 **Interview Answer:**

Synchronous execution means code runs sequentially, and each operation waits for the previous operation to complete.

<h2  class="answer-heading" id="10.2">10.2 What is asynchronous execution?</h2>


📌 **Definition:**

Asynchronous execution allows a program to start an operation and continue executing other code without waiting for that operation to finish.

💻 **Example:**

```js
console.log("Task 1");

setTimeout(() => {
    console.log("Task 2");
}, 2000);

console.log("Task 3");
```

**Output:**

```js
Task 1
Task 3
Task 2
```

⚙️ **How it works:**

1. Executes Task 1.
2. Starts the timer without blocking the remaining JavaScript code.
3. Executes Task 3.
4. After approximately 2 seconds, the callback executes.

🎯 **Interview Answer:**

Asynchronous execution allows Node.js to handle time-consuming operations without blocking the execution of other code.

<h2  class="answer-heading" id="10.3">10.3 What is blocking I/O?</h2>


📌 **Definition:**

Blocking I/O means the program must wait until an input/output operation finishes before continuing to the next statement.

💻 **Example:**

```js
const fs = require("fs");

console.log("Task 1");

const data = fs.readFileSync("example.txt", "utf8");

console.log(data);
console.log("Task 2");
```

**Output:**

```js
Task 1
File content
Task 2
```

⚙️ **How it works:**

- `readFileSync()` reads the file synchronously.
- Node.js waits until the file reading finishes.
- Only then does it execute the next statement.

🎯 **Interview Answer:**

Blocking I/O stops the current execution from continuing until an I/O operation is completed.

<h2  class="answer-heading" id="10.4">10.4 What is non-blocking I/O?</h2>


📌 **Definition:**

Non-blocking I/O allows Node.js to start an I/O operation and continue executing other code while waiting for the operation to finish.

💻 **Example:**

```js
const fs = require("fs");

console.log("Task 1");

fs.readFile("example.txt", "utf8", (error, data) => {
    if (error) {
        console.log(error.message);
        return;
    }

    console.log(data);
});

console.log("Task 2");
```

**Possible output:**

```js
Task 1
Task 2
File content
```

⚙️ **How it works:**

1. Starts reading the file.
2. Continues executing the next statement.
3. Once the file is read, the callback is scheduled and executed.

🎯 **Interview Answer:**

Non-blocking I/O allows Node.js to perform I/O operations without blocking the main JavaScript execution.

<h2  class="answer-heading" id="10.5">10.5 What is callback-based programming?</h2>


📌 **Definition:**

A callback is a function passed as an argument to another function. It is called when a particular operation or event occurs.

💻 **Syntax:**

```js
function mainFunction(callback) {
    // Perform an operation

    callback();
}

mainFunction(() => {
    // Callback function
});
```

💻 **Example:**

```js
function getUser(callback) {
    setTimeout(() => {
        const user = {
            id: 1,
            name: "Arun"
        };

        callback(user);
    }, 1000);
}

getUser((user) => {
    console.log(user);
});
```

**Output:**

```js
{ id: 1, name: 'Arun' }
```

⚙️ **How it works:**

1. `getUser()` receives a callback function.
2. It performs an asynchronous operation.
3. After the operation finishes, it calls the callback.
4. The callback receives the user data.

🎯 **Interview Answer:**

Callback-based programming uses functions passed as arguments to handle the result of an operation, especially asynchronous operations.

<h2  class="answer-heading" id="10.6">10.6 What is callback hell?</h2>


📌 **Definition:**

Callback hell happens when multiple nested callbacks make code difficult to read, understand, and maintain.

💻 **Example:**

```js
getUser((user) => {
    getOrders(user.id, (orders) => {
        getPayment(orders[0].id, (payment) => {
            sendEmail(payment, (result) => {
                console.log(result);
            });
        });
    });
});
```

**Problem:**

- Too many nested callbacks.
- Difficult to maintain code.
- Error handling becomes complicated.
- Code readability decreases.

**Solution:** Use Promises or `async/await`.

🎯 **Interview Answer:**

Callback hell is a situation where multiple nested callbacks make asynchronous code difficult to read and maintain. We can avoid it using Promises and async/await.

<h2  class="answer-heading" id="10.7">10.7 What is a Promise?</h2>


📌 **Definition:**

A Promise is a JavaScript object that represents the eventual success or failure of an asynchronous operation.

💻 **Syntax:**

```js
const promise = new Promise((resolve, reject) => {
    // Perform an operation
    if (condition) {
        resolve(value);
    } else {
        reject(error);
    }
});
```

💻 **Example:**

```js
const getUser = new Promise((resolve, reject) => {
    const user = {
        id: 1,
        name: "Arun"
    };

    resolve(user);
});

getUser.then((result) => {
    console.log(result);
});
```

**Output:**

```js
{ id: 1, name: 'Arun' }
```

⚙️ **How it works:**

- `new Promise()` creates a Promise.
- `resolve()` indicates successful completion.
- `reject()` indicates failure.
- `.then()` handles the fulfilled result.

🎯 **Interview Answer:**

A Promise is an object used to handle asynchronous operations. It represents a value that may be available now, later, or never.

<h2  class="answer-heading" id="10.8">10.8 What are Promise states?</h2>


📌 **Definition:**

A Promise has three possible states.

**1. Pending**
Waiting

The asynchronous operation has not completed yet.

**2. Fulfilled**
Success

The asynchronous operation completed successfully.

**3. Rejected**
Failed

The asynchronous operation failed.

💻 **Example:**

```js
const promise = new Promise((resolve, reject) => {
    resolve("Success");
});

promise.then((result) => {
    console.log(result);
});
```

**Output:**

```js
Success
```

🎯 **Interview Answer:**

A Promise has three states: pending, fulfilled, and rejected. Once it becomes fulfilled or rejected, its state cannot change again.

<h2  class="answer-heading" id="10.9">10.9 What is Promise chaining?</h2>


📌 **Definition:**

Promise chaining means connecting multiple `.then()` methods to execute asynchronous operations one after another.

💻 **Syntax:**

```js
promise
    .then((result) => {
        return nextOperation(result);
    })
    .then((result) => {
        return anotherOperation(result);
    })
    .catch((error) => {
        console.log(error);
    });
```

💻 **Example:**

```js
Promise.resolve(10)
    .then((number) => {
        console.log(number);

        return number * 2;
    })
    .then((result) => {
        console.log(result);

        return result + 5;
    })
    .then((finalResult) => {
        console.log(finalResult);
    });
```

**Output:**

```js
10
20
25
```

⚙️ **How it works:**

1. First `.then()` receives `10`.
2. Returns `20`.
3. Second `.then()` receives `20`.
4. Returns `25`.
5. Third `.then()` receives `25`.

🎯 **Interview Answer:**

Promise chaining allows us to execute multiple asynchronous operations sequentially by returning values or Promises from `.then()`.

<h2  class="answer-heading" id="10.10">10.10 What is `async/await`?</h2>


📌 **Definition:**

`async/await` is a modern JavaScript syntax that makes asynchronous code easier to read and write.

- `async` makes a function return a Promise.
- `await` waits for a Promise to settle and gives its fulfilled value or throws its rejection reason.

💻 **Syntax:**

```js
async function functionName() {
    const result = await promise;

    return result;
}
```

💻 **Example:**

```js
function getUser() {
    return new Promise((resolve) => {
        setTimeout(() => {
            resolve({
                id: 1,
                name: "Arun"
            });
        }, 1000);
    });
}

async function displayUser() {
    const user = await getUser();

    console.log(user);
}

displayUser();
```

**Output:**

```js
{ id: 1, name: 'Arun' }
```

⚙️ **How it works:**

1. `displayUser()` starts executing.
2. `await` waits for `getUser()` to settle.
3. The function pauses at that point, but the JavaScript thread is not blocked.
4. After the Promise fulfills, execution continues.

🎯 **Interview Answer:**

Async/await is used to handle Promises with cleaner, more readable code. It allows us to write asynchronous operations in a synchronous-looking style.

<h2  class="answer-heading" id="10.11">10.11 What is the difference between callbacks and Promises?</h2>


📌 **Definition:**

Both callbacks and Promises are used to handle asynchronous operations, but they handle results differently.

| Callbacks                                       | Promises                              |
| ----------------------------------------------- | ------------------------------------- |
| Pass a function as an argument                  | Return a Promise object               |
| Can create nested callback structures           | Support Promise chaining              |
| Error handling often uses error-first callbacks | Use `.catch()`                        |
| Can become difficult to maintain                | Easier to organize asynchronous flows |

💻 **Callback example:**

```js
fs.readFile("example.txt", "utf8", (error, data) => {
    if (error) {
        console.log(error);
        return;
    }

    console.log(data);
});
```

💻 **Promise example:**

```js
fs.promises.readFile("example.txt", "utf8")
    .then((data) => {
        console.log(data);
    })
    .catch((error) => {
        console.log(error);
    });
```

🎯 **Interview Answer:**

Callbacks use functions to handle asynchronous results, whereas Promises provide `.then()` and `.catch()` for better chaining and error handling.

<h2  class="answer-heading" id="10.12">10.12 What is the difference between Promise and async/await?</h2>


📌 **Definition:**

Both handle asynchronous operations. `async/await` is syntax built on top of Promises.

| Promise                                                 | Async/Await                                    |
| ------------------------------------------------------- | ---------------------------------------------- |
| Uses `.then()`                                          | Uses `await`                                   |
| Uses `.catch()`                                         | Commonly uses `try/catch`                      |
| Supports chaining                                       | Looks like sequential code                     |
| Can be convenient for chaining and parallel composition | Often easier to read for sequential operations |

💻 **Promise example:**

```js
getUser()
    .then((user) => {
        console.log(user);
    })
    .catch((error) => {
        console.log(error);
    });
```

💻 **Async/await example:**

```js
async function displayUser() {
    try {
        const user = await getUser();

        console.log(user);
    } catch (error) {
        console.log(error);
    }
}

displayUser();
```

🎯 **Interview Answer:**

Promises handle asynchronous operations using `.then()` and `.catch()`. Async/await is built on Promises and makes asynchronous code easier to read and maintain.

<h2  class="answer-heading" id="10.13">10.13 What is `Promise.all()`?</h2>


📌 **Definition:**

`Promise.all()` executes multiple Promises concurrently and returns a single Promise.

- Resolves when all Promises fulfill.
- Rejects as soon as one of the Promises rejects.
- Results are returned in the original input order.

💻 **Syntax:**

```js
Promise.all([promise1, promise2, promise3])
    .then((results) => {
        console.log(results);
    })
    .catch((error) => {
        console.log(error);
    });
```

💻 **Example:**

```js
const promise1 = Promise.resolve("User");
const promise2 = Promise.resolve("Orders");
const promise3 = Promise.resolve("Payments");

Promise.all([promise1, promise2, promise3])
    .then((results) => {
        console.log(results);
    });
```

**Output:**

```js
["User", "Orders", "Payments"]
```

⚙️ **Real-world example:**

You need to fetch user details, orders, and payment information independently for a dashboard. You can use `Promise.all()` to wait for all three requests.

🎯 **Interview Answer:**

Promise.all() runs multiple Promises concurrently and returns their results when all fulfill. If any Promise rejects, the returned Promise rejects.

<h2  class="answer-heading" id="10.14">10.14 What is `Promise.allSettled()`?</h2>


📌 **Definition:**

`Promise.allSettled()` waits for all Promises to finish, regardless of whether they fulfill or reject.

💻 **Example:**

```js
const promise1 = Promise.resolve("User");
const promise2 = Promise.reject("Orders failed");
const promise3 = Promise.resolve("Payments");

Promise.allSettled([promise1, promise2, promise3])
    .then((results) => {
        console.log(results);
    });
```

**Output:**

```js
[
    { status: "fulfilled", value: "User" },
    { status: "rejected", reason: "Orders failed" },
    { status: "fulfilled", value: "Payments" }
]
```

⚙️ **How it works:**

- Waits for every Promise to settle.
- Does not reject just because one input Promise rejects.
- Returns the status and value or rejection reason for each Promise.

🎯 **Interview Answer:**

Promise.allSettled() waits for all Promises to complete and returns the result of each Promise, whether successful or failed.

<h2  class="answer-heading" id="10.15">10.15 What is `Promise.race()`?</h2>


📌 **Definition:**

`Promise.race()` returns a Promise that settles as soon as the first input Promise settles.

Important: The first one may either fulfill or reject.

💻 **Example:**

```js
const promise1 = new Promise((resolve) => {
    setTimeout(() => resolve("Task 1"), 2000);
});

const promise2 = new Promise((resolve) => {
    setTimeout(() => resolve("Task 2"), 1000);
});

Promise.race([promise1, promise2])
    .then((result) => {
        console.log(result);
    });
```

**Output:**

```js
Task 2
```

⚙️ **How it works:**

- Task 1 takes 2 seconds.
- Task 2 takes 1 second.
- Task 2 settles first.
- `Promise.race()` returns its result.

🎯 **Interview Answer:**

Promise.race() returns the result of the first Promise that settles, whether it fulfills or rejects.

<h2  class="answer-heading" id="10.16">10.16 What is `Promise.any()`?</h2>


📌 **Definition:**

`Promise.any()` returns the first successfully fulfilled Promise. It ignores rejected Promises unless all input Promises reject.

💻 **Example:**

```js
const promise1 = Promise.reject("Server 1 failed");

const promise2 = new Promise((resolve) => {
    setTimeout(() => {
        resolve("Server 2 success");
    }, 1000);
});

const promise3 = Promise.resolve("Server 3 success");

Promise.any([promise1, promise2, promise3])
    .then((result) => {
        console.log(result);
    })
    .catch((error) => {
        console.log(error);
    });
```

**Output:**

```js
Server 3 success
```

⚙️ **How it works:**

- Promise 1 rejects.
- Promise 2 takes 1 second.
- Promise 3 fulfills immediately.
- Promise 3 provides the first successful result.

🎯 **Interview Answer:**

Promise.any() returns the first successfully fulfilled Promise. If all Promises reject, it throws an AggregateError.

<h2  class="answer-heading" id="10.17">10.17 How do you handle asynchronous errors?</h2>


📌 **Definition:**

Asynchronous errors can be handled using `.catch()` with Promises or `try/catch` with async/await.

**Method 1: Promise with&#x20;**`.catch()`

```js
function getUser() {
    return Promise.reject(new Error("User not found"));
}

getUser()
    .then((user) => {
        console.log(user);
    })
    .catch((error) => {
        console.log(error.message);
    });
```

**Output:**

```js
User not found
```

**Method 2: Async/await with&#x20;**`try/catch`

```js
async function displayUser() {
    try {
        const user = await getUser();

        console.log(user);
    } catch (error) {
        console.log(error.message);
    }
}

displayUser();
```

**Output:**

```js
User not found
```

⚙️ **How it works:**

- `try` contains the asynchronous operation.
- `await` throws if the Promise rejects.
- `catch` handles the error.

🎯 **Interview Answer:**

I handle asynchronous errors using `.catch()` with Promises or `try/catch` with async/await to prevent unhandled Promise rejections and handle failures properly.

<h2  class="answer-heading" id="10.18">10.18 What happens if you forget to use `await`?</h2>


📌 **Definition:**

If you forget `await`, the variable receives the Promise object instead of its fulfilled value.

💻 **Example:**

```js
function getUser() {
    return Promise.resolve({
        id: 1,
        name: "Arun"
    });
}

async function displayUser() {
    const user = getUser();

    console.log(user);
}

displayUser();
```

**Output (conceptually):**

```js
Promise { { id: 1, name: 'Arun' } }
```

**Correct code:**

```js
async function displayUser() {
    const user = await getUser();

    console.log(user);
}

displayUser();
```

**Output:**

```js
{ id: 1, name: 'Arun' }
```

⚙️ **Important:**

Forgetting `await` can also cause errors when you try to access properties before the Promise has fulfilled.

🎯 **Interview Answer:**

If we forget `await`, we get a Promise object instead of its resolved value. We should use `await` when we need the result before continuing.

<h2  class="answer-heading" id="10.19">10.19 How do you execute multiple operations sequentially?</h2>


📌 **Definition:**

Sequential execution means one asynchronous operation starts after the previous operation has completed.

💻 **Example using async/await:**

```js
function getUser() {
    return new Promise((resolve) => {
        setTimeout(() => {
            resolve("User fetched");
        }, 1000);
    });
}

function getOrders() {
    return new Promise((resolve) => {
        setTimeout(() => {
            resolve("Orders fetched");
        }, 1000);
    });
}

function getPayments() {
    return new Promise((resolve) => {
        setTimeout(() => {
            resolve("Payments fetched");
        }, 1000);
    });
}

async function executeTasks() {
    const user = await getUser();
    console.log(user);

    const orders = await getOrders();
    console.log(orders);

    const payments = await getPayments();
    console.log(payments);
}

executeTasks();
```

**Output:**

```js
User fetched
Orders fetched
Payments fetched
```

**Sequential execution**

1\. Get User (1 sec)

2\. Get Orders (1 sec)

3\. Get Payments (1 sec)

Illustrative total: approximately 3 seconds.

🎯 **Interview Answer:**

We can execute multiple asynchronous operations sequentially by using `await` one after another. Each operation waits for the previous operation to complete.

<h2  class="answer-heading" id="10.20">10.20 How do you execute multiple operations in parallel?</h2>


📌 **Definition:**

Parallel-style asynchronous execution means starting multiple independent asynchronous operations without waiting for each one to finish before starting the next.

In JavaScript, we commonly use `Promise.all()` for this.

💻 **Example:**

```js
function getUser() {
    return new Promise((resolve) => {
        setTimeout(() => {
            resolve("User fetched");
        }, 1000);
    });
}

function getOrders() {
    return new Promise((resolve) => {
        setTimeout(() => {
            resolve("Orders fetched");
        }, 1000);
    });
}

function getPayments() {
    return new Promise((resolve) => {
        setTimeout(() => {
            resolve("Payments fetched");
        }, 1000);
    });
}

async function executeTasks() {
    const results = await Promise.all([
        getUser(),
        getOrders(),
        getPayments()
    ]);

    console.log(results);
}

executeTasks();
```

**Output:**

```js
[
    "User fetched",
    "Orders fetched",
    "Payments fetched"
]
```

🎯 **Interview Answer:**

We can execute multiple independent asynchronous operations concurrently using `Promise.all()`. It waits until all operations fulfill and returns their results.





<h2  class="answer-heading" id="11.1">11.1 What is the Node.js event loop?</h2>


📌 **Definition:**

The Event Loop is a mechanism in Node.js that manages asynchronous operations and executes their callbacks when they are ready.

**Why do we need it?**

Node.js uses a single main JavaScript thread. The Event Loop helps it handle multiple I/O operations without waiting for each operation to finish.

🎯 **Interview Answer:**

The Event Loop is a mechanism in Node.js that handles asynchronous operations and executes their callbacks when they are ready, allowing Node.js to handle multiple requests efficiently.

<h2  class="answer-heading" id="11.2">11.2 How does the event loop work?</h2>


📌 **Definition:**

The Event Loop continuously checks whether the Call Stack is available and whether asynchronous callbacks are ready to execute.

**Event Loop execution flow:**

**JavaScript Code**

Synchronous statements and function calls

**Call Stack**

Executes JavaScript functions

**Node.js / libuv**

Handles timers and asynchronous I/O

**Callback Queues**

Ready callbacks wait for execution

**Event Loop**

Schedules callbacks when execution can continue

Repeats while the event loop has work

💻 **Example:**

```js
console.log("Start");

setTimeout(() => {
    console.log("Timer callback");
}, 0);

console.log("End");
```

**Output:**

```js
Start
End
Timer callback
```

⚙️ **How it works:**

1. `console.log("Start")` executes.
2. `setTimeout()` registers a timer.
3. `console.log("End")` executes.
4. The timer callback becomes eligible for execution.
5. The Event Loop executes the callback when the required conditions are met.

🎯 **Interview Answer:**

The Event Loop coordinates the Call Stack, asynchronous operations, and callback queues. It executes ready callbacks when the JavaScript execution stack is available.

<h2  class="answer-heading" id="11.3">11.3 What is the call stack?</h2>


📌 **Definition:**

The Call Stack is a data structure that keeps track of function calls during JavaScript execution.

It follows the **LIFO (Last In, First Out)** principle.

💻 **Example:**

```js
function first() {
    console.log("First function");
    second();
}

function second() {
    console.log("Second function");
    third();
}

function third() {
    console.log("Third function");
}

first();
```

**Output:**

```js
First function
Second function
Third function
```


🎯 **Interview Answer:**

The Call Stack is a LIFO data structure that tracks function execution. JavaScript pushes function calls onto the stack and removes them when execution is complete.

<h2  class="answer-heading" id="11.4">11.4 What is the callback queue?</h2>


📌 **Definition:**

The Callback Queue is a queue where certain asynchronous callbacks wait until they can be executed by the Event Loop.

For example, timer callbacks and some I/O callbacks are scheduled for execution through the Event Loop.

💻 **Example:**

```js
console.log("Start");

setTimeout(() => {
    console.log("Callback Queue");
}, 1000);

console.log("End");
```

**Output:**

```js
Start
End
Callback Queue
```

⚙️ **How it works:**

1. Executes `Start`.
2. Registers the timer.
3. Executes `End`.
4. After the timer expires, its callback becomes ready.
5. The callback executes when the Event Loop can process it.

🎯 **Interview Answer:**

The Callback Queue holds callbacks that are ready to execute. The Event Loop schedules them when the Call Stack is available.

<h2  class="answer-heading" id="11.5">11.5 What is the microtask queue?</h2>


📌 **Definition:**

The Microtask Queue stores high-priority Promise callbacks and other microtasks that need to execute after the current JavaScript operation completes.

Examples:

- `Promise.then()`
- `Promise.catch()`
- `Promise.finally()`
- `queueMicrotask()`

💻 **Example:**

```js
console.log("Start");

setTimeout(() => {
    console.log("Timer");
}, 0);

Promise.resolve().then(() => {
    console.log("Promise");
});

console.log("End");
```

**Output:**

```js
Start
End
Promise
Timer
```

⚙️ **How it works:**

1. Executes `Start`.
2. Registers the timer callback.
3. Schedules the Promise callback as a microtask.
4. Executes `End`.
5. Processes the Promise microtask.
6. Processes the timer callback when its phase is reached.

🎯 **Interview Answer:**

The Microtask Queue stores Promise callbacks and other microtasks. Node.js processes microtasks after the current JavaScript execution completes, before continuing with normal Event Loop work.

<h2  class="answer-heading" id="11.6">11.6 What is the timers phase?</h2>


📌 **Definition:**

The Timers Phase is an Event Loop phase where callbacks registered using `setTimeout()` and `setInterval()` become eligible to execute.

💻 **Example:**

```js
console.log("Start");

setTimeout(() => {
    console.log("Timeout callback");
}, 1000);

console.log("End");
```

**Output:**

```js
Start
End
Timeout callback
```

⚙️ **Important:**

- `setTimeout()` executes after its minimum delay has elapsed, not at an exact guaranteed time.
- `setInterval()` schedules repeated timer callbacks.
- Actual execution depends on Event Loop scheduling.

🎯 **Interview Answer:**

The Timers Phase handles callbacks for expired `setTimeout()` and `setInterval()` timers.

<h2  class="answer-heading" id="11.7">11.7 What is the poll phase?</h2>


📌 **Definition:**

The Poll Phase handles I/O-related callbacks and waits for new I/O events when appropriate.

Examples include:

- File system I/O callbacks.
- Network I/O callbacks.
- Incoming connection and data events.

💻 **Example:**

```js
const fs = require("fs");

console.log("Start");

fs.readFile("example.txt", "utf8", (error, data) => {
    if (error) {
        console.log(error.message);
        return;
    }

    console.log("File reading completed");
});

console.log("End");
```

**Possible output:**

```js
Start
End
File reading completed
```

⚙️ **How it works:**

1. Node.js starts the file-reading operation.
2. The main JavaScript code continues.
3. The file operation completes.
4. Its callback is handled through the I/O processing mechanism, commonly during the Poll Phase.

🎯 **Interview Answer:**

The Poll Phase processes I/O callbacks and can wait for new I/O events when there is no other work to execute.

<h2  class="answer-heading" id="11.8">11.8 What is the check phase?</h2>


📌 **Definition:**

The Check Phase executes callbacks registered using `setImmediate()`.

💻 **Example:**

```js
console.log("Start");

setImmediate(() => {
    console.log("Immediate callback");
});

console.log("End");
```

**Output:**

```js
Start
End
Immediate callback
```

⚙️ **How it works:**

- `setImmediate()` schedules a callback.
- The callback executes in the Check Phase.
- It runs after the Poll Phase in the Event Loop cycle.

🎯 **Interview Answer:**

The Check Phase is an Event Loop phase that executes callbacks registered using `setImmediate()`.

<h2  class="answer-heading" id="11.9">11.9 What is the close callbacks phase?</h2>


📌 **Definition:**

The Close Callbacks Phase executes callbacks when certain resources, such as sockets or handles, are closed.

💻 **Example:**

```js
const net = require("net");

const server = net.createServer();

server.on("close", () => {
    console.log("Server closed");
});

server.listen(3000, () => {
    console.log("Server started");

    server.close();
});
```

**Output:**

```js
Server started
Server closed
```

⚙️ **How it works:**

1. Creates a TCP server.
2. Starts listening.
3. Calls `server.close()`.
4. The close event callback executes when the server is closed.

🎯 **Interview Answer:**

The Close Callbacks Phase handles callbacks for certain closed resources, such as sockets and handles.

<h2  class="answer-heading" id="11.10">11.10 What is libuv?</h2>


📌 **Definition:**

libuv is a C library used by Node.js to provide asynchronous I/O, the Event Loop, timers, and thread pool functionality.

**Main responsibilities:**

- Event Loop implementation.
- Asynchronous file system operations.
- Thread pool management.
- Network I/O support.
- Timers.
- Operating-system-level asynchronous operations.

![Node.js или Go: что выбрать для своего проекта, и что выбирают крупные компании](https://images.openai.com/static-rsc-4/zx6VnQyBhqnHadPF89jBeEcJnV0hCtsIYzf-RNqdod-5GhXAuYVsKOEav6HGeaVxVshCluEe3h6crIRYR_SV0e0nG4ol5DFe9qwKURWyO8v4jLu8ZCKCEv8edWuBXVYe5HX2OKGCMHzTrqMNIC7hhttO1NdqcHl0Gj-8m-RvI3E?purpose=inline)


🎯 **Interview Answer:**

libuv is a C library used by Node.js to implement the Event Loop, asynchronous I/O operations, and thread pool functionality.

<h2  class="answer-heading" id="11.11">11.11 What is the libuv thread pool?</h2>


📌 **Definition:**

The libuv Thread Pool is a group of worker threads used to execute certain operations in the background without blocking the main JavaScript thread.

💻 **Example:**

```js
const crypto = require("crypto");

console.log("Start");

crypto.pbkdf2(
    "password",
    "salt",
    100000,
    64,
    "sha512",
    (error, key) => {
        if (error) {
            console.log(error);
            return;
        }

        console.log("Password hashing completed");
    }
);

console.log("End");
```

**Possible output:**

```js
Start
End
Password hashing completed
```

⚙️ **How it works:**

1. JavaScript calls `crypto.pbkdf2()`.
2. Node.js submits the expensive hashing operation to libuv's thread pool.
3. The main JavaScript thread continues executing.
4. A worker thread performs the hashing.
5. When completed, the callback is scheduled for execution.

🎯 **Interview Answer:**

The libuv Thread Pool contains worker threads that handle certain expensive or blocking operations, such as file system tasks and password hashing, without blocking the main JavaScript thread.

<h2  class="answer-heading" id="11.12">11.12 What is the default thread pool size?</h2>


📌 **Definition:**

The default libuv Thread Pool size in Node.js is **4 worker threads**.

You can change it using the `UV_THREADPOOL_SIZE` environment variable.

💻 **Example:**

```js
UV_THREADPOOL_SIZE=8 node app.js
```

**Check the configured value:**

```js
console.log(process.env.UV_THREADPOOL_SIZE || 4);
```

**Output (if not configured):**

```js
4
```

⚙️ **Important points:**

- Default size: 4.
- Can be configured using `UV_THREADPOOL_SIZE`.
- The setting should be applied before the thread pool is initialized.
- Increasing the size does not automatically improve performance; it depends on workload and system resources.

🎯 **Interview Answer:**

The default libuv Thread Pool size is 4 threads. We can configure it using the `UV_THREADPOOL_SIZE` environment variable.

<h2  class="answer-heading" id="11.13">11.13 What is `process.nextTick()`?</h2>


📌 **Definition:**

`process.nextTick()` schedules a callback to execute after the current JavaScript operation completes, before the Event Loop continues to its next phase.

💻 **Example:**

```js
console.log("Start");

process.nextTick(() => {
    console.log("Next Tick");
});

console.log("End");
```

**Output:**

```js
Start
End
Next Tick
```

⚙️ **How it works:**

1. Executes `Start`.
2. Registers the next-tick callback.
3. Executes `End`.
4. Processes the next-tick callback before moving to the next Event Loop phase.

🎯 **Interview Answer:**

`process.nextTick()` schedules a callback to run immediately after the current JavaScript operation completes, before the Event Loop continues.

<h2  class="answer-heading" id="11.14">11.14 What is the difference between `process.nextTick()` and Promise callbacks?</h2>


📌 **Definition:**

Both schedule callbacks to run after the current JavaScript execution, but Node.js processes them using different queues.

| `process.nextTick()`                        | Promise callbacks                                               |
| ------------------------------------------- | --------------------------------------------------------------- |
| Uses the next-tick queue                    | Uses the microtask queue                                        |
| Usually processed before Promise microtasks | Processed after next-tick callbacks in normal Node.js execution |
| Node.js-specific API                        | Standard JavaScript Promise API                                 |

💻 **Example:**

```js
console.log("Start");

process.nextTick(() => {
    console.log("Next Tick");
});

Promise.resolve().then(() => {
    console.log("Promise");
});

console.log("End");
```

**Output:**

```js
Start
End
Next Tick
Promise
```

⚙️ **How it works:**

1. Executes `Start`.
2. Schedules the next-tick callback.
3. Schedules the Promise callback.
4. Executes `End`.
5. Processes the next-tick queue.
6. Processes the Promise microtask queue.

🎯 **Interview Answer:**

`process.nextTick()` uses Node.js's next-tick queue, while Promise callbacks use the microtask queue. In normal Node.js execution, next-tick callbacks are processed before Promise microtasks.

<h2  class="answer-heading" id="11.15">11.15 Which operations use the thread pool?</h2>


📌 **Definition:**

Some Node.js operations use the libuv Thread Pool to perform work in the background.

**Important examples:**

| Operation                     | Uses Thread Pool? |
| ----------------------------- | ----------------- |
| `fs.readFile()`               | Yes               |
| `fs.writeFile()`              | Yes               |
| `crypto.pbkdf2()`             | Yes               |
| `crypto.scrypt()`             | Yes               |
| `dns.lookup()`                | Yes               |
| `zlib` compression operations | Yes               |
| `setTimeout()`                | No                |
| `setImmediate()`              | No                |
| `process.nextTick()`          | No                |
| Typical TCP socket I/O        | Usually no        |

💻 **Example:**

```js
const fs = require("fs");
const crypto = require("crypto");
const dns = require("dns");

fs.readFile("example.txt", () => {
    console.log("File completed");
});

crypto.pbkdf2("password", "salt", 100000, 64, "sha512", () => {
    console.log("Crypto completed");
});

dns.lookup("example.com", () => {
    console.log("DNS lookup completed");
});
```

🎯 **Interview Answer:**

Common operations that use the libuv Thread Pool include asynchronous file system operations, certain crypto operations, `dns.lookup()`, and zlib operations.

<h2  class="answer-heading" id="11.16">11.16 Does every asynchronous operation use the thread pool?</h2>


Important interview question

📌 **Definition:**

No. Not every asynchronous operation uses the libuv Thread Pool.

Node.js uses different mechanisms depending on the operation.

**Examples:**

| Operation              | How it is handled                              |
| ---------------------- | ---------------------------------------------- |
| File system operations | libuv Thread Pool                              |
| `crypto.pbkdf2()`      | libuv Thread Pool                              |
| `setTimeout()`         | Event Loop timer mechanism                     |
| `setImmediate()`       | Event Loop Check Phase                         |
| Promise callbacks      | Microtask Queue                                |
| `process.nextTick()`   | Next-tick queue                                |
| TCP network I/O        | Operating-system event notification mechanisms |

🎯 **Interview Answer:**

No. Node.js uses the Thread Pool for certain operations, while timers, Promise callbacks, and network I/O use other Event Loop and operating-system mechanisms.

<h2  class="answer-heading" id="11.17">11.17 How can CPU-intensive operations block the event loop?</h2>


📌 **Definition:**

CPU-intensive operations require significant processing time. If they run synchronously on the main JavaScript thread, they block the Event Loop.

💻 **Example:**

```js
console.log("Start");

function calculate() {
    let total = 0;

    for (let i = 0; i < 10000000000; i++) {
        total += i;
    }

    return total;
}

console.log(calculate());

console.log("End");
```

**Problem:**

- The `calculate()` function takes a long time.
- The main JavaScript thread cannot execute other JavaScript callbacks during this calculation.
- Other incoming requests may experience delays.

**Event Loop blocked**

Blocking operation

**Heavy CPU calculation**

Main JavaScript thread is busy

Other callbacks must wait

🎯 **Interview Answer:**

CPU-intensive synchronous operations block the main JavaScript thread, preventing the Event Loop from processing other callbacks and incoming requests efficiently.

<h2  class="answer-heading" id="11.18">11.18 How do you prevent event loop blocking?</h2>


📌 **Definition:**

We prevent Event Loop blocking by moving CPU-intensive work away from the main JavaScript thread and avoiding long-running synchronous operations.

**Important methods:**

**1. Use Worker Threads**

Worker Threads execute JavaScript in separate threads.

```js
const { Worker } = require("worker_threads");

const worker = new Worker("./worker.js");

worker.on("message", (result) => {
    console.log("Result:", result);
});

worker.on("error", (error) => {
    console.log(error);
});
```

**2. Use Child Processes**

Child processes run separate processes and are useful for isolating heavy work or running other programs.

```js
const { fork } = require("child_process");

const child = fork("./worker.js");

child.on("message", (result) => {
    console.log(result);
});
```

**3. Use Asynchronous APIs**

Avoid synchronous file operations in request-handling code.

```js
// Avoid blocking operation
fs.readFileSync("example.txt", "utf8");

// Prefer asynchronous operation
fs.readFile("example.txt", "utf8", (error, data) => {
    if (error) {
        console.log(error);
        return;
    }

    console.log(data);
});
```

**4. Break large tasks into smaller chunks**

Process a large dataset in smaller batches so other callbacks get opportunities to execute between batches.

**5. Use Background Job Queues**

For example, use BullMQ with Redis to process heavy tasks outside the HTTP request-response flow.

🎯 **Interview Answer:**

We can prevent Event Loop blocking by using Worker Threads, Child Processes, asynchronous APIs, background job queues, and breaking large CPU-intensive tasks into smaller chunks.

<h2  class="answer-heading" id="11.19">11.19 Quick Revision – Important Concepts</h2>


| Concept              | Simple meaning                            |
| -------------------- | ----------------------------------------- |
| Event Loop           | Manages asynchronous execution            |
| Call Stack           | Executes JavaScript functions             |
| Callback Queue       | Holds ready callbacks                     |
| Microtask Queue      | Holds Promise callbacks and microtasks    |
| Timers Phase         | Handles timer callbacks                   |
| Poll Phase           | Processes I/O callbacks                   |
| Check Phase          | Executes `setImmediate()` callbacks       |
| Close Callbacks      | Handles certain close events              |
| libuv                | Provides Event Loop and async I/O support |
| Thread Pool          | Worker threads for certain operations     |
| `process.nextTick()` | Schedules a next-tick callback            |
| Worker Threads       | Run JavaScript on separate threads        |

<h2  class="answer-heading" id="11.20">11.20 Important Event Loop Phase Order</h2>


## **Node.js Event Loop**

1. **Timers Phase**

   `setTimeout()` and `setInterval()`
2. **Pending Callbacks Phase**

   Certain deferred system I/O callbacks
3. **Idle / Prepare**

   Internal libuv operations
4. **Poll Phase**

   I/O callbacks and waiting for I/O
5. **Check Phase**

   `setImmediate()`
6. **Close Callbacks Phase**

   Certain resource close callbacks

Simplified phase order. Node.js also processes next-tick callbacks and microtasks between JavaScript callback executions.




<h2  class="answer-heading" id="15.1">15.1 How should we structure a Node.js project?</h2>

## **15.1 How should we structure a Node.js project?**

📌 **Definition:**

A Node.js project structure is an organized arrangement of files and folders that separates different responsibilities, such as routes, controllers, services, models, middleware, and configurations.

💻 **Recommended project structure:**

```js
node-project/
│
├── src/
│   ├── config/
│   │   ├── database.js
│   │   └── env.js
│   │
│   ├── routes/
│   │   └── user.routes.js
│   │
│   ├── controllers/
│   │   └── user.controller.js
│   │
│   ├── services/
│   │   └── user.service.js
│   │
│   ├── repositories/
│   │   └── user.repository.js
│   │
│   ├── models/
│   │   └── user.model.js
│   │
│   ├── middleware/
│   │   ├── auth.middleware.js
│   │   └── error.middleware.js
│   │
│   ├── utils/
│   │   └── response.js
│   │
│   ├── validators/
│   │   └── user.validator.js
│   │
│   ├── app.js
│   └── server.js
│
├── .env
├── .env.example
├── .gitignore
├── package.json
└── README.md
```

**Folder responsibilities:**

| Folder          | Responsibility                             |
| --------------- | ------------------------------------------ |
| `config/`       | Database and application configuration     |
| `routes/`       | API endpoint definitions                   |
| `controllers/`  | Handle HTTP requests and responses         |
| `services/`     | Business logic                             |
| `repositories/` | Database query operations                  |
| `models/`       | Database schemas and models                |
| `middleware/`   | Authentication, validation, error handling |
| `utils/`        | Reusable helper functions                  |
| `validators/`   | Request data validation                    |

**🎯 Interview Answer:**

I structure Node.js projects using separate folders for routes, controllers, services, models, middleware, configuration, and utilities. This improves code readability, maintainability, reusability, and scalability.

<h2  class="answer-heading" id="15.2">15.2 What is MVC architecture?</h2>

## **15.2 What is MVC architecture?**

📌 **Definition:**

MVC stands for **Model-View-Controller**. It is a software architectural pattern that separates an application into three main components.


**Example: User Management Application**

- Model: Stores user information.
- View: Displays user information.
- Controller: Handles user requests and coordinates the response.

🎯 **Interview Answer:**

MVC is an architectural pattern that separates an application into Model, View, and Controller to organize data, user interface, and request-handling responsibilities.

<h2  class="answer-heading" id="15.3">15.3 What is the Model layer?</h2>

## **15.3 What is the Model layer?**

📌 **Definition:**

The Model layer manages application data and defines how data is stored and represented in the database.

**Responsibilities:**

- Define database schemas.
- Define data fields and relationships.
- Apply model-level validation.
- Interact with the database through the ORM or ODM.

💻 **Example –&#x20;**`user.model.js`**:**

```js
const mongoose = require("mongoose");

const userSchema = new mongoose.Schema({
    name: {
        type: String,
        required: true
    },

    email: {
        type: String,
        required: true,
        unique: true
    },

    age: {
        type: Number
    }
});

module.exports = mongoose.model("User", userSchema);
```

🎯 **Interview Answer:**

The Model layer defines the application's data structure and database schema. In MongoDB applications, we commonly use Mongoose models.

<h2  class="answer-heading" id="15.4">15.4 What is the View layer?</h2>

## **15.4 What is the View layer?**

📌 **Definition:**

The View layer is responsible for displaying data to users through the user interface.

**Examples:**

- HTML pages.
- EJS templates.
- React components.
- Other frontend interfaces.

💻 **Example – React View:**

```js
function UserProfile({ user }) {
    return (
        <div>
            <h2>{user.name}</h2>
            <p>{user.email}</p>
        </div>
    );
}

export default UserProfile;
```

**In a MERN application:**

- React handles the View layer.
- Node.js and Express.js handle the backend API.
- MongoDB stores application data.

🎯 **Interview Answer:**

The View layer displays application data to users. In a MERN application, React commonly handles the View layer.

<h2  class="answer-heading" id="15.5">15.5 What is the Controller layer?</h2>

## **15.5 What is the Controller layer?**

📌 **Definition:**

The Controller layer receives HTTP requests, validates or coordinates request handling, calls the appropriate service, and sends HTTP responses.

**Responsibilities:**

- Receive requests.
- Read request parameters and body.
- Call service functions.
- Return HTTP status codes and responses.
- Forward errors to error-handling middleware.

💻 **Example –&#x20;**`user.controller.js`**:**

```js
const userService = require("../services/user.service");

const createUser = async (req, res, next) => {
    try {
        const user = await userService.createUser(req.body);

        res.status(201).json({
            success: true,
            data: user
        });
    } catch (error) {
        next(error);
    }
};

module.exports = {
    createUser
};
```

🎯 **Interview Answer:**

The Controller handles incoming HTTP requests, calls the appropriate service, and sends the response to the client.

<h2  class="answer-heading" id="15.6">15.6 What is the Service layer?</h2>

## **15.6 What is the Service layer?**

📌 **Definition:**

The Service layer contains the application's business logic and rules.

**Responsibilities:**

- Implement business rules.
- Perform calculations.
- Check business conditions.
- Coordinate multiple repositories.
- Call external services when needed.

💻 **Example –&#x20;**`user.service.js`**:**

```js
const userRepository = require("../repositories/user.repository");

const createUser = async (userData) => {
    const existingUser = await userRepository.findByEmail(
        userData.email
    );

    if (existingUser) {
        throw new Error("Email already exists");
    }

    return await userRepository.create(userData);
};

module.exports = {
    createUser
};
```

🎯 **Interview Answer:**

The Service layer contains business logic. It handles application rules and coordinates database operations through repositories or models.

<h2  class="answer-heading" id="15.7">15.7 What is the Repository pattern?</h2>

## **15.7 What is the Repository pattern?**

📌 **Definition:**

The Repository pattern separates database access logic from business logic.

It provides a common interface for performing database operations.

💻 **Example –&#x20;**`user.repository.js`**:**

```js
const User = require("../models/user.model");

const create = async (userData) => {
    return await User.create(userData);
};

const findByEmail = async (email) => {
    return await User.findOne({ email });
};

const findAll = async () => {
    return await User.find();
};

module.exports = {
    create,
    findByEmail,
    findAll
};
```

**Responsibilities:**

- Create database records.
- Find database records.
- Update database records.
- Delete database records.
- Keep database queries separate from business rules.

🎯 **Interview Answer:**

The Repository pattern separates database operations from business logic. It makes database access reusable, organized, and easier to maintain or replace.

<h2  class="answer-heading" id="15.8">15.8 What is the difference between controller and service?</h2>

## **15.8 What is the difference between Controller and Service?**

📌 **Definition:**

The Controller handles HTTP requests and responses, while the Service handles business logic.

| Controller                           | Service                                    |
| ------------------------------------ | ------------------------------------------ |
| Handles HTTP requests                | Handles business rules                     |
| Reads `req.body`, `req.params`       | Processes application data                 |
| Calls service methods                | Calls repositories or other services       |
| Sends HTTP responses                 | Returns results                            |
| Knows about Express request/response | Should generally be independent of Express |

💻 **Example:**

**Controller:**

```js
const userService = require("../services/user.service");

const getUser = async (req, res, next) => {
    try {
        const user = await userService.getUserById(req.params.id);

        res.status(200).json(user);
    } catch (error) {
        next(error);
    }
};

module.exports = { getUser };
```

**Service:**

```js
const userRepository = require("../repositories/user.repository");

const getUserById = async (id) => {
    const user = await userRepository.findById(id);

    if (!user) {
        throw new Error("User not found");
    }

    return user;
};

module.exports = { getUserById };
```

🎯 **Interview Answer:**

The Controller manages HTTP request and response handling, whereas the Service contains business logic. Keeping them separate makes the application easier to maintain and test.

<h2  class="answer-heading" id="15.9">15.9 What is the difference between service and repository?</h2>

## **15.9 What is the difference between Service and Repository?**

📌 **Definition:**

The Service handles business rules, whereas the Repository handles database operations.

| Service                         | Repository                      |
| ------------------------------- | ------------------------------- |
| Contains business logic         | Contains database queries       |
| Checks business conditions      | Fetches and stores data         |
| Coordinates multiple operations | Communicates with the database  |
| Calls repositories              | Uses models or database clients |

💻 **Example:**

```js
// Service: user.service.js

const userRepository = require("../repositories/user.repository");

const registerUser = async (userData) => {
    const existingUser = await userRepository.findByEmail(
        userData.email
    );

    if (existingUser) {
        throw new Error("Email already registered");
    }

    return userRepository.create(userData);
};
```

```js
// Repository: user.repository.js

const User = require("../models/user.model");

const findByEmail = (email) => {
    return User.findOne({ email });
};

const create = (userData) => {
    return User.create(userData);
};

module.exports = { findByEmail, create };
```

🎯 **Interview Answer:**

The Service layer contains business logic, while the Repository layer handles database queries. The Service uses the Repository to access data.

<h2  class="answer-heading" id="15.10">15.10 Why should we separate business logic from controllers?</h2>

## **15.10 Why should we separate business logic from controllers?**

📌 **Definition:**

We separate business logic from controllers to keep controllers small and make business logic reusable, testable, and maintainable.

**Without separation:**

```js
// Controller contains everything

const registerUser = async (req, res) => {
    const existingUser = await User.findOne({
        email: req.body.email
    });

    if (existingUser) {
        return res.status(409).json({
            message: "Email already exists"
        });
    }

    const user = await User.create(req.body);

    res.status(201).json(user);
};
```

**With separation:**

```js
// Controller

const registerUser = async (req, res, next) => {
    try {
        const user = await userService.registerUser(req.body);

        res.status(201).json(user);
    } catch (error) {
        next(error);
    }
};
```

```js
// Service

const registerUser = async (userData) => {
    const existingUser = await userRepository.findByEmail(
        userData.email
    );

    if (existingUser) {
        throw new Error("Email already exists");
    }

    return userRepository.create(userData);
};
```

**Benefits:**

1. Code becomes easier to understand.
2. Business logic can be reused.
3. Unit testing becomes easier.
4. Controllers remain small.
5. Maintenance becomes simpler.

🎯 **Interview Answer:**

We separate business logic from controllers to follow the Single Responsibility Principle. It improves code reusability, testability, readability, and maintainability.

<h2  class="answer-heading" id="15.11">15.11 What is dependency injection?</h2>

## **15.11 What is Dependency Injection?**

📌 **Definition:**

Dependency Injection (DI) is a design technique in which an object or function receives the dependencies it needs from outside instead of creating them internally.

**Simple example without Dependency Injection:**

```js
class UserService {
    constructor() {
        this.repository = new UserRepository();
    }
}
```

Here, `UserService` creates its own repository dependency.

**Example with Dependency Injection:**

```js
class UserService {
    constructor(userRepository) {
        this.userRepository = userRepository;
    }

    async getUsers() {
        return this.userRepository.findAll();
    }
}

const userRepository = new UserRepository();

const userService = new UserService(userRepository);
```

⚙️ **How it works:**

1. Create the repository.
2. Pass the repository to the service.
3. The service uses the injected repository.
4. You can inject a different implementation during testing.

**Real-world benefit:**

You can inject a mock repository during unit testing instead of connecting to the actual database.

🎯 **Interview Answer:**

Dependency Injection means providing required dependencies from outside a class or function. It reduces tight coupling and makes code easier to test and maintain.

<h2  class="answer-heading" id="15.12">15.12 What is a reusable utility function?</h2>

## **15.12 What is a reusable utility function?**

📌 **Definition:**

A utility function is a reusable function that performs a common task and can be used in multiple parts of an application.

**Examples:**

- Date formatting.
- Password hashing.
- Email validation.
- Generating random strings.
- Formatting API responses.

💻 **Example –&#x20;**`utils/format-date.js`**:**

```js
const formatDate = (date) => {
    return new Date(date).toISOString().split("T")[0];
};

module.exports = formatDate;
```

**Using the utility:**

```js
const formatDate = require("../utils/format-date");

const result = formatDate("2026-11-23");

console.log(result);
```

**Output:**

```js
2026-11-23
```

🎯 **Interview Answer:**

A utility function is a reusable helper function that performs a common task. We keep these functions in a separate utils folder to avoid code duplication.

<h2  class="answer-heading" id="15.13">15.13 What is configuration management?</h2>

## **15.13 What is configuration management?**

📌 **Definition:**

Configuration management means organizing and managing application settings in a centralized and maintainable way.

**Examples of configuration:**

- Database connection settings.
- Server port.
- API keys.
- JWT secret.
- Email server settings.
- Application environment.

💻 **Example –&#x20;**`config/env.js`**:**

```js
require("dotenv").config();

module.exports = {
    port: process.env.PORT || 5000,

    databaseUrl: process.env.DATABASE_URL,

    jwtSecret: process.env.JWT_SECRET,

    nodeEnv: process.env.NODE_ENV || "development"
};
```

**Using configuration:**

```js
const config = require("./config/env");

console.log(config.port);
console.log(config.nodeEnv);
```

🎯 **Interview Answer:**

Configuration management means keeping application settings in an organized and centralized location instead of hardcoding them throughout the project.

<h2  class="answer-heading" id="15.14">15.14 How do you manage environment variables?</h2>

## **15.14 How do you manage environment variables?**

📌 **Definition:**

Environment variables are external configuration values used to manage environment-specific settings and sensitive information.

In Node.js, we access them using `process.env`.

**Step 1: Install dotenv**

```js
npm install dotenv
```

**Step 2: Create&#x20;**`.env`**&#x20;file**

```js
PORT=5000
NODE_ENV=development
DATABASE_URL=mongodb://localhost:27017/myapp
JWT_SECRET=my_secret_key
```

**Step 3: Load environment variables**

```js
require("dotenv").config();

console.log(process.env.PORT);
console.log(process.env.NODE_ENV);
```

**Output:**

```js
5000
development
```

**Important points:**

- Never commit the real `.env` file to Git.
- Add `.env` to `.gitignore`.
- Create `.env.example` with placeholder values.
- Validate required environment variables when the application starts.
- Use a secure secret manager or deployment environment configuration for production secrets.

🎯 **Interview Answer:**

I manage environment variables using `process.env` and the dotenv package in development. I keep sensitive values outside the source code and configure them separately for each environment.

<h2  class="answer-heading" id="15.15">15.15 What is the purpose of a centralized database connection?</h2>

## **15.15 What is the purpose of a centralized database connection?**

📌 **Definition:**

A centralized database connection means managing the database connection logic in one dedicated file instead of connecting to the database separately in every controller or service.

**Example –&#x20;**`config/database.js`**:**

```js
const mongoose = require("mongoose");

const connectDB = async () => {
    try {
        await mongoose.connect(process.env.DATABASE_URL);

        console.log("MongoDB connected successfully");
    } catch (error) {
        console.error("Database connection failed:", error.message);

        process.exit(1);
    }
};

module.exports = connectDB;
```

**Using it in&#x20;**`server.js`**:**

```js
require("dotenv").config();

const app = require("./app");
const connectDB = require("./config/database");

const PORT = process.env.PORT || 5000;

const startServer = async () => {
    await connectDB();

    app.listen(PORT, () => {
        console.log(`Server running on port ${PORT}`);
    });
};

startServer();
```

**Benefits:**

1. Avoids duplicate connection code.
2. Makes database configuration easier.
3. Keeps database initialization centralized.
4. Makes error handling easier.
5. Ensures the database is connected before accepting requests.

🎯 **Interview Answer:**

A centralized database connection manages database initialization in one place. It avoids duplicate code and makes connection handling, configuration, and error management easier.

<h2  class="answer-heading" id="15.16">15.16 How do you handle multiple environments (development, staging, production)?</h2>

## **15.16 How do you handle multiple environments (development, staging, production)?**

📌 **Definition:**

Different environments are separate configurations used during development, testing, and deployment.

**Common environments:**

| Environment | Purpose                                |
| ----------- | -------------------------------------- |
| Development | Local development                      |
| Testing     | Automated testing                      |
| Staging     | Production-like testing before release |
| Production  | Application used by real customers     |

💻 **Example configuration:**

**Development&#x20;**`.env`**:**

```js
NODE_ENV=development
PORT=5000
DATABASE_URL=mongodb://localhost:27017/dev_db
```

**Staging environment variables:**

```js
NODE_ENV=staging
PORT=5000
DATABASE_URL=mongodb://staging-server/staging_db
```

**Production environment variables:**

```js
NODE_ENV=production
PORT=5000
DATABASE_URL=mongodb+srv://production-server/prod_db
```

**Access the environment:**

```js
console.log(process.env.NODE_ENV);

if (process.env.NODE_ENV === "production") {
    console.log("Production environment");
} else {
    console.log("Non-production environment");
}
```

**Important points:**

- Use separate databases for each environment.
- Never use production credentials in local development.
- Keep environment variables outside Git.
- Configure production secrets through the hosting platform or secret manager.
- Use the same application code with different configuration values.

🎯 **Interview Answer:**

I manage multiple environments using environment variables and separate configuration settings. Development, staging, and production use their own database URLs, credentials, and application settings.

<h2  class="answer-heading" id="15.17">15.17 How do you organize routes, controllers, services, models, and middleware?</h2>

## **15.17 How do you organize routes, controllers, services, models, and middleware?**

📌 **Definition:**

We organize these components into separate folders based on their responsibilities so that each layer handles a specific part of the application.


**Example route –&#x20;**`user.routes.js`**:**

```js
const express = require("express");
const userController = require("../controllers/user.controller");

const router = express.Router();

router.post("/users", userController.createUser);

router.get("/users/:id", userController.getUser);

module.exports = router;
```

**Example middleware –&#x20;**`auth.middleware.js`**:**

```js
const authMiddleware = (req, res, next) => {
    const token = req.headers.authorization;

    if (!token) {
        return res.status(401).json({
            message: "Unauthorized"
        });
    }

    next();
};

module.exports = authMiddleware;
```

**Responsibilities at a glance:**

| Component  | What it does                                |
| ---------- | ------------------------------------------- |
| Route      | Defines API endpoints                       |
| Middleware | Performs checks before controller execution |
| Controller | Handles HTTP request and response           |
| Service    | Applies business rules                      |
| Repository | Executes database queries                   |
| Model      | Defines data structure                      |

🎯 **Interview Answer:**

I organize Node.js applications by separating routes, middleware, controllers, services, repositories, and models. Each layer has a specific responsibility, which makes the application easier to test, maintain, and scale.

<h2  class="answer-heading" id="15.18">15.18 What is a monolithic architecture?</h2>

## **15.18 What is a Monolithic Architecture?**

📌 **Definition:**

Monolithic architecture is a software architecture where multiple application components are developed and deployed as one application.

**Example:**

An e-commerce application containing:

- User management.
- Product management.
- Order management.
- Payment management.
- Inventory management.

All these modules run as part of one deployable application.

**Monolithic Application**

**Users**

**Products**

**Orders**

**Payments**

**One application deployment**

**Advantages:**

- Easy to start developing.
- Simple deployment.
- Easier debugging in smaller applications.
- Modules can communicate directly within the application.

**Disadvantages:**

- Large applications can become difficult to maintain.
- A deployment usually involves the whole application.
- Scaling individual modules independently is difficult.
- Poorly separated code can become tightly coupled.

🎯 **Interview Answer:**

Monolithic architecture combines multiple application modules into one deployable application. It is simple to develop and deploy initially, but large applications can become difficult to maintain and scale independently.

<h2  class="answer-heading" id="15.19">15.19 What is a modular monolith?</h2>

## **15.19 What is a Modular Monolith?**

📌 **Definition:**

A Modular Monolith is a single deployable application divided into independent, well-organized modules.

Each module manages its own business logic and responsibilities, but all modules run within the same application.

**Example: E-commerce project**

```js
src/
│
├── modules/
│   ├── user/
│   │   ├── user.routes.js
│   │   ├── user.controller.js
│   │   ├── user.service.js
│   │   └── user.model.js
│   │
│   ├── product/
│   │   ├── product.routes.js
│   │   ├── product.controller.js
│   │   ├── product.service.js
│   │   └── product.model.js
│   │
│   ├── order/
│   │   ├── order.routes.js
│   │   ├── order.controller.js
│   │   ├── order.service.js
│   │   └── order.model.js
│   │
│   └── payment/
│       ├── payment.routes.js
│       ├── payment.controller.js
│       ├── payment.service.js
│       └── payment.model.js
│
├── config/
├── middleware/
├── shared/
├── app.js
└── server.js
```

**Advantages:**

1. Clear separation between modules.
2. Easier maintenance.
3. Better code organization.
4. Modules can be tested independently.
5. Can evolve into microservices if there is a real need.

**Monolith vs Modular Monolith:**

| Monolith                               | Modular Monolith                        |
| -------------------------------------- | --------------------------------------- |
| One application                        | One application                         |
| Components may be tightly coupled      | Modules have clear boundaries           |
| Organization may be less structured    | Organized by business modules           |
| Harder to maintain as complexity grows | Easier to maintain with good boundaries |
| One deployment                         | One deployment                          |

🎯 **Interview Answer:**

A Modular Monolith is a single deployable application organized into separate business modules. It provides better code separation and maintainability without the complexity of microservices.

<h2  class="answer-heading" id="15.20">15.20 What is clean architecture?</h2>

## **15.20 What is Clean Architecture?**

📌 **Definition:**

Clean Architecture is a software architecture approach that separates business rules from external technologies such as databases, frameworks, and APIs.

Its main principle is that **business logic should not depend directly on external infrastructure**.

**Common layers:**

1. Entities – Core business rules and domain objects.
2. Use Cases – Application-specific business operations.
3. Interface Adapters – Controllers, presenters, and repository implementations or adapters.
4. Frameworks and Drivers – Express, MongoDB, external APIs, and other infrastructure.

## **Clean Architecture**

**Frameworks & Drivers**

Express, MongoDB, external APIs

**Interface Adapters**

Controllers, repository adapters

**Use Cases**

Application business operations

**Entities**

Core business rules

Conceptual layers: dependencies should point inward toward business rules.

**Example:**

Suppose you are building a payment application.

- Entity: Payment rules.
- Use Case: Process a payment.
- Interface Adapter: Payment controller and repository adapter.
- Framework / Driver: Express, MongoDB, Razorpay API.

If you change MongoDB to PostgreSQL, the core payment business rules should not need to change.

🎯 **Interview Answer:**

Clean Architecture separates business logic from frameworks, databases, and external services. It uses dependency inversion so that core business rules remain independent of infrastructure.


### **Controller vs Service vs Repository vs Model**

| Layer      | Main responsibility       | Example               |
| ---------- | ------------------------- | --------------------- |
| Controller | HTTP request and response | `createUser()`        |
| Service    | Business logic            | Check duplicate email |
| Repository | Database operations       | `findByEmail()`       |
| Model      | Database schema           | `User` schema         |
| Middleware | Request processing        | Authentication        |
| Utility    | Reusable helper           | `formatDate()`        |

### **Monolith vs Modular Monolith vs Microservices**

| Architecture     | Deployment                                 |
| ---------------- | ------------------------------------------ |
| Monolith         | One application                            |
| Modular Monolith | One application with separate modules      |
| Microservices    | Multiple independently deployable services |

### **Important keywords for interviews**

| Keyword | Meaning                                |
| ------- | -------------------------------------- |
| MVC     | Model View Controller                  |
| DI      | Dependency Injection                   |
| SRP     | Single Responsibility Principle        |
| DRY     | Don't Repeat Yourself                  |
| ORM     | Object Relational Mapping              |
| ODM     | Object Document Mapping                |
| API     | Application Programming Interface      |
| SOLID   | Five object-oriented design principles |



<h2  class="answer-heading" id="18.21">18.21 What is request size limiting?</h2>

## **18.21 What is request size limiting?**

📌 **Definition:**

Request size limiting means restricting the maximum amount of data a client can send to a server.

It helps protect Node.js applications from excessively large requests and resource-exhaustion attacks.

**Why do we need it?**

- Prevent large payload attacks.
- Reduce memory consumption.
- Avoid unnecessary server processing.
- Protect API availability.

**Example: Express.js**

```js
const express = require("express");

const app = express();

app.use(express.json({
    limit: "1mb"
}));

app.use(express.urlencoded({
    extended: true,
    limit: "1mb"
}));

app.listen(5000, () => {
    console.log("Server running");
});
```

**How it works:**

- `express.json()` parses JSON request bodies.
- `limit: "1mb"` restricts the maximum parsed JSON body size.
- Requests exceeding the configured limit are rejected, normally with HTTP `413 Payload Too Large`.


**Important:**

For file uploads, configure separate limits in Multer. Also apply appropriate limits at your reverse proxy or API gateway, because Express body-parser limits do not cover every request type.

🎯 **Interview Answer:**

Request size limiting restricts the maximum request body size accepted by the server. In Express.js, I use body-parser limits such as `express.json({ limit: "1mb" })` to protect against oversized payloads and resource-exhaustion attacks.

<h2  class="answer-heading" id="18.22">18.22 How do you prevent brute-force login attempts?</h2>

## **18.22 How do you prevent brute-force login attempts?**

📌 **Definition:**

A brute-force attack occurs when an attacker repeatedly tries different passwords to gain unauthorized access to an account.

**Example:**

An attacker repeatedly tries:

```js
username: arun@gmail.com

password: 123456
password: password123
password: admin123
password: welcome123
password: ...
```

**How do we prevent it?**

1. Rate limiting – Restrict login attempts within a time period.
2. Account lockout – Temporarily lock an account after repeated failures, with safeguards against denial-of-service abuse.
3. CAPTCHA – Add a challenge after suspicious activity.
4. Strong passwords – Enforce appropriate password requirements.
5. Password hashing – Use bcrypt or Argon2.
6. MFA – Require an additional authentication factor.
7. Monitoring – Detect and log suspicious login activity.

**Example: Express Rate Limit**

Install:

```js
npm install express-rate-limit
```

**Step 1: Create rate-limit middleware**

`middleware/login-rate-limit.js`

```js
const rateLimit = require("express-rate-limit");

const loginLimiter = rateLimit({
    windowMs: 15 * 60 * 1000,

    max: 5,

    message: {
        success: false,
        message: "Too many login attempts. Try again later."
    },

    standardHeaders: true,
    legacyHeaders: false
});

module.exports = loginLimiter;
```

**Step 2: Apply it to login route**

```js
const express = require("express");

const loginLimiter = require("../middleware/login-rate-limit");
const authController = require("../controllers/auth.controller");

const router = express.Router();

router.post(
    "/login",
    loginLimiter,
    authController.login
);

module.exports = router;
```

**How it works:**

1. User sends a login request.
2. Rate limiter tracks login attempts.
3. The user is allowed up to 5 requests within 15 minutes under this configuration.
4. Further requests receive HTTP `429 Too Many Requests` until the window resets.

**Important production considerations:**

- Use a shared rate-limit store such as Redis when running multiple Node.js instances.
- Configure proxy trust correctly when behind Nginx or a load balancer.
- Consider limiting by both IP address and account identifier.
- Avoid revealing whether an email address exists.
- Use progressive delays and account protection without allowing attackers to lock out victims easily.

🎯 **Interview Answer:**

I prevent brute-force login attacks using rate limiting, account protection, CAPTCHA, strong password hashing, and multi-factor authentication. In Express.js, I commonly use `express-rate-limit` to restrict repeated login attempts.
