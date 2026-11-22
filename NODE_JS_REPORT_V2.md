
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
    padding: 8px 12px;
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

