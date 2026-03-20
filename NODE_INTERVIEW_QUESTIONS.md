##  1. Node.js Basics

* [What is Node.js and how does it work?](#Node)
* [How is Node.js different from traditional server-side technologies?](#Node_different)
* [What is the V8 engine?](#V8_Engine)
* [What is non-blocking I/O?](#Non-Blocking)
* [What is event-driven architecture?](#Event-Driven)
* [Difference between synchronous and asynchronous code?](#Synchronous_Asynchronous)
* [What are global objects in Node.js?](#Global_Objects)


##  2. Modules & NPM

* [What are modules in Node.js?](#Modules)
* [Difference between CommonJS and ES Modules?](#CommonJS_ES_Modules)
* [What is `require()` vs `import`?](#require_import)
* [What is Module Caching?](#Module_Caching)
* [What is npm? What is npx?](#npm_npx)
* [Difference between dependencies and devDependencies?](#dev_dependencies)
* [What is package.json?](#package)
* [What is semantic versioning?](#Semantic)

---

##  3. File System (fs module)

* [How to read/write files in Node.js?](#read_write_files)
* [Difference between sync and async fs methods?](#Sync_Async)
* [What are streams in file handling?](#Streams)
* [How to handle large file processing?](#large_file_processing)
* [What is buffer in Node.js?](#Buffer)

---

##  4. Event Loop & Async Programming

* [What is the event loop?](#event_loop)
* [What are callbacks?](#callbacks)
* [What is callback hell?](#callback_hell)
* [What are Promises?](#Promises)
* [What is `process.nextTick()`?](#process_nextTick)

---


##  5. Express.js (Most Important)

* [What is Express.js?](#Express)
* [How does middleware work?](#Middleware)
* [What are route handlers?](#Handlers)
* [Difference between `app.use()` and `app.get()`?](#use_get)
* [What is error-handling middleware?](#Error-Handling)
* [How to structure a scalable Express app?](#structure_Express)

---

##  6. API & HTTP

* [How HTTP works in Node.js?](#HTTP_works)
* [What are headers, status codes?](#Headers_Status)
* What is CORS?
* What is REST vs GraphQL?
* [How to handle request validation?](#request_validation)

---

##  7. Database Integration

* [How to connect Node.js with MySQL/MongoDB?](#MySQL_MongoDB)
* [What is ORM/ODM?](#ORM_ODM)
* [Difference between SQL and NoSQL?](#SQL_NoSQL)
* [What is connection pooling?](#Connection_Pooling)
* [What are transactions?](#Transactions)

##  8. Authentication & Security

* [What is JWT?](#JWT)
* [What is OAuth?](#OAuth)
* [How password hashing works?](#Hashing)
* [What is bcrypt?](#bcrypt)
* [What are common security threats?](#Security_Threats)
* [What is rate limiting?](#Rate_Limiting)
* [What is Helmet.js?](#Helmet)

---

<!-- ##  9. Streams & Buffers

* What are streams?
* Types of streams?
* What is pipe()?
* Difference between buffer and stream?
* When to use streams? -->

---

##  10. Error Handling & Debugging

* [How to handle errors in Node.js?](#handle_errors)
* [Tools for debugging Node.js apps?](#Debugging)
* What are uncaught exceptions?
* What is logging?

---


##  11. Performance & Scaling

* [How to scale Node.js apps?](#scale_node)
* [What is clustering?](#Clustering)
* [What is load balancing?](#Load_Balancing)
* [What is PM2?](#PM2)
* [What are worker threads?](#Worker_Threads)
* [How to improve performance?](#improve_performance)

---

##  12. Testing

* What is unit testing?
* Tools like Jest, Mocha?
* What is mocking?
* What is integration testing?

---

##  13. DevOps & Deployment (Important for you 🔥)

* How to deploy Node.js app on server?
* What is Docker?
* What is CI/CD?
* How to use Nginx with Node.js?
* What is reverse proxy?
* Environment variables handling?
* Logging in production?

---


##  14. Advanced Topics

* [What is event emitter?](#Event_Emitter)
* [What is microservices architecture?](#Microservices)
* [What is WebSocket?](#WebSocket)
* What is message queue (RabbitMQ, Kafka)?

---



<hr style="border: 2px solid green;">

<h2 id="Node" style="color:green; text-align:center;">What is Node.js and how does it work?</h2>

- **Node.js Definition** – Node.js is a runtime environment to run JavaScript outside the browser
- **Built on V8 Engine** – Uses Google Chrome V8 Engine to execute code fast
- **Single Threaded** – Works on one main thread but handles many requests
- **Event Driven** – Uses events to manage multiple operations efficiently
- **Non-Blocking I/O** – Executes tasks without waiting (async execution)
- **Uses Event Loop** – Manages and processes requests in a loop system
- **Server-Side Usage** – Mainly used to build backend servers and APIs
- **Fast Performance** – Because of asynchronous and lightweight design




<hr style="border: 2px solid green;">

<h2 id="Node_different" style="color:green; text-align:center;">How is Node.js different from traditional server-side technologies?</h2>

- **Language** 🟢 – Uses JavaScript for backend
- **Thread** 🧵 – Single thread execution
- **Request Handling** ⚡ – Handles many requests at same time
- **Blocking Type** 🚫 – Non-blocking execution
- **Speed** 🚀 – Faster for real-time apps
- **Scalability** 📈 – Handles high traffic easily
- **Use Case** 🎯 – Best for APIs and real-time apps
- **Data Processing** 🔄 – Works with streams not full data


<hr style="border: 2px solid green;">

<h2 id="V8_Engine" style="color:green; text-align:center;">What is the V8 Engine?**</h2>


- **Definition** ⚙️ – JavaScript engine used to run JS code
- **Developed By** 🏢 – Built by Google
- **Used In** 🌐 – Used in Chrome browser and Node.js
- **Fast Execution** 🚀 – Converts JS into machine code
- **Improves Performance** ⚡ – Runs code very fast
- **No Interpreter Delay** ⏱️ – Direct execution without slow steps

<hr style="border: 2px solid green;">

<h2 id="Non-Blocking" style="color:green; text-align:center;">What is Non-Blocking I/O?</h2>


- **Definition** ⚙️ – Executes tasks without waiting
- **Async Work** 🔄 – Runs multiple operations at same time
- **No Waiting** ⏱️ – Does not stop next code execution
- **Better Performance** 🚀 – Handles more requests faster
- **Callback/Promise Use** 📦 – Uses async methods to manage results
- **Real-Time Use** 🌐 – Useful for APIs and live apps


<hr style="border: 2px solid green;">

<h2 id="Event-Driven" style="color:green; text-align:center;">What is Event-Driven Architecture?</h2>

- **Definition** ⚙️ – System works based on events
- **Event Meaning** 🔔 – Action like click, request, or message
- **Event Trigger** 🎯 – When event happens, code runs
- **Listener Use** 👂 – Listens and waits for events
- **Non-Blocking** 🚫 – Does not stop other tasks
- **Fast Response** ⚡ – Handles many events quickly
- **Real-Time Use** 🌐 – Used in chat apps and APIs

<hr style="border: 2px solid green;">

<h2 id="Synchronous_Asynchronous" style="color:green; text-align:center;">Difference between Synchronous and Asynchronous Code</h2>

**Difference between Synchronous and Asynchronous Code**

| Feature          | Synchronous ⏱️        | Asynchronous ⚡            |
| ---------------- | --------------------- | ------------------------- |
| **Execution** ▶️ | Runs one by one       | Runs multiple tasks       |
| **Waiting** 🛑   | Waits for each task   | Does not wait             |
| **Blocking** 🚫  | Blocking code         | Non-blocking code         |
| **Speed** 🚀     | Slower for many tasks | Faster for multiple tasks |
| **Usage** 🎯     | Simple operations     | APIs, file handling       |
| **Example** 💻   | `readFileSync()`      | `readFile()`              |


<hr style="border: 2px solid green;">

<h2 id="Global_Objects" style="color:green; text-align:center;">What are Global Objects in Node.js</h2>


- **Definition** 🌍 – Objects available everywhere in app
- **No Import Needed** 📦 – Can use directly without require
- **Global Scope** 🔓 – Accessible in all files
- **Examples** 🧾 – `global`, `process`, `console`
- **Useful For** 🛠️ – System info and debugging
- **Always Available** ⚡ – Works in every Node.js file


<hr style="border: 2px solid green;">

<h2 id="Modules" style="color:green; text-align:center;">What are Modules in Node.js?</h2>

- **Definition** 📦 – Small parts of code with specific task
- **Code Reuse** 🔁 – Same module can be used many times
- **Better Structure** 🧱 – Keeps code clean and organized
- **Import/Export** 🔄 – Share code using `require` or `import`
- **Types** 🧾 – Built-in, user-defined, third-party
- **Easy Maintenance** 🛠️ – Easy to update and manage code


<hr style="border: 2px solid green;">

<h2 id="CommonJS_ES_Modules" style="color:green; text-align:center;">Difference between CommonJS and ES Modules</h2>


| Feature          | CommonJS 📦           | ES Modules 🔄               |
| ---------------- | --------------------- | --------------------------- |
| **Syntax** 🧾    | `require()`           | `import`                    |
| **Export** 📤    | `module.exports`      | `export`                    |
| **Loading** ⏱️   | Synchronous           | Asynchronous                |
| **Usage** 🎯     | Older Node.js         | Modern JavaScript           |
| **File Type** 📄 | `.js`                 | `.mjs` / `"type": "module"` |
| **Standard** 🌐  | Node.js default (old) | Official JS standard        |


<hr style="border: 2px solid green;">

<h2 id="require_import" style="color:green; text-align:center;">What is `require()` vs `import`?</h2>


| Feature            | `require()` 📦    | `import` 🔄            |
| ------------------ | ----------------- | ---------------------- |
| **Module Type** 🧾 | CommonJS          | ES Modules             |
| **Syntax** ✍️      | `require('file')` | `import x from 'file'` |
| **Loading** ⏱️     | Synchronous       | Asynchronous           |
| **Usage** 🎯       | Older Node.js     | Modern JavaScript      |
| **Flexibility** 🔧 | Can use anywhere  | Top-level only         |
| **Standard** 🌐    | Not JS standard   | Official JS standard   |


<hr style="border: 2px solid green;">

<h2 id="Module_Caching" style="color:green; text-align:center;">What is Module Caching?</h2>


- **Definition** 📦 – Saving module in memory after first load
- **One Time Load** ⏱️ – Module runs only once
- **Reuse** 🔁 – Same module used again without reload
- **Faster Performance** 🚀 – Reduces loading time
- **Same Data** 🔗 – Shares same instance everywhere
- **Automatic Process** ⚙️ – Node.js handles caching automatically

<hr style="border: 2px solid green;">

<h2 id="npm_npx" style="color:green; text-align:center;">What is npm? What is npx?</h2>

**What is npm?**

- **Definition** 📦 – Package manager for Node.js
- **Full Form** 🧾 – Node Package Manager
- **Install Packages** ⬇️ – Used to install libraries
- **Manage Dependencies** 🔄 – Handles project packages
- **Global & Local** 🌐 – Install packages globally or locally
- **Registry Access** 🗂️ – Uses online package store

**What is npx?**

- **Definition** ⚡ – Tool to run packages without install
- **No Install Needed** 🚫 – Executes directly
- **One-Time Use** 🎯 – Best for temporary commands
- **Comes with npm** 📦 – Included in npm
- **Saves Time** ⏱️ – No need to install globally
- **Example Use** 💻 – Run create apps quickly

<hr style="border: 2px solid green;">

<h2 id="dev_dependencies" style="color:green; text-align:center;">Difference between dependencies and devDependencies</h2>

- **dependencies** 📦 – Needed to run the app
- **devDependencies** 🛠️ – Needed only for development
- **Usage (dependencies)** 🚀 – Used in production
- **Usage (devDependencies)** 🧪 – Used in testing/build
- **Install Time (dependencies)** ⬇️ – Installed always
- **Install Time (devDependencies)** ⚡ – Installed only in dev
- **Examples (dependencies)** 🌐 – Express, Axios
- **Examples (devDependencies)** 🔧 – Nodemon, ESLint

<hr style="border: 2px solid green;">

<h2 id="package" style="color:green; text-align:center;">What is package.json?</h2>

- **Definition** 📦 – Main file of Node.js project
- **Project Info** 🧾 – Stores name, version, details
- **Dependencies List** 🔗 – Contains required packages
- **Scripts Section** ▶️ – Stores run commands
- **Version Control** 🔄 – Manages package versions
- **Auto Created** ⚙️ – Created using `npm init`
- **Important File** ⭐ – Required for every project

<hr style="border: 2px solid green;">

<h2 id="Semantic" style="color:green; text-align:center;">What is Semantic Versioning?</h2>

- **Definition** 📦 – Version format for packages
- **Format** 🔢 – `MAJOR.MINOR.PATCH`
- **Major Version** 🚨 – Big changes, may break code
- **Minor Version** ✨ – New features, no break
- **Patch Version** 🛠️ – Bug fixes only
- **Example** 📊 – `1.2.3`
- **Easy Updates** 🔄 – Helps manage versions clearly

<hr style="border: 2px solid green;">

<h2 id="read_write_files" style="color:green; text-align:center;">How to read/write files in Node.js?</h2>

- **File Module** 📂 – Use built-in `fs` module
- **Read File** 📖 – Read data from file
- **Write File** ✍️ – Write data to file
- **Async Method** ⚡ – Non-blocking operations

**Code Example** 💻

```javascript
const fs = require('fs');

// Read File
fs.readFile('test.txt', 'utf8', (err, data) => {
  if (err) throw err;
  console.log("File Data:", data);
});

// Write File
fs.writeFile('test.txt', 'Hello Node.js', (err) => {
  if (err) throw err;
  console.log("File Written Successfully");
});
```

<hr style="border: 2px solid green;">

<h2 id="Sync_Async" style="color:green; text-align:center;">Difference between Sync and Async fs Methods</h2>


| Feature              | Sync Methods ⏱️        | Async Methods ⚡           |
| -------------------- | ---------------------- | ------------------------- |
| **Execution** ▶️     | Runs step by step      | Runs in background        |
| **Blocking** 🚫      | Blocks next code       | Non-blocking              |
| **Speed** 🚀         | Slower for large tasks | Faster for multiple tasks |
| **Usage** 🎯         | Simple scripts         | Real-time apps            |
| **Error Handling** ❗ | Uses try-catch         | Uses callback/promise     |
| **Example** 💻       | `fs.readFileSync()`    | `fs.readFile()`           |



<hr style="border: 2px solid green;">

<h2 id="Streams" style="color:green; text-align:center;">What are Streams in File Handling?</h2>


- **Definition** 🌊 – Process data in small chunks
- **No Full Load** 🚫 – No need to load full file
- **Memory Efficient** 💾 – Uses less memory
- **Faster Processing** ⚡ – Starts processing early
- **Types** 🔄 – Readable, Writable, Duplex

**Code Example** 💻

```javascript
const fs = require('fs');

// Read Stream
const readStream = fs.createReadStream('input.txt', 'utf8');

readStream.on('data', (chunk) => {
  console.log("Chunk:", chunk);
});

// Write Stream
const writeStream = fs.createWriteStream('output.txt');

writeStream.write('Hello Node.js\n');
writeStream.write('Stream Writing Example');
writeStream.end();
```

<hr style="border: 2px solid green;">

<h2 id="large_file_processing" style="color:green; text-align:center;">How to handle large file processing?</h2>


- **Use Streams** 🌊 – Process file in small chunks
- **Avoid Full Load** 🚫 – Do not load full file in memory
- **Use createReadStream** 📖 – Read file step by step
- **Use createWriteStream** ✍️ – Write data in parts
- **Pipe Method** 🔄 – Connect read and write streams
- **Memory Efficient** 💾 – Saves RAM usage
- **Better Performance** 🚀 – Faster for large files

**Code Example** 💻

```javascript
const fs = require('fs');

const readStream = fs.createReadStream('bigfile.txt');
const writeStream = fs.createWriteStream('copy.txt');

// Pipe for efficient processing
readStream.pipe(writeStream);
```

<hr style="border: 2px solid green;">

<h2 id="Buffer" style="color:green; text-align:center;">What is Buffer in Node.js?</h2>

- **Definition** 📦 – Temporary memory to store binary data
- **Used For** 🗂️ – Handle files, streams, network data
- **Raw Data** 🔢 – Stores data in bytes
- **No Encoding Needed** 🚫 – Works with binary directly
- **Fixed Size** 📏 – Size decided at creation

**Code Example** 💻

```javascript
// Create Buffer
const buf = Buffer.from('Hello');

// Print Buffer
console.log(buf);

// Convert Buffer to String
console.log(buf.toString());

// Create Empty Buffer
const buf2 = Buffer.alloc(10);
console.log(buf2);
```

<hr style="border: 2px solid green;">

<h2 id="event_loop" style="color:green; text-align:center;">🔁 Event Loop (Node.js)</h2>


* ⚡ **Single Thread**  → Node.js runs one task at a time
* 🚫 **Non-Blocking** → Doesn’t wait for slow tasks (API, timer)
* 🔄 **Handles Async Tasks** → Runs background tasks like `setTimeout`, API calls
* 📥 **Call Stack** → Where code runs (main execution place)
* 📩 **Callback Queue** → Stores completed async tasks
* 🔁 **Event Loop Work**
  → Checks: “Is stack empty?”
  → Yes → takes task from queue → runs it

---

#### 💻 Example

```js id="m8x2p1"
console.log("Start");

setTimeout(() => {
  console.log("Async");
}, 0);

console.log("End");
```

---

#### 📊 Output

```id="p3k9z2"
Start
End
Async
```
---


<hr style="border: 2px solid green;">

<h2 id="callbacks" style="color:green; text-align:center;">What are callbacks?</h2>

- 📞 **Callback = Function inside another function** → Passed as an argument
- 🔄 **Runs Later** → Executes after some task is done
- ⏱ **Used in Async** → For API calls, file read, timers
- 📥 **Triggered by Event Loop** → Runs when task is completed
- 🚫 **Non-Blocking** → Doesn’t stop main code execution

#### 💻 Example

```js id="cb01"
function greet(name, callback) {
  console.log("Hello " + name);
  callback();
}

greet("John", function() {
  console.log("Done");
});
```

---

#### 📊 Output

```id="cb02"
Hello John
Done
```

👉 **Callback = function passed + executed later**

<hr style="border: 2px solid green;">

<h2 id="callback_hell" style="color:green; text-align:center;">What is callback hell?</h2>


- 📞 **Too Many Nested Callbacks** → Callback inside callback inside callback
- 📉 **Hard to Read** → Code becomes messy and confusing
- 🐛 **Hard to Debug** → Difficult to find errors
- 🔁 **Deep Nesting** → Pyramid shape (goes more to right side)
- 🚫 **Not Maintainable** → Difficult to update or reuse code

---

#### 🧠 Simple Idea - “Callback inside callback again and again”

#### 💻 Example

```js id="cbh01"
setTimeout(() => {
  console.log("Step 1");

  setTimeout(() => {
    console.log("Step 2");

    setTimeout(() => {
      console.log("Step 3");
    }, 1000);

  }, 1000);

}, 1000);
```

#### 📊 Output

```id="cbh02"
Step 1
Step 2
Step 3
```

#### 🎯 Quick Remember

👉 **Callback Hell = Nested callbacks → messy code**

<hr style="border: 2px solid green;">

<h2 id="Promises" style="color:green; text-align:center;">What are Promises?</h2>

- **Definition** 📦 – Object for async result
- **States** 🔄 – Pending, Resolved, Rejected
- **Success Handle** ✅ – Uses `.then()`
- **Error Handle** ❌ – Uses `.catch()`
- **Better Than Callback** 👍 – Cleaner async code

**Code Example** 💻

```javascript id="l0a2ks"
const myPromise = new Promise((resolve, reject) => {
  let success = true;

  if (success) {
    resolve("Task Completed");
  } else {
    reject("Task Failed");
  }
});

myPromise
  .then((result) => {
    console.log(result);
  })
  .catch((error) => {
    console.log(error);
  });
```

👉 **Promise = async result (success or error)**

<hr style="border: 2px solid green;">

<h2 id="process_nextTick" style="color:green; text-align:center;">What is `process.nextTick()`?</h2>

- ⚡ **Runs Immediately After Current Code** → Executes before event loop continues
- 📌 **Higher Priority** → Runs before `setTimeout` and `setImmediate`
- 🔄 **Not Part of Event Loop Phases** → Runs in **next tick queue** (special queue)
- 📥 **Executes Before Callback Queue** → Faster than other async tasks
- 🚫 **Can Block Event Loop** → Too many `nextTick` → delays other tasks


#### 💻 Example

```js id="nt01"
console.log("Start");

process.nextTick(() => {
  console.log("NextTick");
});

console.log("End");
```

#### 📊 Output

```id="nt02"
Start
End
NextTick
```

#### 🎯 Quick Remember -> **process.nextTick() = run before all async tasks**

<hr style="border: 2px solid green;">

<h2 id="Express" style="color:green; text-align:center;">What is Express.js?</h2>

- **Definition** 🚀 – Web framework for Node.js
- **Purpose** 🎯 – Build APIs and web apps
- **Fast Setup** ⚡ – Easy server creation
- **Routing** 🛣️ – Handle different URLs
- **Middleware** 🔄 – Process request/response
- **Lightweight** 🪶 – Minimal and flexible
- **Widely Used** 🌐 – Popular in backend development


<hr style="border: 2px solid green;">

<h2 id="Middleware" style="color:green; text-align:center;">How does Middleware work?</h2>


- **Definition** 🔄 – Function between request and response
- **Execution Flow** ▶️ – Runs before final response
- **Next Function** ⏭️ – Pass control using `next()`
- **Multiple Layers** 🧱 – Can use many middleware
- **Use Cases** 🎯 – Logging, auth, validation

**Simple Code Example** 💻

```javascript id="k3f9l2"
const express = require('express');
const app = express();

// Middleware
app.use((req, res, next) => {
  console.log("Request Received");
  next(); // move to next
});

// Route
app.get('/', (req, res) => {
  res.send("Hello World");
});

app.listen(3000);
```

<hr style="border: 2px solid green;">

<h2 id="Route_Handlers" style="color:green; text-align:center;">What are Route Handlers?</h2>

- **Definition** 🛣️ – Functions to handle requests
- **URL Based** 🌐 – Works for specific route (URL)
- **Request & Response** 🔄 – Gets `req` and sends `res`
- **Different Methods** 📬 – GET, POST, PUT, DELETE
- **Used In Express** 🚀 – Core part of routing

**Simple Code Example** 💻

```javascript id="p9x2d1"
const express = require('express');
const app = express();

// Route Handler - GET
app.get('/', (req, res) => {
  res.send("Home Page");
});

// Route Handler - POST
app.post('/user', (req, res) => {
  res.send("User Created");
});

app.listen(3000);
```

<hr style="border: 2px solid green;">

<h2 id="use_get" style="color:green; text-align:center;">Difference between `app.use()` and `app.get()`</h2>


| Feature             | `app.use()` 🔄                  | `app.get()` 📬               |
| ------------------- | ------------------------------- | ---------------------------- |
| **Purpose** 🎯      | Used for middleware             | Used for GET routes          |
| **URL Matching** 🌐 | Matches all HTTP methods        | Matches only GET requests    |
| **Path Usage** 🛣️  | Optional path prefix            | Specific route path          |
| **Execution** ▶️    | Runs for every matching request | Runs only for GET request    |
| **Use Case** 🧱     | Logging, auth, parsing          | Sending response for GET API |

**Simple Example** 💻

```javascript id="m2k8q7"
const express = require('express');
const app = express();

// Middleware
app.use((req, res, next) => {
  console.log("Middleware runs");
  next();
});

// GET Route
app.get('/', (req, res) => {
  res.send("Home Page");
});

app.listen(3000);
```


<hr style="border: 2px solid green;">

<h2 id="AAAAAAAAAAAAAAAAA" style="color:green; text-align:center;">What is Error-Handling Middleware?</h2>

- **Definition** ⚠️ – Middleware used to handle errors
- **Special Signature** 🧾 – Uses `(err, req, res, next)`
- **Error Catching** 🛑 – Captures errors from routes/middleware
- **Central Handling** 🎯 – Manages all errors in one place
- **Response Sending** 📤 – Sends proper error response

**Simple Code Example** 💻

```javascript id="err1x2"
const express = require('express');
const app = express();

// Route with error
app.get('/', (req, res, next) => {
  const error = new Error("Something went wrong");
  next(error); // pass error to middleware
});

// Error-handling middleware
app.use((err, req, res, next) => {
  console.log(err.message);
  res.status(500).send("Server Error");
});

app.listen(3000);
```


<hr style="border: 2px solid green;">

<h2 id="AAAAAAAAAAAAAAAAA" style="color:green; text-align:center;">What is Error-Handling Middleware?</h2>


- **Definition** ⚠️ – Middleware used to handle errors in Express
- **Special Parameters** 🧾 – Uses `(err, req, res, next)`
- **Error Capture** 🛑 – Catches errors from routes or middleware
- **Central Control** 🎯 – Handles all errors in one place
- **Response** 📤 – Sends error message to client

**Simple Code Example** 💻

```javascript id="e5r7t3"
const express = require('express');
const app = express();

// Route that creates error
app.get('/', (req, res, next) => {
  next(new Error("Error occurred"));
});

// Error-handling middleware
app.use((err, req, res, next) => {
  res.status(500).send(err.message);
});

app.listen(3000);
```


<hr style="border: 2px solid green;">

<h2 id="structure_Express" style="color:green; text-align:center;">How to structure a scalable Express app?</h2>



- **Folder Structure** 🧱 – Separate files by feature (routes, controllers, services)
- **Routes Layer** 🛣️ – Define API endpoints only
- **Controllers Layer** 🎮 – Handle request & response logic
- **Services Layer** ⚙️ – Business logic and processing
- **Models Layer** 🗄️ – Database schema and queries
- **Middleware** 🔄 – Common logic like auth, logging
- **Config Files** ⚙️ – Environment and database configs
- **Error Handling** ⚠️ – Centralized error middleware
- **Modular Code** 📦 – Keep features independent and reusable

**Example Folder Structure** 📁

```
project/
 ├── routes/
 ├── controllers/
 ├── services/
 ├── models/
 ├── middleware/
 ├── config/
 ├── app.js
 └── server.js
```


<hr style="border: 2px solid green;">

<h2 id="HTTP_works" style="color:green; text-align:center;">How HTTP works in Node.js</h2>

- **HTTP Module** 🌐 – Uses built-in `http` module to create server
- **Request Handling** 📥 – Server receives request object (`req`)
- **Response Sending** 📤 – Sends response using `res.end()`
- **Server Creation** 🖥️ – Uses `http.createServer()`
- **Event Driven** 🔔 – Callback runs for every request
- **Simple Response** ⚡ – Send same response for all requests

**Simple Code Example** 💻

```javascript id="http2x3"
const http = require('http');

const server = http.createServer((req, res) => {
  res.writeHead(200, { 'Content-Type': 'text/plain' });
  res.end('Hello from Node.js server');
});

server.listen(3000, () => {
  console.log("Server running on port 3000");
});
```


<hr style="border: 2px solid green;">

<h2 id="Headers_Status" style="color:green; text-align:center;">What are Headers and Status Codes?</h2>


- **Headers** 🧾 – Extra information sent with request/response
- **Headers Use** 🔄 – Define content type, auth, caching
- **Example Headers** 📦 – `Content-Type`, `Authorization`, `Accept`
- **Status Codes** 🔢 – Numbers showing result of request
- **Success Code** ✅ – `200` means OK
- **Client Error** ❌ – `404` means Not Found
- **Server Error** ⚠️ – `500` means Server Error
- **Purpose** 🎯 – Tell client what happened with request

**Simple Code Example** 💻

```javascript id="hdr1x2"
const http = require('http');

const server = http.createServer((req, res) => {
  res.writeHead(200, {
    'Content-Type': 'text/plain',
    'Custom-Header': 'MyHeader'
  });

  res.end('Headers and Status Code Example');
});

server.listen(3000);
```


<hr style="border: 2px solid green;">

<h2 id="request_validation" style="color:green; text-align:center;">How to handle request validation?</h2>



- **Validation Libraries** 📚 – Use packages like `express-validator`
- **Schema Validation** 🧾 – Define rules for request data
- **Middleware Based** 🔄 – Validation done before controller
- **Cleaner Code** 🧱 – Separates validation from logic
- **Reusable Rules** 🔁 – Same validation used in multiple routes

**Simple Code Example (express-validator)** 💻

```javascript id="val2x3"
const express = require('express');
const { body, validationResult } = require('express-validator');

const app = express();
app.use(express.json());

app.post(
  '/user',
  [
    body('name').notEmpty().withMessage('Name is required'),
    body('age').isInt().withMessage('Age must be a number')
  ],
  (req, res) => {
    const errors = validationResult(req);

    if (!errors.isEmpty()) {
      return res.status(400).json({ errors: errors.array() });
    }

    res.send("Valid data");
  }
);

app.listen(3000);
```


<hr style="border: 2px solid green;">

<h2 id="MySQL_MongoDB" style="color:green; text-align:center;">How to connect Node.js with MySQL/MongoDB?</h2>


### 🔹 **MySQL Connection** 🗄️

- **Library** 📦 – Use `mysql2` package
- **Connection** 🔗 – Create connection using config
- **Query Execution** ⚡ – Run SQL queries using connection

**Code Example** 💻

```javascript id="sql1x2"
const mysql = require('mysql2');

const connection = mysql.createConnection({
  host: 'localhost',
  user: 'root',
  password: '',
  database: 'test_db'
});

connection.connect();

connection.query('SELECT * FROM users', (err, results) => {
  if (err) throw err;
  console.log(results);
});

connection.end();
```

---

### 🔹 **MongoDB Connection** 🍃

- **Library** 📦 – Use `mongoose` or `mongodb` driver
- **Connection** 🔗 – Connect using connection string
- **Schema Use** 🧾 – Define models (in Mongoose)

**Code Example** 💻

```javascript id="mongo1x2"
const mongoose = require('mongoose');

mongoose.connect('mongodb://127.0.0.1:27017/test_db')
  .then(() => console.log("MongoDB Connected"))
  .catch(err => console.log(err));
```



<hr style="border: 2px solid green;">

<h2 id="ORM_ODM" style="color:green; text-align:center;">What is ORM / ODM?</h2>


| Feature               | ORM 🗄️                    | ODM 🍃                      |
| --------------------- | -------------------------- | --------------------------- |
| **Full Form** 🧾      | Object Relational Mapping  | Object Document Mapping     |
| **Database Type** 🗂️ | SQL (MySQL, PostgreSQL)    | NoSQL (MongoDB)             |
| **Data Structure** 📊 | Tables & Rows              | Documents (JSON-like)       |
| **Query Style** 🔍    | No raw SQL needed          | No raw Mongo queries needed |
| **Tools** 🛠️         | Sequelize, TypeORM         | Mongoose                    |
| **Purpose** 🎯        | Map tables to objects      | Map documents to objects    |
| **Usage** 🚀          | Structured relational data | Flexible schema data        |

---

### **Code Example (ORM - Sequelize MySQL)** 💻

```javascript id="orm1x2"
const { Sequelize, DataTypes } = require('sequelize');

const sequelize = new Sequelize('test_db', 'root', '', {
  host: 'localhost',
  dialect: 'mysql'
});

const User = sequelize.define('User', {
  name: DataTypes.STRING,
  age: DataTypes.INTEGER
});

(async () => {
  await sequelize.sync();
  const users = await User.findAll();
  console.log(users);
})();
```

---

### **Code Example (ODM - Mongoose MongoDB)** 💻

```javascript id="odm1x2"
const mongoose = require('mongoose');

mongoose.connect('mongodb://127.0.0.1:27017/test_db');

const userSchema = new mongoose.Schema({
  name: String,
  age: Number
});

const User = mongoose.model('User', userSchema);

(async () => {
  const users = await User.find();
  console.log(users);
})();
```


<hr style="border: 2px solid green;">

<h2 id="SQL_NoSQL" style="color:green; text-align:center;">Difference between SQL and NoSQL</h2>


| Feature               | SQL 🗄️                      | NoSQL 🍃                       |
| --------------------- | ---------------------------- | ------------------------------ |
| **Database Type** 🧾  | Relational database          | Non-relational database        |
| **Structure** 📊      | Tables with rows & columns   | Documents / key-value / graphs |
| **Schema** 📐         | Fixed schema                 | Flexible schema                |
| **Scalability** 📈    | Vertical scaling             | Horizontal scaling             |
| **Query Language** 🔍 | Uses SQL queries             | No standard query language     |
| **Relationships** 🔗  | Strong relationships (joins) | Limited or no joins            |
| **Examples** 🧾       | MySQL, PostgreSQL            | MongoDB, Redis                 |
| **Use Case** 🎯       | Structured data              | Unstructured or dynamic data   |

---

### **Simple Code Example (SQL - MySQL)** 💻

```javascript id="sql2x3"
const mysql = require('mysql2');

const connection = mysql.createConnection({
  host: 'localhost',
  user: 'root',
  password: '',
  database: 'test_db'
});

connection.query('SELECT * FROM users', (err, results) => {
  console.log(results);
});
```

---

### **Simple Code Example (NoSQL - MongoDB)** 💻

```javascript id="nosql2x3"
const mongoose = require('mongoose');

mongoose.connect('mongodb://127.0.0.1:27017/test_db');

const User = mongoose.model('User', new mongoose.Schema({
  name: String,
  age: Number
}));

(async () => {
  const users = await User.find();
  console.log(users);
})();
```


<hr style="border: 2px solid green;">

<h2 id="Connection_Pooling" style="color:green; text-align:center;">What is Connection Pooling?</h2>


- **Definition** 🔗 – Reuse database connections instead of creating new ones
- **Connection Reuse** 🔁 – Uses existing connections from a pool
- **Performance** 🚀 – Reduces time to connect to database
- **Resource Efficient** 💾 – Avoids creating too many connections
- **Concurrency** ⚡ – Handles multiple requests at same time
- **Common Use** 🗄️ – Used in MySQL, PostgreSQL, MongoDB apps

**Simple Code Example (MySQL Pool)** 💻

```javascript id="pool1x2"
const mysql = require('mysql2');

const pool = mysql.createPool({
  host: 'localhost',
  user: 'root',
  password: '',
  database: 'test_db',
  connectionLimit: 10
});

pool.query('SELECT * FROM users', (err, results) => {
  if (err) throw err;
  console.log(results);
});
```


<hr style="border: 2px solid green;">

<h2 id="Transactions" style="color:green; text-align:center;">What are Transactions?</h2>


- **Definition** 🔄 – Group of database operations treated as one unit
- **All or Nothing** ⚖️ – Either all succeed or all fail
- **Consistency** ✅ – Keeps data accurate and reliable
- **Rollback** ↩️ – Undo changes if error occurs
- **Commit** 💾 – Save changes permanently
- **Use Case** 🎯 – Bank transfer, multi-step updates

**Simple Code Example (MySQL Transaction)** 💻

```javascript id="txn1x2"
const mysql = require('mysql2');

const connection = mysql.createConnection({
  host: 'localhost',
  user: 'root',
  password: '',
  database: 'test_db'
});

connection.beginTransaction((err) => {
  if (err) throw err;

  connection.query('UPDATE accounts SET balance = balance - 100 WHERE id = 1', (err) => {
    if (err) {
      return connection.rollback(() => {
        console.log("Rollback due to error");
      });
    }

    connection.query('UPDATE accounts SET balance = balance + 100 WHERE id = 2', (err) => {
      if (err) {
        return connection.rollback(() => {
          console.log("Rollback due to error");
        });
      }

      connection.commit((err) => {
        if (err) {
          return connection.rollback();
        }
        console.log("Transaction Successful");
      });
    });
  });
});
```


<hr style="border: 2px solid green;">

<h2 id="JWT" style="color:green; text-align:center;">What is JWT (JSON Web Token)?</h2>

- **Definition** 🔐 – Token used for authentication and authorization
- **Structure** 🧾 – Consists of Header, Payload, Signature
- **Stateless** 🌐 – No need to store session on server
- **Secure** 🔒 – Signed to prevent tampering
- **Used For** 🎯 – Login, API authentication
- **Compact Format** 📦 – Easy to send in headers or URL

**Simple Code Example** 💻

```javascript id="jwt1x2"
const jwt = require('jsonwebtoken');

// Create Token
const token = jwt.sign({ userId: 1 }, 'secretKey', { expiresIn: '1h' });

console.log("Token:", token);

// Verify Token
const decoded = jwt.verify(token, 'secretKey');
console.log("Decoded:", decoded);
```


<hr style="border: 2px solid green;">

<h2 id="OAuth" style="color:green; text-align:center;">What is OAuth?</h2>



- **Definition** 🔐 – Authorization framework for secure access
- **Purpose** 🎯 – Allow apps to access user data without password
- **Token Based** 🎟️ – Uses access tokens instead of credentials
- **Third-Party Login** 🌐 – Login with Google, Facebook, etc.
- **Secure Access** 🔒 – User grants limited permissions
- **No Password Sharing** 🚫 – Credentials are never shared with app
- **Use Case** 📱 – Social login, API access between services




<hr style="border: 2px solid green;">

<h2 id="Hashing" style="color:green; text-align:center;">How Password Hashing Works?</h2>


- **Definition** 🔐 – Converts password into encrypted format
- **One-Way Process** 🚫 – Cannot reverse original password
- **Hash Function** ⚙️ – Uses algorithms like bcrypt
- **Salt Added** 🧂 – Random data added for extra security
- **Store Hash Only** 💾 – Password itself is never saved
- **Verification** ✅ – Compare entered password with stored hash

**Simple Code Example (bcrypt)** 💻

```javascript id="hash1x2"
const bcrypt = require('bcrypt');

const password = "mypassword";

// Hash Password
bcrypt.hash(password, 10, (err, hash) => {
  console.log("Hashed Password:", hash);

  // Compare Password
  bcrypt.compare(password, hash, (err, result) => {
    console.log("Password Match:", result);
  });
});
```


<hr style="border: 2px solid green;">

<h2 id="bcrypt" style="color:green; text-align:center;">What is bcrypt?</h2>


- **Definition** 🔐 – Password hashing library
- **Purpose** 🎯 – Securely store passwords
- **One-Way Hash** 🚫 – Cannot get original password back
- **Salt Included** 🧂 – Adds random data for security
- **Slow Hashing** ⏳ – Designed to prevent brute-force attacks
- **Common Use** 🛠️ – Used in authentication systems


<hr style="border: 2px solid green;">

<h2 id="Security_Threats" style="color:green; text-align:center;">What are Common Security Threats?</h2>


- **SQL Injection** 💉 – Malicious SQL queries injected into inputs
- **Cross-Site Scripting (XSS)** 🧠 – Injecting scripts into web pages
- **Cross-Site Request Forgery (CSRF)** 🔁 – Unauthorized actions on behalf of user
- **Authentication Attacks** 🔓 – Weak passwords or brute force attacks
- **Man-in-the-Middle (MITM)** 🕵️ – Intercepting data between client and server
- **Denial of Service (DoS/DDoS)** 🚫 – Overloading server with traffic
- **Data Breach** 📂 – Unauthorized access to sensitive data
- **Insecure APIs** 🌐 – Poorly protected endpoints exposed to attacks


<hr style="border: 2px solid green;">

<h2 id="Rate_Limiting" style="color:green; text-align:center;">What is Rate Limiting?</h2>

- **Definition** 🚦 – Limits number of requests from a user
- **Purpose** 🎯 – Prevent abuse and overload
- **Request Control** ⛔ – Restricts too many requests in time
- **Security** 🔒 – Protects from attacks like DDoS
- **Performance** 🚀 – Keeps server stable
- **Use Case** 🌐 – APIs, login attempts, public endpoints

**Simple Code Example (Express + rate-limit)** 💻

```javascript id="rate1x2"
const express = require('express');
const rateLimit = require('express-rate-limit');

const app = express();

const limiter = rateLimit({
  windowMs: 1 * 60 * 1000, // 1 minute
  max: 5 // limit each IP to 5 requests
});

app.use(limiter);

app.get('/', (req, res) => {
  res.send("Rate limiting applied");
});

app.listen(3000);
```


<hr style="border: 2px solid green;">

<h2 id="Helmet" style="color:green; text-align:center;">What is Helmet.js?</h2>


- **Definition** 🪖 – Security middleware for Express apps
- **Purpose** 🎯 – Protects app by setting HTTP headers
- **Security Headers** 🔐 – Adds headers like `Content-Security-Policy`
- **Prevents Attacks** 🛡️ – Helps against XSS, clickjacking
- **Easy to Use** ⚡ – Simple middleware setup
- **Best Practice** ✅ – Commonly used in production apps

**Simple Code Example** 💻

```javascript id="helmet1x2"
const express = require('express');
const helmet = require('helmet');

const app = express();

// Use Helmet
app.use(helmet());

app.get('/', (req, res) => {
  res.send("Secure App with Helmet");
});

app.listen(3000);
```


<hr style="border: 2px solid green;">

<h2 id="handle_errors" style="color:green; text-align:center;">How to handle errors in Node.js?</h2>


- **Try-Catch** 🛑 – Handle errors in synchronous code
- **Callbacks** 📞 – Check `err` in callback functions
- **Promises** 🔄 – Use `.catch()` for errors
- **Async/Await** ⚡ – Use try-catch with async code
- **Error Middleware** ⚠️ – Handle errors in Express
- **Custom Errors** 🧾 – Create your own error messages


**Simple Code Example** 💻

```javascript id="err2x3"
// Try-Catch (Sync)
try {
  throw new Error("Sync Error");
} catch (err) {
  console.log(err.message);
}

// Promise Error
Promise.reject("Promise Error")
  .catch(err => console.log(err));

// Async/Await Error
async function test() {
  try {
    throw new Error("Async Error");
  } catch (err) {
    console.log(err.message);
  }
}

test();
```


<hr style="border: 2px solid green;">

<h2 id="Debugging" style="color:green; text-align:center;">Tools for Debugging Node.js Apps</h2>

- **Built-in Debugger** 🐞 – Use `node inspect` for debugging
- **Console Logs** 🧾 – Use `console.log()` for quick checks
- **Chrome DevTools** 🌐 – Debug using Chrome browser tools
- **VS Code Debugger** 💻 – Built-in debugger in VS Code
- **Nodemon** 🔄 – Auto restart app on changes
- **Debug Package** 📦 – Use `debug` library for logs
- **Postman** 📬 – Test APIs and responses
- **Logging Tools** 📊 – Use Winston or Morgan for logs


<hr style="border: 2px solid green;">

<h2 id="scale_node" style="color:green; text-align:center;">How to scale Node.js apps?</h2>

- **Clustering** 🧵 – Use multiple CPU cores
- **Load Balancer** ⚖️ – Distribute traffic across servers
- **PM2 Tool** 🚀 – Manage and run multiple instances
- **Microservices** 🧩 – Split app into small services
- **Caching** 💾 – Use Redis to reduce load
- **Database Scaling** 🗄️ – Use replication or sharding
- **Async Code** ⚡ – Use non-blocking operations
- **Cloud Deployment** ☁️ – Use AWS, Docker, Kubernetes



<hr style="border: 2px solid green;">

<h2 id="Clustering" style="color:green; text-align:center;">What is Clustering?</h2>

- **Definition** 🧵 – Running multiple Node.js processes
- **CPU Usage** ⚙️ – Uses all CPU cores
- **Same App** 🔁 – Each process runs same code
- **Load Sharing** ⚖️ – Distributes requests between processes
- **Better Performance** 🚀 – Handles more traffic
- **Fault Tolerance** 🛡️ – If one fails, others continue

**Simple Code Example** 💻

```javascript id="clus1x2"
const cluster = require('cluster');
const os = require('os');

if (cluster.isMaster) {
  const cpuCount = os.cpus().length;

  for (let i = 0; i < cpuCount; i++) {
    cluster.fork(); // create workers
  }
} else {
  const http = require('http');

  http.createServer((req, res) => {
    res.end("Handled by worker " + process.pid);
  }).listen(3000);
}
```


<hr style="border: 2px solid green;">

<h2 id="Load_Balancing" style="color:green; text-align:center;">What is Load Balancing?</h2>


- **Definition** ⚖️ – Distributes traffic across multiple servers
- **Purpose** 🎯 – Prevents server overload
- **Traffic Split** 🔄 – Sends requests to different instances
- **Improves Performance** 🚀 – Faster response time
- **High Availability** 🛡️ – If one server fails, others handle
- **Scalability** 📈 – Supports more users easily
- **Common Tools** 🛠️ – Nginx, AWS ELB


<hr style="border: 2px solid green;">

<h2 id="PM2" style="color:green; text-align:center;">What is PM2?</h2>

- **Definition** 🚀 – Process manager for Node.js apps
- **Run Apps** ▶️ – Starts and manages applications
- **Auto Restart** 🔄 – Restarts app if it crashes
- **Cluster Mode** 🧵 – Runs multiple instances
- **Monitoring** 📊 – Shows CPU and memory usage
- **Log Management** 🧾 – Stores and manages logs
- **Production Use** 🌐 – Used in live server apps

**Simple Command Example** 💻

```bash
# Install PM2
npm install -g pm2

# Start app
pm2 start app.js

# View status
pm2 list
```


<hr style="border: 2px solid green;">

<h2 id="Worker_Threads" style="color:green; text-align:center;">What are Worker Threads?</h2>


- **Definition** 🧵 – Run code in separate threads
- **Purpose** 🎯 – Handle heavy CPU tasks
- **Parallel Work** ⚡ – Runs tasks in parallel
- **Non-Blocking** 🚫 – Keeps main thread free
- **Better Performance** 🚀 – Improves speed for heavy work
- **Data Sharing** 🔗 – Can share data using messages

**Simple Code Example** 💻

```javascript id="wrk1x2"
const { Worker, isMainThread, parentPort } = require('worker_threads');

if (isMainThread) {
  // Main Thread
  const worker = new Worker(__filename);

  worker.on('message', (msg) => {
    console.log("From Worker:", msg);
  });

} else {
  // Worker Thread
  parentPort.postMessage("Task Done");
}
```


<hr style="border: 2px solid green;">

<h2 id="improve_performance" style="color:green; text-align:center;">How to improve performance in Node.js?</h2>



- **Use Async Code** ⚡ – Avoid blocking operations, use async/await or promises
- **Use Caching** 💾 – Store frequently used data (Redis) to reduce DB calls
- **Use Streams** 🌊 – Process large files in chunks, not full load
- **Clustering** 🧵 – Use multiple CPU cores for better performance
- **Load Balancing** ⚖️ – Distribute traffic across multiple servers
- **Optimize Queries** 🗄️ – Write efficient database queries and use indexes
- **Use Compression** 📦 – Reduce response size using gzip
- **Limit Logs** 🧾 – Avoid too many console logs in production
- **Use Worker Threads** 🔄 – Handle CPU-heavy tasks separately
- **Monitor App** 📊 – Track CPU, memory, and performance regularly



<hr style="border: 2px solid green;">

<h2 id="Event_Emitter" style="color:green; text-align:center;">Event_Emitter</h2>


**What is Event Emitter? (Simple Clear Explanation)**

- **Definition** 🔔 – Used to create and handle custom events in Node.js
- **Think Like This** 💡 – One part sends signal, another part listens
- **Emit** 📢 – `emit()` sends event (like button click)
- **Listener** 👂 – `on()` waits and runs code when event happens
- **Flow** 🔄 – Emit → Listener catches → Code runs
- **Decoupled Code** 🧱 – Sender and receiver are separate
- **Real Use** 🌐 – Used in HTTP, streams, real-time apps

**Step-by-Step Code Example** 💻

```javascript id="evt2x3"
const EventEmitter = require('events');

const emitter = new EventEmitter();

// Step 1: Create Listener
emitter.on('login', (user) => {
  console.log(user + " logged in");
});

// Step 2: Emit Event
emitter.emit('login', "John");
```

🔹 **Output** 📤 – `John logged in`



<hr style="border: 2px solid green;">

<h2 id="Microservices" style="color:green; text-align:center;">What is Microservices Architecture?</h2>

- **Definition** 🧩 – App is divided into small independent services
- **Independent Services** 🔄 – Each service works separately
- **Single Responsibility** 🎯 – One service = one task
- **Communication** 🔗 – Services talk using APIs
- **Easy Scaling** 📈 – Scale only needed service
- **Better Maintenance** 🛠️ – Easy to update small parts
- **Technology Flexibility** ⚙️ – Each service can use different tech
- **Example** 🌐 – User service, Payment service, Order service

<hr style="border: 2px solid green;">

<h2 id="WebSocket" style="color:green; text-align:center;">What is WebSocket?</h2>

- **Definition** 🌐 – Protocol for real-time communication
- **Full Duplex** 🔄 – Send and receive data both ways
- **Persistent Connection** 🔗 – Connection stays open
- **Real-Time Data** ⚡ – Instant data transfer
- **No Reconnect** 🚫 – No need to request again and again
- **Low Latency** 🚀 – Faster than HTTP for live data
- **Use Case** 🎯 – Chat apps, live updates, gaming

**Simple Code Example** 💻

```javascript id="ws1x2"
const WebSocket = require('ws');

const server = new WebSocket.Server({ port: 3000 });

server.on('connection', (ws) => {
  ws.send("Connected");

  ws.on('message', (msg) => {
    console.log("Received:", msg);
  });
});
```



====================================

# 🟢 1. Create Server (Without Express)

**Question:** How do you create a basic HTTP server in Node.js?

```js
const http = require('http');

const server = http.createServer((req, res) => {
    res.writeHead(200, { 'Content-Type': 'text/plain' });
    res.end('Hello World');
});

server.listen(3000, () => {
    console.log('Server running on port 3000');
});
```

---

# 🟡 2. Create Server (With Express)

**Question:** How do you create a server using Express?

```js
const express = require('express');
const app = express();

app.get('/', (req, res) => {
    res.send('Hello Express');
});

app.listen(3000, () => {
    console.log('Server running on port 3000');
});
```

---

# 🔵 3. Create Middleware

**Question:** How do you create custom middleware in Express?

```js
const logger = (req, res, next) => {
    console.log(`${req.method} ${req.url}`);
    next();
};

app.use(logger);
```

---

# 🟣 4. Connect MySQL

**Question:** How to connect Node.js with MySQL?

```js
const mysql = require('mysql2');

const connection = mysql.createConnection({
    host: 'localhost',
    user: 'root',
    password: '',
    database: 'test'
});

connection.connect(err => {
    if (err) throw err;
    console.log('MySQL Connected');
});
```

---

# 🔴 5. Connect MongoDB

**Question:** How to connect Node.js with MongoDB?

```js
const mongoose = require('mongoose');

mongoose.connect('mongodb://127.0.0.1:27017/test')
    .then(() => console.log('MongoDB Connected'))
    .catch(err => console.log(err));
```

---

# 🟠 6. Create Model (MongoDB)

**Question:** How to create and use a model?

```js
const mongoose = require('mongoose');

const UserSchema = new mongoose.Schema({
    name: String,
    email: String
});

const User = mongoose.model('User', UserSchema);

// Usage
const user = new User({ name: 'John', email: 'john@test.com' });
user.save();
```


### 1. DB Connection

```js
// db.js
const mysql = require('mysql2');

const db = mysql.createConnection({
    host: 'localhost',
    user: 'root',
    password: '',
    database: 'test'
});

module.exports = db;
```

---

## 2. Create Model

👉 (Like Laravel Model concept — reusable functions)

```js
// models/User.js
const db = require('../db');

const User = {

    getAll: (callback) => {
        db.query('SELECT * FROM users', callback);
    },

    getById: (id, callback) => {
        db.query('SELECT * FROM users WHERE id = ?', [id], callback);
    },

    create: (data, callback) => {
        db.query('INSERT INTO users SET ?', data, callback);
    },

    update: (id, data, callback) => {
        db.query('UPDATE users SET ? WHERE id = ?', [data, id], callback);
    },

    delete: (id, callback) => {
        db.query('DELETE FROM users WHERE id = ?', [id], callback);
    }

};

module.exports = User;
```

---

## 3. Use Model in Controller / Route

```js
const express = require('express');
const app = express();
const User = require('./models/User');

app.use(express.json());

// Get all users
app.get('/users', (req, res) => {
    User.getAll((err, result) => {
        if (err) return res.status(500).send(err);
        res.json(result);
    });
});

// Create user
app.post('/users', (req, res) => {
    User.create(req.body, (err, result) => {
        if (err) return res.status(500).send(err);
        res.send('User created');
    });
});
```

---

# 🔥 Modern Version (Promise-Based – Recommended)

👉 Interviewers LOVE this version

```js
// db.js
const mysql = require('mysql2/promise');

const db = mysql.createPool({
    host: 'localhost',
    user: 'root',
    password: '',
    database: 'test'
});

module.exports = db;
```

---

## Model (Async/Await)

```js
// models/User.js
const db = require('../db');

const User = {

    getAll: async () => {
        const [rows] = await db.query('SELECT * FROM users');
        return rows;
    },

    getById: async (id) => {
        const [rows] = await db.query('SELECT * FROM users WHERE id = ?', [id]);
        return rows[0];
    },

    create: async (data) => {
        const [result] = await db.query('INSERT INTO users SET ?', data);
        return result;
    }

};

module.exports = User;
```

---

## Usage

```js
app.get('/users', async (req, res) => {
    try {
        const users = await User.getAll();
        res.json(users);
    } catch (err) {
        res.status(500).send(err);
    }
});
```


---

# 🟢 7. Promise Example

**Question:** How to create and use a Promise?

```js
const myPromise = new Promise((resolve, reject) => {
    let success = true;

    if (success) resolve('Success');
    else reject('Error');
});

myPromise
    .then(res => console.log(res))
    .catch(err => console.log(err));
```

---

# 🟡 8. Async/Await

**Question:** How to use async/await?

```js
const fetchData = async () => {
    try {
        const result = await myPromise;
        console.log(result);
    } catch (err) {
        console.log(err);
    }
};

fetchData();
```

---

# 🔵 9. WebSocket Example

**Question:** How to create a simple WebSocket server?

```js
const WebSocket = require('ws');

const wss = new WebSocket.Server({ port: 3000 });

wss.on('connection', ws => {
    ws.on('message', message => {
        console.log('Received:', message);
        ws.send('Hello Client');
    });
});
```

---

# 🟣 10. Simple CRUD (Express + Memory)

**Question:** Build simple CRUD API.

```js
let users = [];

app.post('/users', (req, res) => {
    users.push(req.body);
    res.send('User added');
});

app.get('/users', (req, res) => {
    res.json(users);
});

app.put('/users/:id', (req, res) => {
    users[req.params.id] = req.body;
    res.send('Updated');
});

app.delete('/users/:id', (req, res) => {
    users.splice(req.params.id, 1);
    res.send('Deleted');
});
```

---

# 🔴 11. Add Header in Response

**Question:** How to set headers in response?

```js
app.get('/', (req, res) => {
    res.set('X-Custom-Header', 'MyValue');
    res.send('Header Set');
});
```

---

# 🟠 12. Parse JSON Body (Important)

```js
app.use(express.json());
```

---

# 🟢 13. Error Handling Middleware

```js
app.use((err, req, res, next) => {
    res.status(500).json({ error: err.message });
});
```

---

# 🟡 14. Route Parameters

```js
app.get('/user/:id', (req, res) => {
    res.send(req.params.id);
});
```



# 🟢 1. Custom Event Emitter

**Question:** Create your own event emitter.

```js id="evt123"
class MyEmitter {
    constructor() {
        this.events = {};
    }

    on(event, cb) {
        if (!this.events[event]) this.events[event] = [];
        this.events[event].push(cb);
    }

    emit(event, data) {
        if (this.events[event]) {
            this.events[event].forEach(cb => cb(data));
        }
    }
}

// Usage
const emitter = new MyEmitter();
emitter.on('msg', data => console.log(data));
emitter.emit('msg', 'Hello');
```

---

# 🟡 2. Debounce Function

**Question:** Implement debounce.

```js id="deb456"
function debounce(fn, delay) {
    let timer;
    return function (...args) {
        clearTimeout(timer);
        timer = setTimeout(() => fn.apply(this, args), delay);
    };
}
```

---

# 🔵 3. Throttle Function

**Question:** Implement throttle.

```js id="thr789"
function throttle(fn, limit) {
    let flag = true;
    return function (...args) {
        if (!flag) return;
        flag = false;
        fn.apply(this, args);
        setTimeout(() => flag = true, limit);
    };
}
```

---

# 🟣 4. Rate Limiter Middleware (Important 🔥)

**Question:** Limit API requests.

```js id="rat111"
const rateLimit = {};

const limiter = (req, res, next) => {
    const ip = req.ip;
    const now = Date.now();

    if (!rateLimit[ip]) rateLimit[ip] = [];

    rateLimit[ip] = rateLimit[ip].filter(time => now - time < 60000);

    if (rateLimit[ip].length >= 5) {
        return res.status(429).send('Too many requests');
    }

    rateLimit[ip].push(now);
    next();
};

app.use(limiter);
```

---

# 🔴 5. LRU Cache (Important for interviews)

**Question:** Implement LRU Cache.

```js id="lru222"
class LRU {
    constructor(limit) {
        this.cache = new Map();
        this.limit = limit;
    }

    get(key) {
        if (!this.cache.has(key)) return null;
        const val = this.cache.get(key);
        this.cache.delete(key);
        this.cache.set(key, val);
        return val;
    }

    set(key, val) {
        if (this.cache.has(key)) {
            this.cache.delete(key);
        } else if (this.cache.size === this.limit) {
            const firstKey = this.cache.keys().next().value;
            this.cache.delete(firstKey);
        }
        this.cache.set(key, val);
    }
}
```

---

# 🟠 6. Retry API Call

**Question:** Retry API 3 times if failed.

```js id="retry333"
async function retry(fn, attempts = 3) {
    for (let i = 0; i < attempts; i++) {
        try {
            return await fn();
        } catch (err) {
            if (i === attempts - 1) throw err;
        }
    }
}
```



---

# 🟢 7. Parallel API Calls

**Question:** Run APIs in parallel.

```js id="par444"
const fetchAll = async () => {
    const results = await Promise.all([
        fetch('url1'),
        fetch('url2')
    ]);
    return results;
};
```

---

# 🟡 8. Sequential Execution

```js id="seq555"
async function runSequential(tasks) {
    for (let task of tasks) {
        await task();
    }
}
```

---

# 🔵 9. File Upload (Express)

```js id="upl666"
const multer = require('multer');

const upload = multer({ dest: 'uploads/' });

app.post('/upload', upload.single('file'), (req, res) => {
    res.send('File uploaded');
});
```

---

# 🟣 10. Stream File (Large File Handling)

```js id="str777"
const fs = require('fs');

app.get('/file', (req, res) => {
    const stream = fs.createReadStream('bigfile.txt');
    stream.pipe(res);
});
```

---

# 🔴 11. Simple Logger

```js id="log888"
const fs = require('fs');

function log(message) {
    fs.appendFileSync('app.log', message + '\n');
}
```

---

# 🟠 12. Environment Variables

```js id="env999"
require('dotenv').config();

console.log(process.env.PORT);
```

---

# 🟢 13. JWT Authentication

```js id="jwt101"
const jwt = require('jsonwebtoken');

const token = jwt.sign({ id: 1 }, 'secret', { expiresIn: '1h' });

jwt.verify(token, 'secret', (err, decoded) => {
    console.log(decoded);
});
```

---

# 🟡 14. Password Hashing

```js id="hash202"
const bcrypt = require('bcrypt');

const hash = await bcrypt.hash('password', 10);
const match = await bcrypt.compare('password', hash);
```

---

# 🔵 15. Simple Queue System

```js id="que303"
class Queue {
    constructor() {
        this.tasks = [];
    }

    add(task) {
        this.tasks.push(task);
    }

    async run() {
        while (this.tasks.length) {
            const task = this.tasks.shift();
            await task();
        }
    }
}
```

---

# 🟣 16. WebSocket Chat Broadcast

```js id="ws404"
wss.on('connection', ws => {
    ws.on('message', msg => {
        wss.clients.forEach(client => {
            if (client.readyState === 1) {
                client.send(msg.toString());
            }
        });
    });
});
```

---

# 🔥 17. API Caching

```js id="cache505"
const cache = {};

app.get('/data', async (req, res) => {
    if (cache['data']) return res.json(cache['data']);

    const data = { msg: 'Hello' };
    cache['data'] = data;

    res.json(data);
});
```

---

# 🟠 18. Validate Request

```js id="val606"
app.post('/user', (req, res) => {
    if (!req.body.name) {
        return res.status(400).send('Name required');
    }
    res.send('Valid');
});
```

---

# 🟢 19. Custom Error Throw

```js id="err707"
app.get('/', (req, res, next) => {
    try {
        throw new Error('Something wrong');
    } catch (err) {
        next(err);
    }
});
```

---

# 🟡 20. Pagination Logic

```js id="pag808"
app.get('/users', (req, res) => {
    const page = +req.query.page || 1;
    const limit = 5;

    const start = (page - 1) * limit;
    const end = start + limit;

    res.json(users.slice(start, end));
});
```
