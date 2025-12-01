<a href="#top" id="backToTop" style="
    position: fixed;
    bottom: 20px;
    right: 20px;
    background: #007bff;
    color: white;
    padding: 8px 12px;
    border-radius: 6px;
    text-decoration: none;
    font-size: 14px;
">⬆ Top</a>

<script>
document.querySelector('#backToTop').addEventListener('click', function(e) {
    e.preventDefault();
    document.querySelector('#top').scrollIntoView({
        behavior: 'smooth'
    });
});
</script>



# ✅ **Node.js Topic-Wise Interview & Learning Questions**

---

## **Node.js Basics**

- [What is Node.js?](#what_is_node_js)

- [What is the V8 engine?](#what_is_the_v8_engine)

- [What is non-blocking I/O?](#what_is_non_blocking_input_output)

- [What is the difference between Node.js and JavaScript (browser)?](#what_is_the_difference_between_node_js_and_javascript_browser)

- [What is the role of libuv in Node.js?](#what_is_the_role_of_libuv_in_node_js)

- [What is event-driven architecture in Node.js?](#what_is_event_driven_architecture)

- [What is thread pool in Node.js?](#what_is_thread_pool)

- [What is I/O Polling Techniques in Node.js?](#what_is_Polling)


## **ES Modules (ESM) in Node.js**


* [What is an ES module?](#what_is_an_es_module)

* [What is the difference between ESM and CommonJS?](#what_is_the_difference_between_esm_and_commonjs)

* [What are named exports vs default exports?](#what_are_named_exports_vs_default_exports)

---

## **NPM & Package Management**


* [What is `package.json`?](#what_is_package_json)

* [What is `package-lock.json`?](#what_is_package_lock_json)

* [What are dependencies vs devDependencies?](#what_are_dependencies_vs_devdependencies)

* [What is semantic versioning?](#what_is_semantic_versioning)

* [What is a global package?](#what_is_a_global_package)

* [Combined Explanation — npm vs npx (clear + simple) ?](#what_is_npx_npm)


---

## **Node.js Core Modules**


* [What is the `fs` module?](#what_is_the_fs_module)

* [What is the difference between sync and async file methods?](#what_is_the_difference_between_sync_and_async_file_methods)

* [What is the `path` module used for?](#what_is_the_path_module_used_for)

* [What is the `http` module used for?](#what_is_the_http_module_used_for)

* [What is the `events` module?](#what_is_the_events_module)

* [What are event emitters?](#what_are_event_emitters)

* [What is the `crypto` module?](#what_is_the_crypto_module_used_for)

---


## **Asynchronous Programming**


* [What are callbacks?](#what_are_callbacks)\

* [What is an error-first callback?](#what_is_an_error_first_callback)

* [What are microtasks vs macrotasks?](#what_are_microtasks_vs_macrotasks)

* [What are Promises?](#what_are_promises)

* [What are Promises Chain?](#what_are_promises)

* [What is async/await?](#what_is_async_await)

---

---

<h1 style="text-align:center;" >Node.js Basics</h1>

---

<h2 id="what_is_node_js" style="color:green">What is Node.js</h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/2c33f160-decb-4ac0-a9e5-f3d10ce9c16c" />

**Node.js is a way to run JavaScript outside the browser.**
Normally, JavaScript runs only inside web browsers (like Chrome, Firefox).
Node.js allows you to run JavaScript directly on your computer or server.

---

### **A very simple way to remember:**

* **Browser = JavaScript for webpages**
* **Node.js = JavaScript for backend/server**

---

### **Why is Node.js popular?**

* It is **fast** (uses Google Chrome’s V8 engine).
* It can handle many requests at the same time.
* Great for **APIs**, **real-time apps** (chat, notifications), and **servers**.

---

<span style="color:green;">================================================================ </span>

<h2 id="what_is_the_v8_engine" style="color:green">What is the V8 engine?</h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/62f95755-0cf0-416e-90e3-b55cb3048aa5" />

**The V8 engine is a program made by Google that runs JavaScript very fast.**

It is used in:

* **Google Chrome browser**
* **Node.js**

---

### **Why is it important?**

* It converts JavaScript into **machine code** (code the computer understands).
* This makes JavaScript run **very fast and efficiently**.

---

### **In short:**

**V8 = Fast JavaScript engine created by Google.**


<span style="color:green;">================================================================ </span>

<h2 id="what_is_non_blocking_input_output" style="color:green">⚡ What is Non-Blocking I/O in Node.js?</h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/fd7c9572-37f3-4ace-b5cc-95ea6626f8c6" />

**Non-blocking I/O** means that **Node.js does not wait** for slow operations (like reading a file, querying a database, or making an API call) to finish.

Instead, it:

1. **Starts the I/O operation**
2. **Immediately moves on** to the next line of code
3. When the operation completes, Node.js uses

   * a **callback**,
   * **promise**, or
   * **async/await**
     to return the result.

---

## 🧠 Why is it important?

* It prevents the main thread from **getting stuck** waiting.
* Helps Node.js handle **thousands of requests at the same time**.
* This makes Node.js **fast, scalable, and efficient**, especially for I/O-heavy apps.

---

## 🔌 Example (Simple)

```js
fs.readFile("file.txt", "utf8", (err, data) => {
  console.log(data);
});
console.log("I continue running...");
```

Here:

* File reading happens in the background 🧵
* The main thread continues immediately 🚀

---

## 🗣️ **Short Interview Answer**

**“Non-blocking I/O means Node.js performs input/output operations asynchronously. It doesn't wait for the operation to finish; instead, it uses callbacks, promises, or async/await to handle results. This keeps the main thread free and allows Node.js to handle many requests efficiently.”**


<span style="color:green;">================================================================ </span>


<h2 id="what_is_the_difference_between_node_js_and_javascript_browser" style="color:green"> 🔍 Difference Between Node.js and JavaScript (Browser) </h2>

### 🌐 1. **Environment**

* **Browser JavaScript:** Runs inside a web browser (Chrome, Firefox, Safari).
* **Node.js:** Runs **outside the browser** on the server using the **V8 engine**.

---

### 📁 2. **APIs Available**

* **Browser JS:** Has **DOM**, `window`, `document`, `localStorage`, `fetch` (browser version).
* **Node.js:** Has **file system**, **network**, **process**, **streams**, and other backend APIs.

---

### 🧵 3. **Threading Model**

* **Browser JS:** Single-threaded (main thread + Web Workers).
* **Node.js:** Single-threaded for JS but uses **event loop + thread pool** for async tasks.

---

### 📦 4. **Modules**

* **Browser JS:** Uses ES Modules (`import/export`).
* **Node.js:** Supports **CommonJS (`require`)** and **ES Modules**.

---

### 🚀 5. **Use Cases**

* **Browser JS:** User interfaces, web pages, DOM manipulation.
* **Node.js:** Backend development, APIs, real-time apps, CLI tools.

---

## 🗣️ **Short Interview Answer**

**“JavaScript is a programming language, but Node.js is a runtime environment that allows JavaScript to run outside the browser. Browsers provide DOM APIs, while Node.js provides server-side APIs like file system and networking. In short, browser JS is for frontend; Node.js is for backend.”**


<span style="color:green;">================================================================ </span>

<h2 id="what_is_the_role_of_libuv_in_node_js" style="color:green"> 🔧 What is the Role of "libuv" in Node.js? </h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/65384c4f-0339-40d3-a6ae-299c32f3706d" />

**libuv** is a C library inside Node.js that makes **asynchronous, non-blocking I/O** possible.

It is the **engine behind Node.js’s event loop and thread pool**.

---

## 🧠 libuv Handles 4 Main Things

### ⏱️ 1. **Event Loop**

* Manages how Node.js runs asynchronous tasks
* Decides *when* callbacks, promises, and async functions execute

### 🧵 2. **Thread Pool**

* Provides background threads for slow tasks like:

  * File system operations
  * DNS lookups
  * Crypto tasks
  * Compression
* Offloads work so the main thread never gets blocked

### 🌐 3. **Cross-Platform Support**

* Makes Node.js run the same on:

  * Windows
  * Linux
  * macOS
* Handles OS-level differences internally

### 🖧 4. **Async I/O Operations**

* Manages networking (TCP/UDP)
* Manages timers (setTimeout / setInterval)
* Manages pipes, streams, handles, file I/O

---

## 🗣️ **Short Interview Answer**

**“libuv is the C library that provides Node.js with an event loop and a thread pool. It enables non-blocking I/O by handling asynchronous operations like file system tasks, network requests, timers, and DNS in the background. This allows Node.js to remain fast and efficient even with a single-threaded JavaScript runtime.”**


<span style="color:green;">================================================================ </span>

<h2 id="what_is_event_driven_architecture" style="color:green"> ⚡ What is Event-Driven Architecture in Node.js? </h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/973550cb-a223-4ce9-a608-a06c6ae23991" />


**Event-Driven Architecture (EDA)** is a programming style where your application **reacts to events** instead of following a strict top-to-bottom flow.

Node.js is built heavily on this pattern.

---

### 🔔 How It Works (Simple Explanation)

1. **An event happens**
   (e.g., user clicks, file finishes reading, data received)

2. **Node emits the event**

3. **Your code listens for the event**
   and runs the callback function.

This makes Node.js **fast**, **non-blocking**, and great for handling many requests.

---

### 🧱 Example Flow

* You start reading a file → Node emits a **"start"** event
* File finishes → Node emits a **"done"** event
* If an error occurs → Node emits an **"error"** event

You write listeners for these events.

---

### 🧪 Small Example

```js
const EventEmitter = require('events');
const events = new EventEmitter();

events.on('order', () => {
  console.log("Order received!");
});

events.emit('order');
```

---

### 🎯 Why Node.js Uses Event-Driven Architecture?

* ⚡ Handles many requests at once
* 🧵 No need for multi-threading
* 📬 Everything is queue/event based
* 🚀 Perfect for real-time apps (chat, live updates)

---

### 🛠 Real-Life Examples in Node.js

| Example      | Event Trigger   |
| ------------ | --------------- |
| HTTP server  | "request"       |
| Streams      | "data", "end"   |
| File reading | "open", "close" |
| Timers       | "timeout"       |
| WebSockets   | "message"       |

---

### 🧠 In One Line (Very Simple)

**Node.js works like: Something happens → Node emits an event → Your code reacts.**



<span style="color:green;">================================================================ </span>

<h2 id="what_is_thread_pool" style="color:green"> 🧵 What is Thread Pool in Node.js? </h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/2202fddc-cecd-4c5f-9613-2a256aafd92c" />

The **Thread Pool** in Node.js is a group of **background worker threads** that handle **heavy or blocking tasks** so the main thread (event loop) stays free.

---

## ✅ What It Does

When Node.js gets a **slow or CPU-heavy task**, like:

* File system operations
* Compression
* Encryption / hashing
* DNS lookup

➡️ It sends that work to the **Thread Pool** instead of blocking the main thread.

---

## 🔧 Who Provides It?

The Thread Pool is provided by **libuv** (a C library inside Node.js).

Default size: **4 threads**

---

## 🗣️ Simple Interview Answer

**“Thread Pool is a group of background threads in Node.js that handle heavy tasks so the main thread doesn’t get blocked.”**
**“Thread Pool = background workers for heavy tasks.”**


<span style="color:green;">================================================================ </span>

<h2 id="what_is_Polling" style="color:green"> 🔍 I/O Polling Techniques in Node.js </h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/1b543125-c044-44a7-bbf8-5a71f76d8987" />

**I/O Polling** is how Node.js **checks the status** of non-blocking tasks
(like file read, DB query, network request).

Node.js asks the system again and again:
👉 “Is the task finished?”
When finished, the event loop runs the callback.

---

# 🧪 **Polling Types (Simple Explanation)**

These are **application-level polling techniques** (used in web apps), not Node.js internals —
but interviewers often ask them together.

## 🕒 **1. Long Polling (Simple)**

Client sends a request →
Server **waits** until new data is available →
Then responds.

If no new data, server holds the request for some time.

**Pros:** Better than short polling
**Cons:** Still creates repeated connections

---

## 🔗 **2. WebSocket (Simple)**

A **continuous, two-way connection** between client and server.

Both sides can send data any time without repeated requests.

**Pros:** Fast, real-time
**Cons:** Slightly more complex to set up

---

# 🗣️ **Super Simple Interview Answer**

**“I/O Polling in Node.js means checking when non-blocking tasks are finished.
Short polling means checking repeatedly.
Long polling means waiting until data is available.
WebSocket creates a constant real-time connection.”**

**“I/O Polling = checking the status of non-blocking I/O tasks.”**


<span style="color:green;">================================================================ </span>

<h1 style="text-align:center;">ES Modules (ESM) in Node.js</h1>

<h2 id="what_is_an_es_module" style="color:green">📦 What Is an ES Module (ESM)?</h2>

![Image](https://github.com/user-attachments/assets/7af28ebf-07e3-4527-8213-b17d0b5938c2)

An **ES Module (ESM)** is the modern JavaScript module system introduced in **ES6 (ECMAScript 2015)**.
It is the official, standard way to import and export code in JavaScript.

Node.js supports ESM using the `.mjs` extension **or** `"type": "module"` in `package.json`.

---

### 🧩 Key Features

* Uses `import` and `export` keywords
* Supports static analysis (better optimization)
* Works in both **browsers** and **Node.js**
* More modern and standardized than CommonJS

---

### 🧪 Example

**export.js**

```js
export const name = "John";
export function greet() {
  console.log("Hello!");
}
```

**import.js**

```js
import { name, greet } from "./export.js";

greet();
```

---

### 🧠 Simple Definition

**ES Modules are the modern JavaScript module system using `import` and `export`. They replace older CommonJS (`require`, `module.exports`).**


<span style="color:green;">================================================================ </span>

<h2 id="what_is_the_difference_between_esm_and_commonjs" style="color:green">🔀 What Is the Difference Between ESM and CommonJS? </h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/250c7bf6-1042-4304-ba34-ffd5629259d7" />

### 📦 **1. Syntax**

**CommonJS (CJS)**

```js
const fs = require("fs");
module.exports = something;
```

**ESM**

```js
import fs from "fs";
export default something;
```

---

### ⚙️ **2. Loading Type**

* **CJS:** Loaded **synchronously**
* **ESM:** Loaded **asynchronously**

---

### 🌍 **3. Where They're Used**

* **CJS:** Node.js originally (older system)
* **ESM:** Modern JavaScript (browser + Node.js)

---

### 🔧 **4. Filename Requirements**

* **CJS:** `.js` (default)
* **ESM:** `.mjs` or `"type": "module"` in `package.json`

---

### 🔁 **5. Exports**

* **CJS:** Only one export object

  ```js
  module.exports = { a, b }
  ```

* **ESM:** Named + default exports

  ```js
  export const a = 1;
  export default b;
  ```

---

### 🧠 **6. Top-Level await**

* **CJS:** ❌ Not supported
* **ESM:** ✅ Supported

---

### ⚡ **7. Performance**

* **CJS:** Faster for small modules
* **ESM:** Better optimization by engines

---

### 🧠 Simple Summary

* **CommonJS = require + module.exports (old system)**
* **ESM = import + export (modern standard)**

Node.js supports **both**, but ESM is the **future**.

<span style="color:green;">================================================================ </span>

<h2 id="what_are_named_exports_vs_default_exports" style="color:green">What are named exports vs default exports?</h2>

### 🔹 Named Exports

Export **multiple items by name**.

Example:

```js
export const add = (a, b) => a + b;
export const subtract = (a, b) => a - b;
```

Import:

```js
import { add, subtract } from './math.js';
```

🔑 **Key Points**

* Can export **many things**
* Import names **must match exactly**

---

### 🔸 Default Export

Export **one main value** from a file.

Example:

```js
export default function add(a, b) {
  return a + b;
}
```

Import:

```js
import add from './math.js';
```

🔑 **Key Points**

* Only **one default export** per file
* Import name can be **anything**

---

### ✅ Quick Summary (Icons)

* 🔹 **Named exports** → many exports, import by exact name
* 🔸 **Default export** → one main export, name is flexible


<span style="color:green;">================================================================ </span>

<h1 style="text-align:center;">NPM & Package Management</h1>

<h2 id="what_is_package_json" style="color:green">📦 What is `package.json`?</h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/32074b23-f7de-455b-bef4-cd144e693bf4" />

`package.json` is the **main configuration file** for a Node.js project.
It tells Node.js and npm **important info** about your project.

### 📘 What it contains

* 📛 **Project name & version**
* 📚 **List of dependencies** (packages your project needs)
* ⚙️ **Scripts** (commands like start, build, test)
* 🧩 **Metadata** (author, license, description)
* 🔧 **Settings** (like `"type": "module"`)

### 🧠 Simple idea

👉 `package.json` is the **brain of your Node project**—it keeps track of everything your project uses and needs.



<span style="color:green;">================================================================ </span>

<h2 id="what_is_package_lock_json" style="color:green">🔒 What is `package-lock.json`?</h2>

`package-lock.json` is a file that **locks the exact versions** of every package (and their sub-packages) installed in your project.

### 📘 What it does

* Ensures **everyone installs the same versions**
* Speeds up installation
* Records the full dependency tree
* Prevents unexpected updates that might break your app

### 🧠 Simple idea

👉 `package-lock.json` makes your project’s dependencies **stable and consistent**, no matter who installs it or when.


<span style="color:green;">================================================================ </span>

<h2 id="what_are_dependencies_vs_devdependencies" style="color:green">📦 Dependencies vs ⚙️ DevDependencies</h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/54ce5787-892a-44aa-a506-0605e6c707e7" />

### 📦 Dependencies (`dependencies`)

These are packages your project **needs to run** in production.

Example:

* Express
* Mongoose
* Axios

Installed via:

```bash
npm install express
```

These packages are required when your app is actually running.

---

### ⚙️ DevDependencies (`devDependencies`)

These are packages used **only during development**, not in production.

Example:

* Nodemon
* ESLint
* Jest (testing)
* Webpack

Installed via:

```bash
npm install --save-dev nodemon
```

They help you build, test, or develop the project but are **not needed by users**.

---

### 🧠 Simple idea

👉 **Dependencies = needed to run the app**
👉 **DevDependencies = needed to build or develop the app, not to run it**


<span style="color:green;">================================================================ </span>

<h2 id="what_is_semantic_versioning" style="color:green">What is semantic versioning?</h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/16878532-d9e0-4ace-a9de-27b460dc4548" />

### 🔢 What is Semantic Versioning?

Semantic Versioning (SemVer) is a system for writing version numbers in the format:

### **📌 MAJOR.MINOR.PATCH**

Example:

```
2.5.3
```

### 🧩 What each number means

* **🔴 MAJOR** — Breaking changes
  (Old code might stop working)

* **🟡 MINOR** — New features added
  (No breaking changes)

* **🟢 PATCH** — Bug fixes
  (No new features, no breaking changes)



<span style="color:green;">================================================================ </span>

<h2 id="what_is_a_global_package" style="color:green">🌍 What is a Global Package?</h2>

A **global package** is an npm package that you install **system-wide**, not inside a single project.

Installed with:

```bash
npm install -g packageName
```

### 📌 What it means

* You can use it **from anywhere** in your terminal
* It works like a **system command**

### 🛠 Examples of global packages

* `nodemon`
* `npm` (itself)
* `pm2`
* `eslint` (sometimes)

### 🧠 Simple idea

👉 A global package is like a **tool installed on your whole computer**, not just one project.


<span style="color:green;">================================================================ </span>

<h2 id="what_is_npx_npm" style="color:green">⚡ Combined Explanation — npm vs npx (clear + simple)</h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/43b49ee4-b18c-4e0e-8e7f-557a305564bd" />

### 📦 **npm (Node Package Manager)**

`npm` is used to **install, manage, or remove** packages in your project.

What it does:

* Installs packages **locally** (`node_modules`)
* Installs packages **globally** (with `-g`)
* Updates or removes packages

Examples:

```bash
npm install express        # install locally
npm install -g nodemon     # install globally
npm uninstall lodash       # remove package
```

🧠 **Think:**
👉 **npm = installs packages** (locally or globally)

---

### ⚡ **npx (Node Package Execute)**

`npx` is used to **run packages without installing them globally**.

What it does:

* Runs a local package if it already exists
* If not installed, it downloads it **temporarily**, runs it, then deletes it
* Perfect for one-time tools

Examples:

```bash
npx create-react-app myApp
npx nodemon app.js
```

🧠 **Think:**
👉 **npx = runs packages instantly (no install needed)**

---

### ✅ Final Simple Difference

* **npm** → installs packages
* **npx** → runs packages (without installing them globally)

Let me know if you want examples of when to use each!



<span style="color:green;">================================================================ </span>

<h1 style="text-align:center;"> Node.js Core Modules</h1>

<h2 id="what_is_the_fs_module" style="color:green">📁 What is the `fs` Module?</h2>

The `fs` (File System) module in Node.js allows you to **work with files and folders** on your computer.

### 📌 What you can do with `fs`

* 📄 Read files
* ✍️ Write files
* 📂 Create folders
* 🗑 Delete files
* 🔄 Update or rename files
* 👀 Watch file changes

### 🛠 Example

```js
const fs = require('fs');

fs.readFile('test.txt', 'utf8', (err, data) => {
  console.log(data);
});
```

### 🧠 Simple idea

👉 `fs` lets Node.js **interact with your system’s files** just like a file manager.



<span style="color:green;">================================================================ </span>

<h2 id="what_is_the_difference_between_sync_and_async_file_methods" style="color:green">🔄 Difference Between Sync and Async File Methods</h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/2ce4228c-e602-435d-868e-4c6dd8b32f5c" />

### ⚡ Async (Asynchronous)

Async methods **do not block** the program.
Node keeps running other code while the file operation happens in the background.

Example:

```js
fs.readFile('a.txt', 'utf8', (err, data) => {
  console.log(data);
});
console.log("I run immediately!");
```

🧠 **Idea:**
👉 Fast, non-blocking, best for servers.

---

### ⏸ Sync (Synchronous)

Sync methods **block** the program until the operation finishes.
Nothing else can run during that time.

Example:

```js
const data = fs.readFileSync('a.txt', 'utf8');
console.log(data);
console.log("I run after file is done!");
```

🧠 **Idea:**
👉 Slower, blocking, good for small scripts or startup code.

---

### ✅ Simple Summary

* **Async = non-blocking, recommended for real apps**
* **Sync = blocking, avoid in servers**


<span style="color:green;">================================================================ </span>

<h2 id="what_is_the_path_module_used_for" style="color:green">📍 What is the `path` Module Used For?</h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/dc564833-7e2e-4b7e-8836-7ad14a6260d0" />

The `path` module helps you **work with file and folder paths** in a safe and consistent way.

### 📌 What it does

* Joins paths
* Resolves absolute paths
* Gets file extensions
* Normalizes messy paths
* Extracts filenames or directory names

### 🛠 Example

```js
const path = require('path');

const fullPath = path.join('folder', 'subfolder', 'file.txt');
console.log(fullPath);
```

### 🧠 Simple idea

👉 The `path` module helps Node.js handle **file paths correctly on all operating systems** (Windows, Mac, Linux).


<span style="color:green;">================================================================ </span>

<h2 id="what_is_the_http_module_used_for" style="color:green">What is the `http` module used for?</h2>

The **`http` module** in Node.js is used to **create and manage HTTP servers and clients**. It provides the core functionality required to build web servers without needing any external libraries.

---

## ✅ **What the `http` module is used for**

### **1. Creating HTTP Servers**

It allows you to create a web server that listens for requests and sends responses.

```js
const http = require('http');

const server = http.createServer((req, res) => {
  res.write('Hello World');
  res.end();
});

server.listen(3000, () => {
  console.log('Server running on port 3000');
});
```

---

### **2. Handling HTTP Requests**

You can access:

* `req.url` → request URL
* `req.method` → GET, POST, etc.
* `req.headers` → HTTP headers

---

### **3. Sending HTTP Responses**

Use methods like:

* `res.writeHead(statusCode, headers)`
* `res.write()`
* `res.end()`

Example:

```js
res.writeHead(200, { "Content-Type": "application/json" });
res.end(JSON.stringify({ message: "OK" }));
```

---

### **4. Creating HTTP Clients**

You can also make outgoing HTTP requests using `http.request()` or `http.get()`.

Example:

```js
const http = require('http');

http.get('http://example.com', (res) => {
  let data = '';

  res.on('data', chunk => data += chunk);
  res.on('end', () => console.log(data));
});
```

---

## ✅ **When to use `http` module**

Use it when:

* You want a lightweight web server without frameworks.
* You need low-level control over the request/response process.
* You're building your own framework or a customized microservice.

---

## ❗ When NOT to use it

For most real-world apps, use frameworks like:

* **Express.js**
* **Fastify**
* **NestJS**

They simplify routing, middleware, body parsing, and more.

<span style="color:green;">================================================================ </span>

<h2 id="what_is_the_events_module" style="color:green">What is the `events` module?</h2>

The **`events` module** in Node.js provides the foundation for **event-driven programming**. It lets you create, listen for, and handle custom events in your application.

---

## ✅ What the `events` module is

It is a **built-in Node.js module** that defines the `EventEmitter` class.
This class lets objects **emit events** and **register listeners** for those events.

Node.js itself uses this pattern internally—streams, HTTP servers, file reads, and many core parts of Node are built on top of `EventEmitter`.

---

## ✅ Why the `events` module is useful

### It allows you to:

* Create custom events
* Attach multiple listeners
* Emit events asynchronously or synchronously
* Decouple logic (cleaner architecture)
* Build reactive/observer-style systems

---

### 📌 Basic Example

### Create an event emitter and listen for an event:

```js
const EventEmitter = require('events');

const emitter = new EventEmitter();

// Listener
emitter.on('greet', (name) => {
  console.log(`Hello, ${name}!`);
});

// Emit event
emitter.emit('greet', 'John');
```

**Output:**

```
Hello, John!
```

---

### 📌 Common Methods

| Method                            | Description                |
| --------------------------------- | -------------------------- |
| `on(event, listener)`             | Attach a listener          |
| `once(event, listener)`           | Listener runs only once    |
| `emit(event, ...args)`            | Trigger an event           |
| `removeListener(event, listener)` | Remove a specific listener |
| `removeAllListeners(event)`       | Remove all listeners       |

---

### 📌 Real Use Cases

### ✔ Handling server requests

HTTP server emits `request`, `connection`, `close` events.

### ✔ Streams

Readable/Writable streams use events like `data`, `end`, `error`.

### ✔ Custom app logic

For example, an event after user registration:

```js
emitter.emit('user_registered', userData);
```

---

### 🧠 Summary (in simple words)

The **`events` module** is like Node.js’s built-in **pub/sub system**.
You emit an event → Code listening for that event runs.




<span style="color:green;">================================================================ </span>

<h2 id="what_are_event_emitters" style="color:green">📢 What Are Event Emitters?</h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/3d1fca0b-772b-4dc3-8056-552f9ce3de3c" />

**Event Emitters** are objects in Node.js that can:

1. **Emit (trigger) events**
2. **Listen for events**
3. **Run callback functions when events occur**

They are the core of Node’s **event-driven architecture**.

Node.js provides this through the **`EventEmitter` class** inside the `events` module.

---

### 🔧 How It Works

* You *emit* an event → like saying **“Hey! Something happened!”**
* You *listen* for that event → using `on()` or `once()`
* When the event occurs → the attached function runs

---

### 🧪 Simple Example

```js
const EventEmitter = require('events');

const emitter = new EventEmitter();

emitter.on('greet', () => {
  console.log("Hello!");
});

emitter.emit('greet'); // triggers the event
```

---

### 🔍 Key Methods

| Method                  | Meaning             |
| ----------------------- | ------------------- |
| `on(event, listener)`   | Listen for an event |
| `once(event, listener)` | Listen only once    |
| `emit(event, data)`     | Trigger an event    |
| `removeListener()`      | Remove a listener   |

---

### 🎯 Real Uses of Event Emitters

* HTTP server emits `"request"`
* Streams emit `"data"`, `"end"`
* File system emits `"open"`, `"close"`
* WebSockets emit `"message"`

---

### 🧠 In Simple Words

**Event Emitters let Node.js say: “I’ll call you when something happens.”**


<span style="color:green;">================================================================ </span>

<h2 id="what_is_the_crypto_module_used_for" style="color:green">🔐 What Is the `crypto` Module?</h2>

The **`crypto` module** in Node.js is a **built-in security module** used to perform cryptographic operations such as:

* Hashing
* Encryption & decryption
* Generating random values
* Creating HMACs
* Working with keys & certificates

It helps you securely handle passwords, tokens, signatures, and more.

---

### 🧪 Simple Example (Hashing a Password)

```js
const crypto = require('crypto');

const hash = crypto
  .createHash('sha256')
  .update('hello')
  .digest('hex');

console.log(hash);
```

---

### 🔧 Common Things You Can Do with `crypto`

| Feature           | Use                                             |
| ----------------- | ----------------------------------------------- |
| 🔑 Hashing        | Securely store passwords (SHA256, SHA512, etc.) |
| 🧩 HMAC           | Create keyed signatures                         |
| 🎲 Random values  | Generate tokens, OTPs                           |
| 🔐 Encryption     | Encrypt/decrypt data                            |
| 🧵 Key generation | Create public/private keys                      |

---

### 🧠 Simple Definition

**The `crypto` module provides tools to secure your application using encryption, hashing, and cryptographic functions.**



<span style="color:green;">================================================================ </span>



<span style="color:green;">================================================================ </span>

<h1 style="text-align:center;" >Asynchronous Programming</h1>

<h2 id="what_are_callbacks" style="color:green">What are callbacks?</h2>

### 🔁 What Are Callbacks?

A **callback** is a **function passed as an argument to another function**, and it runs **after an asynchronous task completes**.

It’s how Node.js handles async operations like reading files, making requests, or waiting for timers—*without blocking the program*.

---

### 🧪 Simple Example

```js
function greet(name, callback) {
  console.log("Hello " + name);
  callback(); // run after main task
}

greet("John", () => {
  console.log("Callback finished!");
});
```

---

### 📦 Real Node.js Async Example (fs module)

```js
const fs = require('fs');

fs.readFile("file.txt", "utf8", (err, data) => {
  if (err) return console.error(err);
  console.log(data);
});
```

---

### 🎯 Why Callbacks Are Important

* They let Node.js do **non-blocking** operations
* They run **when the async task is done**
* They keep the server fast, even with many requests

---

### ⚠️ Callback Hell (Common Problem)

Too many nested callbacks:

```js
doA(() => {
  doB(() => {
    doC(() => {
      doD(() => {
        console.log("Too deep!");
      });
    });
  });
});
```

This is why Node.js later introduced **Promises** and **async/await**.

---

### 🧠 Simple Definition

**A callback is a function you give to another function, and it runs later when the async work finishes.**


<span style="color:green;">================================================================ </span>

<h2 id="what_is_an_error_first_callback" style="color:green"> ⚠️ What Is an Error-First Callback? </h2>

![Image](https://github.com/user-attachments/assets/216cb864-dede-4cff-b9ed-020f2c7aa943)


An **error-first callback** is a special style of callback function used in Node.js where:

* The **first argument is always the error** (if any)
* The **second argument is the result**

This pattern helps Node.js easily detect and handle errors in async operations.

---

### 🧪 Example Format

```js
function callback(err, result) {
  if (err) {
    // handle error
  } else {
    // use the result
  }
}
```

---

### 📌 Real Node.js Example (fs.readFile)

```js
const fs = require("fs");

fs.readFile("file.txt", "utf8", (err, data) => {
  if (err) {
    console.error("Something went wrong!");
    return;
  }

  console.log("File content:", data);
});
```

---

### 🎯 Why This Pattern Exists?

* Makes error handling **consistent**
* Easy to detect failure: if `err` is not `null`, something went wrong
* Works perfectly with async operations

---

### 🧠 Simple Definition

**An error-first callback is a callback where the first argument is an error, and the second is the result. If the error exists, you handle it; otherwise, you use the result.**



<span style="color:green;">================================================================ </span>

<h2 id="what_are_microtasks_vs_macrotasks" style="color:green">🕒 What Are Microtasks vs Macrotasks?</h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/a4a016cb-91fe-4d25-98ce-92ebb71d3f8d" />

In Node.js (and browsers), asynchronous work is handled by the **event loop**, which uses two main queues:


### 🧩 **Macrotasks (Task Queue)**

Macrotasks are **big async operations** that run *after the current code finishes*.

**Examples of macrotasks:**

* `setTimeout()`
* `setInterval()`
* `setImmediate()`
* I/O callbacks (fs, http)
* `requestAnimationFrame` (browser)

**Runs later** → slower priority.

---

### ⚡ **Microtasks (Microtask Queue)**

Microtasks are **small, high-priority async tasks** that run **before macrotasks**.

**Examples of microtasks:**

* Promises (`.then`, `.catch`, `.finally`)
* `process.nextTick()` (Node-specific)
* QueueMicrotask

**Runs immediately after current code** → highest priority.

---

### 🎯 Which runs first?

✔ **Microtasks ALWAYS run before macrotasks**
✔ After each macrotask, Node empties the microtask queue

---

### 🧪 Example

```js
console.log("A");

setTimeout(() => console.log("B"), 0);  // macrotask
Promise.resolve().then(() => console.log("C")); // microtask

console.log("D");
```

**Output:**

```
A
D
C  <-- microtask
B  <-- macrotask
```

---

### 🧠 Simple Definition

* **Microtasks = high-priority async tasks (Promises)**
* **Macrotasks = regular async tasks (setTimeout, I/O)**
* **Microtasks run first**


<span style="color:green;">================================================================ </span>

<h2 id="what_are_promises" style="color:green">🤝 What Are Promises?</h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/d5e64e34-c7d6-43a0-9a79-9d4c479255c2" />

A **Promise** in JavaScript is an object that represents the **eventual result of an asynchronous operation**.
It’s a cleaner alternative to callbacks and helps avoid *callback hell*.

A Promise can be in one of three states:

1. **Pending** → still running
2. **Fulfilled** → completed successfully
3. **Rejected** → failed

---

### 🧪 Simple Example

```js
const myPromise = new Promise((resolve, reject) => {
  const success = true;

  if (success) {
    resolve("Done!");
  } else {
    reject("Error!");
  }
});

myPromise
  .then(result => console.log(result))
  .catch(error => console.log(error));
```

---

### 🎯 Why Promises Are Useful?

* Avoids callback nesting
* Easy error handling
* Chain async operations
* Works with `async/await`

---

### 🧠 Simple Definition

**A Promise is a placeholder for a value that you will get in the future (success or failure).**


<span style="color:green;">================================================================ </span>

<h2 id="what_are_promises" style="color:green">🔗 What Is a Promise Chain?</h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/55a26169-70cb-4d51-808a-260c80a74c22" />


A **Promise chain** is when you connect multiple `.then()` calls one after another so each step runs **after the previous Promise finishes**.

It allows you to run async tasks in sequence **without callback hell**.

---

### 🧩 How It Works

Each `.then()` returns a **new Promise**, so you can keep chaining:

```js
doTask1()
  .then(result1 => doTask2(result1))
  .then(result2 => doTask3(result2))
  .then(result3 => console.log("All done!", result3))
  .catch(error => console.log("Error:", error));
```

---

### 🧪 Simple Example

```js
Promise.resolve(1)
  .then(num => num + 1)     // 2
  .then(num => num * 5)     // 10
  .then(num => console.log(num));
```

**Output:**

```
10
```

---

### 🎯 Why Promise Chaining Is Useful?

* Runs async tasks **step-by-step**
* Avoids nested callbacks
* Makes async code **clean and readable**
* Errors propagate automatically to `.catch()`

---

### 🧠 Simple Definition

**Promise chaining means linking multiple `.then()` calls so each one waits for the previous promise to finish.**


<span style="color:green;">================================================================ </span>

<h2 id="what_is_async_await" style="color:green">⏳ What Is async/await?</h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/335e4109-6c67-49b6-ad55-d4964b54a0e9" />

**`async/await`** is modern JavaScript syntax that makes working with Promises look like **simple, synchronous code**—even though it’s still fully asynchronous.

It is built on top of Promises and helps you avoid long `.then()` chains.

---

### 🔧 How It Works

* You mark a function as **`async`**
* Inside it, you use **`await`** to pause the function until a Promise resolves
* The code *looks* synchronous but *runs* asynchronously

---

### 🧪 Simple Example

```js
async function demo() {
  const result = await Promise.resolve("Hello!");
  console.log(result);
}

demo();
```

**Output:**

```
Hello!
```

---

### 📦 Real Example (Fetching Data)

```js
async function getData() {
  try {
    const response = await fetch("https://api.example.com");
    const json = await response.json();
    console.log(json);
  } catch (err) {
    console.error("Error:", err);
  }
}
```

---

### 🎯 Why async/await is great?

* Cleaner and more readable
* Easier error handling using `try...catch`
* No callback hell
* No long Promise chains

---

### 🧠 Simple Definition

**`async/await` lets you write asynchronous code that looks like normal, synchronous code, using Promises behind the scenes.**


<span style="color:green;">================================================================ </span>
