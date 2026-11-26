# **Complete Node.js Interview Preparation Checklist**

**Level: 3–5 years experience | Node.js Backend / MERN Full-Stack**

# **1. Node.js Fundamentals**

- 1.1 What is Node.js?
- 1.2 Why is Node.js used?
- 1.3 How does Node.js work internally?
- 1.4 Is Node.js single-threaded?
- 1.5 What is the V8 Engine?
- 1.6 What is libuv?
- 1.7 What is the Node.js Runtime?
- 1.8 Node.js vs Browser JavaScript?
- 1.9 Node.js vs PHP?
- 1.10 Node.js vs Java?
- 1.11 What are the advantages of Node.js?
- 1.12 What are the disadvantages of Node.js?
- 1.13 When should you use Node.js?
- 1.14 When should you avoid Node.js?
- 1.15 What is non-blocking I/O?
- 1.16 What is blocking I/O?
- 1.17 Blocking vs non-blocking?
- 1.18 What is synchronous execution?
- 1.19 What is asynchronous execution?
- 1.20 Synchronous vs asynchronous execution?
- 1.21 What is I/O?
- 1.22 What is I/O-intensive work?
- 1.23 What is CPU-intensive work?
- 1.24 Why is Node.js suitable for APIs?
- 1.25 What happens when a Node.js application starts?

# **2. JavaScript Core Concepts for Node.js**

- 2.1 What is JavaScript?
- 2.2 What are JavaScript data types?
- 2.3 Primitive vs non-primitive data types?
- 2.4 `var`, `let` and `const`?
- 2.5 What is scope?
- 2.6 Global, function and block scope?
- 2.7 What is lexical scope?
- 2.8 What is a closure?
- 2.9 What is hoisting?
- 2.10 What is the Temporal Dead Zone?
- 2.11 What is `this`?
- 2.12 Arrow function vs regular function?
- 2.13 What is a callback?
- 2.14 What is a higher-order function?
- 2.15 What is a pure function?
- 2.16 What is an impure function?
- 2.17 What is recursion?
- 2.18 What is destructuring?
- 2.19 What is spread syntax?
- 2.20 What is rest syntax?
- 2.21 What is optional chaining?
- 2.22 What is nullish coalescing?
- 2.23 `null` vs `undefined`?
- 2.24 `==` vs `===`?
- 2.25 What is type coercion?
- 2.26 What is `NaN`?
- 2.27 What is the `typeof` operator?
- 2.28 What is the `instanceof` operator?
- 2.29 What is `Object.freeze()`?
- 2.30 What is `Object.seal()`?
- 2.31 What is the difference between shallow copy and deep copy?
- 2.32 What is mutable vs immutable data?
- 2.33 What are `map()`, `filter()` and `reduce()`?
- 2.34 What are `some()` and `every()`?
- 2.35 What are `find()` and `findIndex()`?
- 2.36 What is `forEach()`?
- 2.37 `forEach()` vs `map()`?
- 2.38 What is `Promise`?
- 2.39 What are Promise states?
- 2.40 What is `Promise.all()`?
- 2.41 What is `Promise.allSettled()`?
- 2.42 What is `Promise.race()`?
- 2.43 What is `Promise.any()`?
- 2.44 What is `async` and `await`?
- 2.45 What is error handling in async functions?
- 2.46 What is the Event Loop in JavaScript?
- 2.47 What are microtasks and macrotasks?
- 2.48 What is `setTimeout()`?
- 2.49 What is `setInterval()`?
- 2.50 What is `setImmediate()`?
- 2.51 What is `process.nextTick()`?
- 2.52 `setImmediate()` vs `setTimeout()`?
- 2.53 `process.nextTick()` vs Promise?
- 2.54 What is memory management in JavaScript?
- 2.55 What is garbage collection?

# **3. Node.js Event Loop, Process & Threads**

- 3.1 What is the Event Loop?
- 3.2 How does the Event Loop work?
- 3.3 What are the Event Loop phases?
- 3.4 What is the Call Stack?
- 3.5 What is the Callback Queue?
- 3.6 What is the Microtask Queue?
- 3.7 What is the libuv thread pool?
- 3.8 What tasks are handled by the thread pool?
- 3.9 How can you change the thread pool size?
- 3.10 What is a process?
- 3.11 What is a thread?
- 3.12 Process vs thread?
- 3.13 What is the main thread?
- 3.14 What is concurrency?
- 3.15 What is parallelism?
- 3.16 Concurrency vs parallelism?
- 3.17 What is the Cluster module?
- 3.18 What are Worker Threads?
- 3.19 What are Child Processes?
- 3.20 Cluster vs Worker Threads?
- 3.21 Worker Threads vs Child Processes?
- 3.22 How do you handle CPU-intensive tasks?
- 3.23 How do you prevent Event Loop blocking?
- 3.24 What is Event Loop lag?
- 3.25 What happens when the Event Loop is blocked?

# **4. Node.js Modules & Module Systems**

- 4.1 What is a module?
- 4.2 Why do we use modules?
- 4.3 What is CommonJS?
- 4.4 What is ES Module?
- 4.5 CommonJS vs ES Modules?
- 4.6 What is `require()`?
- 4.7 What is `module.exports`?
- 4.8 What is `exports`?
- 4.9 `exports` vs `module.exports`?
- 4.10 What is `import`?
- 4.11 What is `export`?
- 4.12 Default export vs named export?
- 4.13 How do you create custom modules?
- 4.14 How do you reuse modules?
- 4.15 What is module caching?
- 4.16 What happens when you require the same module multiple times?
- 4.17 What is the `package.json` `type` field?
- 4.18 What is `__dirname`?
- 4.19 What is `__filename`?
- 4.20 How do ES Modules handle file paths?

# **5. Node.js Built-in Modules**

- 5.1 What is the `fs` module?
- 5.2 Synchronous vs asynchronous file operations?
- 5.3 What is `fs.promises`?
- 5.4 What is the `path` module?
- 5.5 What is the `os` module?
- 5.6 What is the `http` module?
- 5.7 What is the `https` module?
- 5.8 What is the `events` module?
- 5.9 What is `EventEmitter`?
- 5.10 What are `emit()`, `on()` and `once()`?
- 5.11 What is the `stream` module?
- 5.12 What is the `buffer` module?
- 5.13 What is the `crypto` module?
- 5.14 What is the `zlib` module?
- 5.15 What is the `url` module?
- 5.16 What is the `util` module?
- 5.17 What is the `child_process` module?
- 5.18 What is the `worker_threads` module?
- 5.19 What is the `cluster` module?
- 5.20 What is the `readline` module?
- 5.21 What is the `dns` module?
- 5.22 What is the `net` module?
- 5.23 What is the `tls` module?
- 5.24 What is the `timers` module?
- 5.25 What is the `process` object?

# **6. NPM, Package Management & Dependencies**

- 6.1 What is NPM?
- 6.2 What is a package?
- 6.3 What is a dependency?
- 6.4 What is a dev dependency?
- 6.5 Dependency vs dev dependency?
- 6.6 What is `package.json`?
- 6.7 What is `package-lock.json`?
- 6.8 Why do we use `package-lock.json`?
- 6.9 What is semantic versioning?
- 6.10 What are major, minor and patch versions?
- 6.11 What does `^` mean in package versions?
- 6.12 What does `~` mean in package versions?
- 6.13 What is `npm install`?
- 6.14 What is `npm ci`?
- 6.15 `npm install` vs `npm ci`?
- 6.16 What is `npm update`?
- 6.17 What is `npm audit`?
- 6.18 How do you fix dependency vulnerabilities?
- 6.19 What are npm scripts?
- 6.20 What is `npx`?
- 6.21 NPM vs NPX?
- 6.22 What is a global package?
- 6.23 What is a local package?
- 6.24 What is dependency management?
- 6.25 How do you manage package versions across environments?

# **7. Express.js Fundamentals**

- 7.1 What is Express.js?
- 7.2 Why do we use Express?
- 7.3 Node.js vs Express.js?
- 7.4 How does Express work?
- 7.5 How do you create an Express server?
- 7.6 What is routing?
- 7.7 What is route handling?
- 7.8 What are route parameters?
- 7.9 What are query parameters?
- 7.10 What are request body parameters?
- 7.11 Route parameters vs query parameters?
- 7.12 What is `req`?
- 7.13 What is `res`?
- 7.14 What is `next()`?
- 7.15 What is `app.use()`?
- 7.16 What is `app.get()`?
- 7.17 What is `app.post()`?
- 7.18 What is `app.put()`?
- 7.19 What is `app.patch()`?
- 7.20 What is `app.delete()`?
- 7.21 What is Express Router?
- 7.22 How do you separate routes?
- 7.23 How do you handle 404 errors?
- 7.24 How do you handle API errors?
- 7.25 How do you return JSON responses?
- 7.26 What is `express.json()`?
- 7.27 What is `express.urlencoded()`?
- 7.28 How do you serve static files?
- 7.29 How do you handle route-specific middleware?
- 7.30 What is Express request lifecycle?

# **8. Middleware**

- 8.1 What is middleware?
- 8.2 Why do we use middleware?
- 8.3 How does middleware work?
- 8.4 What is application-level middleware?
- 8.5 What is router-level middleware?
- 8.6 What is built-in middleware?
- 8.7 What is third-party middleware?
- 8.8 What is custom middleware?
- 8.9 What is error-handling middleware?
- 8.10 What is the middleware execution order?
- 8.11 What happens if middleware does not call `next()`?
- 8.12 What happens when middleware calls `next(error)`?
- 8.13 How do you write reusable middleware?
- 8.14 How do you protect routes using middleware?
- 8.15 How do you validate requests using middleware?
- 8.16 How do you handle authentication using middleware?
- 8.17 How do you implement authorization middleware?
- 8.18 How do you handle logging using middleware?
- 8.19 How do you handle rate limiting using middleware?
- 8.20 What happens if middleware sends a response and then calls `next()`?

# **9. REST API Development**

- 9.1 What is an API?
- 9.2 What is REST?
- 9.3 What is a REST API?
- 9.4 What are REST principles?
- 9.5 What is a RESTful API?
- 9.6 What is HTTP?
- 9.7 What is HTTPS?
- 9.8 HTTP vs HTTPS?
- 9.9 What are HTTP methods?
- 9.10 GET vs POST?
- 9.11 PUT vs PATCH?
- 9.12 DELETE vs POST?
- 9.13 What is an HTTP status code?
- 9.14 What is 200?
- 9.15 What is 201?
- 9.16 What is 204?
- 9.17 What is 400?
- 9.18 What is 401?
- 9.19 What is 403?
- 9.20 What is 404?
- 9.21 What is 409?
- 9.22 What is 422?
- 9.23 What is 429?
- 9.24 What is 500?
- 9.25 What is 502?
- 9.26 What is 503?
- 9.27 What is 504?
- 9.28 What are request headers?
- 9.29 What are response headers?
- 9.30 What is Content-Type?
- 9.31 What is Authorization?
- 9.32 What is Accept?
- 9.33 What is idempotency?
- 9.34 Which HTTP methods are idempotent?
- 9.35 What is API versioning?
- 9.36 How do you version REST APIs?
- 9.37 What is pagination?
- 9.38 What is offset pagination?
- 9.39 What is cursor pagination?
- 9.40 Offset vs cursor pagination?
- 9.41 What is filtering?
- 9.42 What is sorting?
- 9.43 What is API search?
- 9.44 How do you design consistent API responses?
- 9.45 How do you handle API errors?
- 9.46 What is API documentation?
- 9.47 What is OpenAPI/Swagger?
- 9.48 How do you implement API rate limiting?
- 9.49 How do you handle large API responses?
- 9.50 How do you design a scalable REST API?

# **10. API Architecture & Project Structure**

- 10.1 How do you structure a Node.js project?
- 10.2 What is MVC?
- 10.3 What is the Model layer?
- 10.4 What is the View layer?
- 10.5 What is the Controller layer?
- 10.6 What is the Service layer?
- 10.7 What is the Repository layer?
- 10.8 What is the Utils layer?
- 10.9 What is the Config layer?
- 10.10 Controller vs Service?
- 10.11 Service vs Repository?
- 10.12 What is layered architecture?
- 10.13 What is feature-based architecture?
- 10.14 Layered vs feature-based structure?
- 10.15 What is Dependency Injection?
- 10.16 What is the Repository Pattern?
- 10.17 What is separation of concerns?
- 10.18 What is single responsibility?
- 10.19 How do you reuse business logic?
- 10.20 How do you avoid duplicate code?
- 10.21 How do you handle shared utilities?
- 10.22 How do you manage application configuration?
- 10.23 How do you structure a large Node.js application?
- 10.24 How do you maintain a Node.js project as the team grows?
- 10.25 How do you refactor a tightly coupled application?

# **11. Authentication**

- 11.1 What is authentication?
- 11.2 What is authorization?
- 11.3 Authentication vs authorization?
- 11.4 What is login authentication?
- 11.5 What is password hashing?
- 11.6 Why should passwords not be stored as plain text?
- 11.7 What is bcrypt?
- 11.8 What is salt?
- 11.9 What is password comparison?
- 11.10 What is JWT?
- 11.11 What are JWT components?
- 11.12 What is JWT signing?
- 11.13 What is JWT verification?
- 11.14 What is JWT expiration?
- 11.15 What is an Access Token?
- 11.16 What is a Refresh Token?
- 11.17 Access Token vs Refresh Token?
- 11.18 How does JWT authentication work?
- 11.19 How do you implement JWT middleware?
- 11.20 How do you refresh expired tokens?
- 11.21 How do you invalidate JWT tokens?
- 11.22 How do you implement logout?
- 11.23 JWT vs session authentication?
- 11.24 What is cookie-based authentication?
- 11.25 What is HttpOnly?
- 11.26 What is Secure cookie?
- 11.27 What is SameSite?
- 11.28 How do you implement authentication using cookies?
- 11.29 How do you prevent stolen token misuse?
- 11.30 What is OAuth 2.0?
- 11.31 What is OpenID Connect?
- 11.32 How does Google login work?
- 11.33 What is MFA?
- 11.34 What is OTP authentication?
- 11.35 How do you implement forgot password?
- 11.36 How do you implement reset password?
- 11.37 How do you implement email verification?
- 11.38 What is account lockout?
- 11.39 How do you secure login APIs?
- 11.40 What happens if the Refresh Token is compromised?

# **12. Authorization & RBAC**

- 12.1 What is authorization?
- 12.2 What is Role-Based Access Control (RBAC)?
- 12.3 What is permission-based authorization?
- 12.4 Role vs permission?
- 12.5 How do you implement admin/user access?
- 12.6 How do you restrict APIs based on roles?
- 12.7 How do you implement reusable authorization middleware?
- 12.8 How do you manage multiple roles?
- 12.9 What is ownership-based authorization?
- 12.10 How do you prevent users from accessing other users' records?
- 12.11 What is ABAC?
- 12.12 RBAC vs ABAC?
- 12.13 How do you implement multi-tenant authorization?
- 12.14 How do you manage permissions in a large application?
- 12.15 How do you secure admin APIs?

# **13. Node.js Security & OWASP**

- 13.1 What is application security?
- 13.2 What is OWASP?
- 13.3 What is OWASP Top 10?
- 13.4 What is SQL Injection?
- 13.5 What is NoSQL Injection?
- 13.6 How do you prevent SQL Injection?
- 13.7 How do you prevent NoSQL Injection?
- 13.8 What is XSS?
- 13.9 How do you prevent XSS?
- 13.10 What is CSRF?
- 13.11 How do you prevent CSRF?
- 13.12 What is CORS?
- 13.13 Why do we use CORS?
- 13.14 What is a CORS preflight request?
- 13.15 What is Helmet?
- 13.16 Why do we use Helmet?
- 13.17 What is Content Security Policy (CSP)?
- 13.18 What is request validation?
- 13.19 What is input sanitization?
- 13.20 Validation vs sanitization?
- 13.21 How do you validate API request bodies?
- 13.22 What is rate limiting?
- 13.23 How do you prevent brute-force attacks?
- 13.24 How do you protect sensitive environment variables?
- 13.25 How do you validate uploaded files?
- 13.26 How do you restrict file upload size?
- 13.27 How do you prevent malicious file uploads?
- 13.28 What is request size limiting?
- 13.29 How do you prevent mass assignment vulnerabilities?
- 13.30 How do you protect APIs from abuse?
- 13.31 What is SSRF?
- 13.32 What is insecure direct object reference (IDOR)?
- 13.33 What is a security header?
- 13.34 How do you secure HTTP headers?
- 13.35 How do you manage dependency vulnerabilities?
- 13.36 How do you store secrets securely?
- 13.37 What is encryption?
- 13.38 Encryption vs hashing?
- 13.39 Symmetric vs asymmetric encryption?
- 13.40 How do you protect APIs in production?

# **14. Request Validation & Error Handling**

- 14.1 Why is validation important?
- 14.2 What is schema validation?
- 14.3 What is Joi?
- 14.4 What is Zod?
- 14.5 Joi vs Zod?
- 14.6 How do you validate request bodies?
- 14.7 How do you validate query parameters?
- 14.8 How do you validate route parameters?
- 14.9 How do you validate nested objects?
- 14.10 How do you validate arrays?
- 14.11 How do you handle optional fields?
- 14.12 How do you handle validation errors?
- 14.13 What is centralized error handling?
- 14.14 What is a custom error class?
- 14.15 What is operational error?
- 14.16 What is programmer error?
- 14.17 Operational vs programmer errors?
- 14.18 How do you handle async errors?
- 14.19 How do you handle unhandled Promise rejections?
- 14.20 How do you handle uncaught exceptions?
- 14.21 Why should you avoid continuing after an unrecoverable exception?
- 14.22 How do you log errors?
- 14.23 How do you return safe error responses?
- 14.24 How do you prevent stack traces from leaking?
- 14.25 How do you handle errors across services?

# **15. MongoDB Fundamentals**

- 15.1 What is MongoDB?
- 15.2 What is NoSQL?
- 15.3 SQL vs NoSQL?
- 15.4 What is a document?
- 15.5 What is a collection?
- 15.6 What is BSON?
- 15.7 What is ObjectId?
- 15.8 What is a MongoDB database?
- 15.9 What is CRUD?
- 15.10 What is `insertOne()`?
- 15.11 What is `insertMany()`?
- 15.12 What is `find()`?
- 15.13 What is `findOne()`?
- 15.14 What is `updateOne()`?
- 15.15 What is `updateMany()`?
- 15.16 What is `replaceOne()`?
- 15.17 What is `deleteOne()`?
- 15.18 What is `deleteMany()`?
- 15.19 What is `$set`?
- 15.20 What is `$unset`?
- 15.21 What is `$inc`?
- 15.22 What is `$push`?
- 15.23 What is `$pull`?
- 15.24 What is `$addToSet`?
- 15.25 What is `$in`?
- 15.26 What is `$nin`?
- 15.27 What is `$gte`?
- 15.28 What is `$lte`?
- 15.29 What is `$or`?
- 15.30 What is `$and`?

# **16. MongoDB Advanced & Mongoose**

- 16.1 What is Mongoose?
- 16.2 MongoDB vs Mongoose?
- 16.3 What is a Schema?
- 16.4 What is a Model?
- 16.5 What is a Document?
- 16.6 Schema vs Model?
- 16.7 What is Schema Validation?
- 16.8 What are Mongoose validators?
- 16.9 What is Middleware in Mongoose?
- 16.10 What are pre hooks?
- 16.11 What are post hooks?
- 16.12 What is `populate()`?
- 16.13 What is `lean()`?
- 16.14 What is Projection?
- 16.15 What is Indexing?
- 16.16 Why do we use indexes?
- 16.17 What is a Compound Index?
- 16.18 What is a Unique Index?
- 16.19 What is a TTL Index?
- 16.20 What is a Text Index?
- 16.21 What is an Aggregation Pipeline?
- 16.22 What is `$match`?
- 16.23 What is `$group`?
- 16.24 What is `$lookup`?
- 16.25 What is `$project`?
- 16.26 What is `$unwind`?
- 16.27 What is `$sort`?
- 16.28 What is `$facet`?
- 16.29 What is a MongoDB transaction?
- 16.30 What is a session in MongoDB?
- 16.31 How do you implement transactions using Mongoose?
- 16.32 What is atomicity?
- 16.33 What is a race condition?
- 16.34 How do you prevent inventory overselling?
- 16.35 How do you prevent duplicate records?
- 16.36 What is optimistic concurrency?
- 16.37 What is cursor pagination?
- 16.38 How do you optimize slow MongoDB queries?
- 16.39 What is `explain()`?
- 16.40 How do you identify unused indexes?

# **17. SQL & MySQL/PostgreSQL**

- 17.1 What is SQL?
- 17.2 What is a relational database?
- 17.3 SQL vs NoSQL?
- 17.4 What is a table?
- 17.5 What is a row?
- 17.6 What is a column?
- 17.7 What is a primary key?
- 17.8 What is a foreign key?
- 17.9 What is a unique key?
- 17.10 What is a composite key?
- 17.11 What is an index?
- 17.12 What are the types of indexes?
- 17.13 What is a JOIN?
- 17.14 What is INNER JOIN?
- 17.15 What is LEFT JOIN?
- 17.16 What is RIGHT JOIN?
- 17.17 What is FULL JOIN?
- 17.18 INNER JOIN vs LEFT JOIN?
- 17.19 What is GROUP BY?
- 17.20 What is HAVING?
- 17.21 WHERE vs HAVING?
- 17.22 What is ORDER BY?
- 17.23 What is LIMIT?
- 17.24 What is OFFSET?
- 17.25 What is a subquery?
- 17.26 What is a CTE?
- 17.27 What is a Window Function?
- 17.28 What is `ROW_NUMBER()`?
- 17.29 What is `RANK()`?
- 17.30 What is `DENSE_RANK()`?
- 17.31 What is Normalization?
- 17.32 What is Denormalization?
- 17.33 What are 1NF, 2NF and 3NF?
- 17.34 What is a transaction?
- 17.35 What are ACID properties?
- 17.36 What is isolation?
- 17.37 What is a deadlock?
- 17.38 How do you prevent SQL injection?
- 17.39 How do you optimize slow queries?
- 17.40 What is EXPLAIN?
- 17.41 What is connection pooling?
- 17.42 How do you manage database connections in Node.js?
- 17.43 MongoDB vs MySQL for a project?
- 17.44 How do you design relational tables?
- 17.45 What is database migration?

# **18. Redis & Caching**

- 18.1 What is Redis?
- 18.2 Why do we use Redis?
- 18.3 Redis vs MongoDB?
- 18.4 Redis vs in-memory caching?
- 18.5 What is caching?
- 18.6 What is cache TTL?
- 18.7 What is Cache-Aside?
- 18.8 What is Write-Through?
- 18.9 What is Write-Behind?
- 18.10 What is cache invalidation?
- 18.11 How do you cache API responses?
- 18.12 How do you invalidate cache after updating data?
- 18.13 What is cache stampede?
- 18.14 What is cache avalanche?
- 18.15 What is cache penetration?
- 18.16 How do you handle Redis failures?
- 18.17 How do you use Redis for session management?
- 18.18 How do you use Redis for rate limiting?
- 18.19 How do you use Redis for distributed locking?
- 18.20 What is Redis Pub/Sub?
- 18.21 What is Redis Streams?
- 18.22 Pub/Sub vs Streams?
- 18.23 How do you scale Redis?
- 18.24 What is Redis persistence?
- 18.25 What are RDB and AOF?

# **19. File Uploads & File Management**

- 19.1 How do you upload files using Node.js?
- 19.2 What is Multipart Form Data?
- 19.3 What is Multer?
- 19.4 How does Multer work?
- 19.5 What is memory storage?
- 19.6 What is disk storage?
- 19.7 Memory storage vs disk storage?
- 19.8 How do you upload multiple files?
- 19.9 How do you upload multiple files for different fields?
- 19.10 How do you validate file size?
- 19.11 How do you validate file type?
- 19.12 How do you validate MIME type and file content?
- 19.13 How do you prevent malicious file uploads?
- 19.14 How do you upload files to AWS S3?
- 19.15 Local storage vs cloud storage?
- 19.16 How do you upload large files?
- 19.17 What is a presigned URL?
- 19.18 How do you generate a presigned URL?
- 19.19 How do you delete files from S3?
- 19.20 How do you manage file access permissions?
- 19.21 How do you avoid storing files directly in the database?
- 19.22 How do you process uploaded images?
- 19.23 How do you handle failed file uploads?
- 19.24 How do you handle files when the database operation fails?
- 19.25 How do you scale file upload APIs?

# **20. Streams & Buffers**

- 20.1 What is a Stream?
- 20.2 Why do we use Streams?
- 20.3 What are the types of Streams?
- 20.4 What is a Readable Stream?
- 20.5 What is a Writable Stream?
- 20.6 What is a Duplex Stream?
- 20.7 What is a Transform Stream?
- 20.8 What is a Buffer?
- 20.9 Why do we use Buffers?
- 20.10 Buffer vs Stream?
- 20.11 Stream vs reading an entire file?
- 20.12 What is `pipe()`?
- 20.13 What is `pipeline()`?
- 20.14 What is backpressure?
- 20.15 How do Streams handle large files?
- 20.16 How do you process a large CSV file?
- 20.17 How do you upload large files using Streams?
- 20.18 How do you handle Stream errors?
- 20.19 What is stream buffering?
- 20.20 How do Streams reduce memory usage?

# **21. WebSockets & Socket.IO**

- 21.1 What is WebSocket?
- 21.2 What is Socket.IO?
- 21.3 WebSocket vs Socket.IO?
- 21.4 Why do we use WebSockets?
- 21.5 What is a WebSocket handshake?
- 21.6 What is a Socket.IO event?
- 21.7 What is `emit()`?
- 21.8 What is `on()`?
- 21.9 What is a Socket.IO room?
- 21.10 What is a namespace?
- 21.11 Room vs Namespace?
- 21.12 How do you implement a chat application?
- 21.13 How do you implement real-time notifications?
- 21.14 How do you track online users?
- 21.15 How do you handle disconnections?
- 21.16 How do you handle reconnections?
- 21.17 How do you authenticate Socket.IO connections?
- 21.18 How do you authorize Socket.IO events?
- 21.19 How do you scale Socket.IO?
- 21.20 What is the Redis Adapter?
- 21.21 How do you broadcast between multiple instances?
- 21.22 How do you handle WebSocket failures?
- 21.23 How do you prevent unauthorized socket access?
- 21.24 How do you handle duplicate socket events?
- 21.25 How do you manage large numbers of socket connections?

# **22. Background Jobs & Task Processing**

- 22.1 What is a background job?
- 22.2 Why do we use background jobs?
- 22.3 What is a job queue?
- 22.4 What is Bull?
- 22.5 What is BullMQ?
- 22.6 What is a producer?
- 22.7 What is a consumer?
- 22.8 What is a worker?
- 22.9 How do you process jobs asynchronously?
- 22.10 How do you send emails using background jobs?
- 22.11 How do you process large reports?
- 22.12 How do you process uploaded files?
- 22.13 What is retry logic?
- 22.14 What is exponential backoff?
- 22.15 What is a Dead Letter Queue?
- 22.16 How do you handle failed jobs?
- 22.17 How do you prevent duplicate jobs?
- 22.18 What is job idempotency?
- 22.19 How do you schedule jobs?
- 22.20 What is a cron job?
- 22.21 What is a recurring job?
- 22.22 How do you manage concurrent workers?
- 22.23 How do you scale background workers?
- 22.24 How do you monitor job queues?
- 22.25 How do you handle a worker crash?

# **23. Application Performance & Optimization**

- 23.1 What is performance optimization?
- 23.2 How do you identify a performance bottleneck?
- 23.3 How do you optimize a slow API?
- 23.4 How do you optimize CPU usage?
- 23.5 How do you optimize memory usage?
- 23.6 How do you optimize database queries?
- 23.7 How do you reduce API response time?
- 23.8 What is profiling?
- 23.9 What is CPU profiling?
- 23.10 What is memory profiling?
- 23.11 What is a memory leak?
- 23.12 How do you identify a memory leak?
- 23.13 What is garbage collection?
- 23.14 What is heap memory?
- 23.15 What is stack memory?
- 23.16 Heap vs stack?
- 23.17 What is Event Loop blocking?
- 23.18 How do you detect Event Loop blocking?
- 23.19 What is connection pooling?
- 23.20 Why is connection pooling important?
- 23.21 What is compression?
- 23.22 How do you optimize large JSON responses?
- 23.23 What is pagination optimization?
- 23.24 How do you optimize file processing?
- 23.25 How do you optimize Node.js for high traffic?

# **24. Application Scaling**

- 24.1 What is scaling?
- 24.2 What is vertical scaling?
- 24.3 What is horizontal scaling?
- 24.4 Vertical vs horizontal scaling?
- 24.5 What is a stateless application?
- 24.6 What is a stateful application?
- 24.7 Why should applications be stateless?
- 24.8 What is Cluster?
- 24.9 What are Worker Threads?
- 24.10 Cluster vs Worker Threads?
- 24.11 What is PM2?
- 24.12 PM2 Fork vs Cluster mode?
- 24.13 What is load balancing?
- 24.14 What are load balancing algorithms?
- 24.15 What is Round Robin?
- 24.16 What is Least Connections?
- 24.17 What is IP Hash?
- 24.18 What is Nginx?
- 24.19 What is a reverse proxy?
- 24.20 What is graceful shutdown?
- 24.21 What is zero-downtime deployment?
- 24.22 What is rolling deployment?
- 24.23 What is Blue-Green deployment?
- 24.24 What is Canary deployment?
- 24.25 How do you scale a Node.js API?

# **25. Microservices Architecture**

- 25.1 What are microservices?
- 25.2 What is monolithic architecture?
- 25.3 Monolith vs microservices?
- 25.4 What is modular monolith?
- 25.5 Modular monolith vs microservices?
- 25.6 Why do we use microservices?
- 25.7 What are the advantages of microservices?
- 25.8 What are the disadvantages of microservices?
- 25.9 When should you use microservices?
- 25.10 When should you avoid microservices?
- 25.11 How do you split a monolith into microservices?
- 25.12 What is service responsibility?
- 25.13 What is bounded context?
- 25.14 What is Domain-Driven Design?
- 25.15 How do microservices communicate?
- 25.16 What is synchronous communication?
- 25.17 What is asynchronous communication?
- 25.18 REST vs gRPC?
- 25.19 What is an API Gateway?
- 25.20 What is service discovery?
- 25.21 What is Database-per-Service?
- 25.22 How do services share data?
- 25.23 What is eventual consistency?
- 25.24 What is the Saga Pattern?
- 25.25 What is a compensating transaction?
- 25.26 What is distributed transaction?
- 25.27 What is event-driven architecture?
- 25.28 What is message-based communication?
- 25.29 What is a Circuit Breaker?
- 25.30 What is the Retry Pattern?
- 25.31 What is the Outbox Pattern?
- 25.32 What is distributed tracing?
- 25.33 How do you monitor microservices?
- 25.34 How do you secure service-to-service communication?
- 25.35 How do you deploy microservices independently?

# **26. Message Queues & Event-Driven Systems**

- 26.1 What is a message queue?
- 26.2 Why do we use message queues?
- 26.3 What is a message broker?
- 26.4 What is a producer?
- 26.5 What is a consumer?
- 26.6 What is a queue?
- 26.7 What is a topic?
- 26.8 Queue vs topic?
- 26.9 What is Pub/Sub?
- 26.10 What is RabbitMQ?
- 26.11 What is Apache Kafka?
- 26.12 What is Redis Queue?
- 26.13 RabbitMQ vs Kafka?
- 26.14 Kafka vs Redis Queue?
- 26.15 What is message acknowledgment?
- 26.16 What is message retry?
- 26.17 What is Dead Letter Queue?
- 26.18 What is message ordering?
- 26.19 What is duplicate message processing?
- 26.20 How do you prevent duplicate processing?
- 26.21 What is idempotent processing?
- 26.22 What is backpressure?
- 26.23 How do you scale consumers?
- 26.24 How do you handle failed consumers?
- 26.25 When should you use queues instead of direct API calls?

# **27. System Design for Node.js Developers**

- 27.1 What is system design?
- 27.2 What is high-level design?
- 27.3 What is low-level design?
- 27.4 What is scalability?
- 27.5 What is availability?
- 27.6 What is reliability?
- 27.7 What is fault tolerance?
- 27.8 What is redundancy?
- 27.9 What is a single point of failure?
- 27.10 What is load balancing?
- 27.11 What is caching?
- 27.12 What is a CDN?
- 27.13 What is database sharding?
- 27.14 What is database replication?
- 27.15 What is a read replica?
- 27.16 What is horizontal partitioning?
- 27.17 What is vertical partitioning?
- 27.18 What is distributed architecture?
- 27.19 What is eventual consistency?
- 27.20 What is CAP theorem?
- 27.21 What is consistency?
- 27.22 What is availability?
- 27.23 What is partition tolerance?
- 27.24 What is a CDN?
- 27.25 What is API Gateway?
- 27.26 What is a distributed cache?
- 27.27 How do you estimate API traffic?
- 27.28 How do you estimate database storage?
- 27.29 How do you design a scalable backend?
- 27.30 How do you identify system bottlenecks?

# **28. Testing Node.js Applications**

- 28.1 What is software testing?
- 28.2 Why do we test Node.js applications?
- 28.3 What is unit testing?
- 28.4 What is integration testing?
- 28.5 What is end-to-end testing?
- 28.6 Unit vs integration testing?
- 28.7 Integration vs end-to-end testing?
- 28.8 What is Jest?
- 28.9 What is Mocha?
- 28.10 What is Chai?
- 28.11 What is Supertest?
- 28.12 What is mocking?
- 28.13 What is stubbing?
- 28.14 What is spying?
- 28.15 Mock vs Stub vs Spy?
- 28.16 How do you test controllers?
- 28.17 How do you test services?
- 28.18 How do you test API endpoints?
- 28.19 How do you test authentication?
- 28.20 How do you test authorization?
- 28.21 How do you test error scenarios?
- 28.22 How do you mock database operations?
- 28.23 How do you test async code?
- 28.24 What is test coverage?
- 28.25 What is a CI testing pipeline?
- 28.26 How do you test a production-like environment?
- 28.27 How do you test background jobs?
- 28.28 How do you test Socket.IO applications?

# **29. Deployment & DevOps for Node.js**

- 29.1 What is deployment?
- 29.2 Development vs staging vs production?
- 29.3 What is Linux?
- 29.4 Basic Linux commands?
- 29.5 How do you deploy Node.js on Linux?
- 29.6 How do you configure a server?
- 29.7 What is SSH?
- 29.8 What is a server firewall?
- 29.9 What is Nginx?
- 29.10 What is PM2?
- 29.11 How do you manage production processes?
- 29.12 How do you manage environment variables?
- 29.13 How do you configure production secrets?
- 29.14 How do you configure HTTPS?
- 29.15 What is SSL/TLS?
- 29.16 What is Docker?
- 29.17 What is Docker Compose?
- 29.18 What is CI/CD?
- 29.19 What is Continuous Integration?
- 29.20 What is Continuous Delivery?
- 29.21 What is Continuous Deployment?
- 29.22 What is GitHub Actions?
- 29.23 What is a deployment pipeline?
- 29.24 How do you deploy automatically?
- 29.25 How do you rollback deployments?
- 29.26 How do you deploy without downtime?
- 29.27 How do you manage database migrations during deployment?
- 29.28 How do you manage logs in production?
- 29.29 How do you monitor production applications?
- 29.30 How do you troubleshoot production issues?

# **30. Logging, Monitoring & Observability**

- 30.1 What is logging?
- 30.2 Why do we need logging?
- 30.3 What is structured logging?
- 30.4 What is Winston?
- 30.5 What is Pino?
- 30.6 What is Morgan?
- 30.7 Winston vs Pino?
- 30.8 What is log rotation?
- 30.9 What is centralized logging?
- 30.10 What is monitoring?
- 30.11 What is observability?
- 30.12 What are logs?
- 30.13 What are metrics?
- 30.14 What are traces?
- 30.15 Logs vs metrics vs traces?
- 30.16 What is a correlation ID?
- 30.17 What is a request ID?
- 30.18 What is distributed tracing?
- 30.19 What is OpenTelemetry?
- 30.20 What is Prometheus?
- 30.21 What is Grafana?
- 30.22 What is alerting?
- 30.23 How do you monitor CPU usage?
- 30.24 How do you monitor memory usage?
- 30.25 How do you monitor API latency?
- 30.26 How do you monitor error rates?
- 30.27 How do you monitor database performance?
- 30.28 How do you monitor queue processing?
- 30.29 How do you monitor microservices?
- 30.30 How do you investigate production errors?

# **31. Git & Team Development**

- 31.1 What is Git?
- 31.2 What is GitHub?
- 31.3 Git vs GitHub?
- 31.4 What is a branch?
- 31.5 What is branching?
- 31.6 What is merging?
- 31.7 What is rebasing?
- 31.8 Merge vs rebase?
- 31.9 What is a Pull Request?
- 31.10 What is a Merge Request?
- 31.11 What is a merge conflict?
- 31.12 How do you resolve merge conflicts?
- 31.13 What is cherry-picking?
- 31.14 What is `git stash`?
- 31.15 What is `git revert`?
- 31.16 What is `git reset`?
- 31.17 Reset vs revert?
- 31.18 What is Git workflow?
- 31.19 What is feature branching?
- 31.20 What is GitFlow?
- 31.21 How do you collaborate with multiple developers?
- 31.22 How do you handle code reviews?
- 31.23 How do you manage release branches?
- 31.24 How do you rollback code using Git?
- 31.25 How do you resolve conflicts in a production release?

# **32. TypeScript for Node.js**

- 32.1 What is TypeScript?
- 32.2 Why do we use TypeScript with Node.js?
- 32.3 JavaScript vs TypeScript?
- 32.4 What is a Type?
- 32.5 What is an Interface?
- 32.6 Type vs Interface?
- 32.7 What is a Union Type?
- 32.8 What is an Intersection Type?
- 32.9 What is a Generic?
- 32.10 What is an Enum?
- 32.11 What is Type Inference?
- 32.12 What is Type Assertion?
- 32.13 What is `unknown`?
- 32.14 What is `any`?
- 32.15 `any` vs `unknown`?
- 32.16 What is `never`?
- 32.17 What is Optional Property?
- 32.18 What is Readonly?
- 32.19 What are Utility Types?
- 32.20 What is `Partial`?
- 32.21 What is `Pick`?
- 32.22 What is `Omit`?
- 32.23 What is `Record`?
- 32.24 How do you type Express requests and responses?
- 32.25 How do you type services and repositories?

# **33. DSA & Coding Interview Practice for Node.js**

## **Array**

- 33.1 Find the largest number.
- 33.2 Find the smallest number.
- 33.3 Find the second-largest number.
- 33.4 Reverse an array.
- 33.5 Remove duplicates.
- 33.6 Find duplicate elements.
- 33.7 Count occurrences.
- 33.8 Find missing numbers.
- 33.9 Merge two arrays.
- 33.10 Sort an array.
- 33.11 Find common elements.
- 33.12 Move zeros to the end.
- 33.13 Split an array into chunks.
- 33.14 Flatten a nested array.
- 33.15 Rotate an array.

## **String**

- 33.16 Reverse a string.
- 33.17 Check palindrome.
- 33.18 Count vowels.
- 33.19 Count character frequency.
- 33.20 Find duplicate characters.
- 33.21 Remove duplicate characters.
- 33.22 Find the first non-repeating character.
- 33.23 Check anagrams.
- 33.24 Reverse words in a sentence.
- 33.25 Capitalize each word.
- 33.26 Find the longest word.
- 33.27 Find the longest substring without repeating characters.

## **Object & Data Manipulation**

- 33.28 Group array objects by property.
- 33.29 Sort objects by property.
- 33.30 Find object duplicates.
- 33.31 Merge objects.
- 33.32 Convert an array into an object.
- 33.33 Convert an object into an array.
- 33.34 Count values in an array of objects.
- 33.35 Filter nested data.
- 33.36 Find an object by ID.
- 33.37 Remove an object by ID.
- 33.38 Update an object by ID.

## **Logic & Algorithms**

- 33.39 Fibonacci sequence.
- 33.40 Factorial.
- 33.41 Prime number.
- 33.42 Find GCD.
- 33.43 Find LCM.
- 33.44 Binary search.
- 33.45 Linear search.
- 33.46 Two Sum.
- 33.47 Frequency map.
- 33.48 Two-pointer technique.
- 33.49 Sliding window.
- 33.50 Recursion problems.

## **Node.js-specific coding tasks**

- 33.51 Implement a custom Promise-based function.
- 33.52 Implement a retry mechanism.
- 33.53 Implement a debounce function.
- 33.54 Implement a throttle function.
- 33.55 Implement a concurrency limiter.
- 33.56 Implement a simple task queue.
- 33.57 Implement a cache with TTL.
- 33.58 Implement an EventEmitter-like system.
- 33.59 Process a large file using Streams.
- 33.60 Implement a rate limiter.
- 33.61 Implement pagination.
- 33.62 Implement a request timeout.
- 33.63 Implement a Promise-based parallel task executor.
- 33.64 Handle multiple async operations with controlled concurrency.
- 33.65 Implement an idempotency check.

# **34. Real-World Scenario-Based Node.js Interview Questions**

**These are the types of questions interviewers ask when you have 3–5 years of experience.**

## **API & Backend Scenarios**

- 34.1 Your API takes 10 seconds to respond. How would you investigate?
- 34.2 Two users submit the same request simultaneously. How do you prevent duplicate data?
- 34.3 Your API receives an empty request body. How do you handle it?
- 34.4 Your API receives invalid data. How do you validate it?
- 34.5 Your API is receiving too many requests. How do you protect it?
- 34.6 Your API returns sensitive information. How do you fix it?
- 34.7 Your API has multiple filters and sorting options. How do you design it?
- 34.8 Your API returns 100,000 records. How do you optimize it?
- 34.9 Your API needs to handle multiple external API calls. How do you handle them?
- 34.10 Your API depends on an external service that is slow. How do you handle it?

## **Authentication & Security Scenarios**

- 34.11 A user's JWT expires while using the application. How do you handle it?
- 34.12 A user's Refresh Token is stolen. How do you handle it?
- 34.13 A user tries to access another user's data. How do you prevent it?
- 34.14 An admin and normal user access the same API. How do you restrict permissions?
- 34.15 Your login API receives 1,000 failed attempts. How do you protect it?
- 34.16 A user logs out, but the JWT is still valid. How do you handle it?
- 34.17 How do you implement secure password reset?
- 34.18 How do you protect a payment API from duplicate requests?
- 34.19 How do you secure file upload APIs?
- 34.20 How do you protect sensitive data in logs?

## **Database Scenarios**

- 34.21 A MongoDB query is slow. How do you investigate?
- 34.22 Your database has millions of records. How do you implement pagination?
- 34.23 Two customers try to purchase the last available product. How do you prevent overselling?
- 34.24 A user submits the same registration request twice. How do you prevent duplicate accounts?
- 34.25 Your API uses too many database connections. How do you solve it?
- 34.26 Your application needs data from multiple collections. How do you optimize it?
- 34.27 A database transaction fails. How do you handle it?
- 34.28 How do you implement search across large datasets?
- 34.29 How do you migrate database schema without breaking production?
- 34.30 How do you backup and restore production databases?

## **Architecture Scenarios**

- 34.31 How would you structure a large Node.js project?
- 34.32 How would you separate business logic from controllers?
- 34.33 How would you avoid duplicate logic across modules?
- 34.34 How would you design a reusable authentication system?
- 34.35 How would you design a multi-tenant application?
- 34.36 How would you design an e-commerce backend?
- 34.37 How would you design an order management system?
- 34.38 How would you design a payment integration?
- 34.39 How would you design an audit logging system?
- 34.40 How would you design a notification system?

## **Scaling & Performance Scenarios**

- 34.41 Your Node.js server CPU reaches 100%. What would you do?
- 34.42 Your application memory keeps increasing. How would you investigate?
- 34.43 Your application is running on one server. How would you scale it?
- 34.44 Your application needs to handle 50,000 concurrent users. How would you design it?
- 34.45 How would you handle a sudden traffic spike?
- 34.46 How would you scale a Node.js application across multiple CPU cores?
- 34.47 How would you implement zero-downtime deployment?
- 34.48 How would you handle a failed server?
- 34.49 How would you scale a real-time chat application?
- 34.50 How would you scale an application with multiple backend services?

## **Microservices & Distributed Systems Scenarios**

- 34.51 How would you split a monolithic application into microservices?
- 34.52 Your order service depends on a payment service. What happens if payment is unavailable?
- 34.53 How do you communicate between microservices?
- 34.54 How do you handle failures between microservices?
- 34.55 How do you maintain consistency across multiple databases?
- 34.56 How do you prevent duplicate queue messages?
- 34.57 How do you scale background job workers?
- 34.58 How do you trace a request across 10 microservices?
- 34.59 How do you secure communication between services?
- 34.60 How would you design a scalable microservices system?
