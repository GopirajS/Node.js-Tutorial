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

* [When should you use `"type": "module"`?](#when_should_you_use_type_module)

* [What are named exports vs default exports?](#what_are_named_exports_vs_default_exports)

---

## **NPM & Package Management**


* [What is `package.json`?](#what_is_package_json)

* [What is `package-lock.json`?](#what_is_package_lock_json)

* [What are dependencies vs devDependencies?](#what_are_dependencies_vs_devdependencies)

* [What is semantic versioning?](#what_is_semantic_versioning)

* [What is a global package?](#what_is_a_global_package)

* [Combined Explanation — npm vs npx (clear + simple) ?](#what_is_npx_npm)


<h1 style="text-align:center;" >Node.js Basics</h1>

---

<h2 id="what_is_node_js" style="color:green">What is Node.js</h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/916830b3-fb05-4dc0-974c-1d84c9c31cc5" />

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

**1. Many requests come to the Node.js server.**
**2. All requests are placed into the Event Queue.**
**3. The Event Loop keeps checking the Event Queue and decides how to handle each request.**

### 🔹 Non-blocking tasks

(Like reading files, database queries, network operations)
➡️ Sent to **I/O Polling**
➡️ When they finish, the Event Loop picks up the result

### 🔹 Blocking / heavy tasks

(Like CPU-heavy work, encryption, compression)
➡️ Sent to the **Thread Pool**
➡️ The thread pool processes them in the background
➡️ Then returns the result to the Event Loop

**4. The Event Loop continues handling more requests without waiting.**

---

## 🗣️ Super Short Version for Interview

**“Requests go into the Event Queue.
The Event Loop checks them.
Non-blocking tasks go to I/O polling.
Blocking tasks go to the thread pool.
The Event Loop keeps running without waiting.”**

---

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

<h2 id="UNIQVAUE" style="color:green">🟦 What is an ES Module (ESM)?</h2>

An **ES Module** is the **modern, official JavaScript module system** that uses:

* `import`
* `export`

It is the standard used in browsers *and also supported in Node.js*.

Think of it like:

👉 **A clean, modern way to share code between files.**

---

# 🧩 Example of an ES Module

### **math.js**

```js
export function add(a, b) {
  return a + b;
}
```

### **app.js**

```js
import { add } from './math.js';
console.log(add(2, 3)); // 5
```

---

## 🔑 Key Features (Very Simple)

* Uses `import` / `export` (not `require()`)
* Works in browsers and Node.js
* Supports tree shaking (removing unused code)
* Strict mode automatically
* Asynchronous module loading

---

## 📦 How to use ES Modules in Node.js?

You must do **one** of these:

### Option 1: File extension `.mjs`

```js
app.mjs
math.mjs
```

### Option 2: Use `"type": "module"` in **package.json**

```json
{
  "type": "module"
}
```

Then `.js` files become ES Modules.

---

## 🆚 ES Modules vs CommonJS (Easy Table)

| Feature         | ES Module         | CommonJS         |
| --------------- | ----------------- | ---------------- |
| Import          | `import`          | `require()`      |
| Export          | `export`          | `module.exports` |
| Standard?       | Yes (official JS) | No (Node-only)   |
| Browser support | Yes               | No               |

---

### 📝 Summary

**ES Modules = modern JavaScript modules using `import` and `export`**

They are the future standard for both browsers and Node.js.



<span style="color:green;">================================================================ </span>

<h2 id="what_is_the_difference_between_esm_and_commonjs" style="color:green">🟦 ES Modules (ESM) vs 🟧 CommonJS (CJS)</h2>

## 🔑 **1. Syntax Difference**

### **ESM**

* Uses modern JavaScript keywords

```js
import something from './file.js';
export default something;
```

### **CommonJS**

* Uses Node.js-specific functions

```js
const something = require('./file');
module.exports = something;
```

---

## 🧠 **2. When they load**

### **ESM → Static (checked before running)**

* Imports are checked *before* the code runs
* Faster for bundlers
* Allows tree shaking (removing unused code)

### **CommonJS → Dynamic**

* `require()` can run *anytime*
* Can load based on conditions

```js
if (true) {
  const x = require('./x');
}
```

---

## 📝 **3. File Extensions**

### **ESM**

* `.mjs`
* or `.js` when `"type": "module"` in package.json

### **CJS**

* `.js` (default)
* `.cjs` (when `"type": "module"` is used)

---

## 🗂 **4. Module Resolution**

### **ESM**

* Requires full file extensions (`.js`, `.json`)
* Stricter rules

### **CommonJS**

* Can omit extensions
* Tries `.js`, `.json`, `.node` automatically

---

## 🔄 **5. Import/Export Style**

### **ESM (multiple
 exports)**

```js
export function a() {}
export function b() {}
```

### **CJS (exports object)**

```js
module.exports = { a, b };
```

---

## 🌍 **6. Usage**

| Environment | ESM   | CommonJS |
| ----------- | ----- | -------- |
| Browsers    | ✅ Yes | ❌ No     |
| Node.js     | ✅ Yes | ✅ Yes    |

---

## 🧾 **7. Summary (Super Short)**

| Feature            | ESM      | CommonJS         |
| ------------------ | -------- | ---------------- |
| Import             | `import` | `require()`      |
| Export             | `export` | `module.exports` |
| Standard JS        | ✅ Yes    | ❌ No             |
| Browser support    | Yes      | No               |
| Loading            | Static   | Dynamic          |
| Tree-shaking       | Yes      | No               |
| Default in Node.js | No       | Yes              |


<span style="color:green;">================================================================ </span>

<h2 id="UNIQVAUE" style="color:green"> 🟦 When should you use `"type": "module"`</h2>

You should add this to **package.json**:

```json
{
  "type": "module"
}
```

**ONLY when you want your Node.js project to use ES Modules (ESM)**
→ meaning you want to use **`import`** and **`export`** instead of `require()`.

---

## ✅ Use `"type": "module"` when:

### 1️⃣ **You prefer modern syntax**

```js
import fs from "fs";
export function add() {}
```

### 2️⃣ **Your project is frontend + backend with same ESM style**

(Browser uses ESM → your Node code also uses ESM)

### 3️⃣ **You want tree-shaking or bundling benefits**

Tools like Vite, Webpack, Rollup work better with ESM.

### 4️⃣ **You are writing modern, future-proof JavaScript**

---

## ❌ Don’t use `"type": "module"` when:

### 1️⃣ You use many Node packages still based on CommonJS

(some older packages don’t support ESM well)

### 2️⃣ You prefer `require()`

```js
const fs = require("fs");
```

### 3️⃣ You want faster and simpler development in Node.js

(CommonJS is easier for quick scripts)

---

### 🎯 Simple Rule to Remember

### 👉 If you want to write **modern JS** → use `"type": "module"`

### 👉 If you want **classic Node.js style** → don’t use it

---

### 📝 Quick Comparison

| Needs `type: module`? | ESM                 | CJS         |
| --------------------- | ------------------- | ----------- |
| Keyword               | `import` / `export` | `require()` |
| Browser-compatible    | Yes                 | No          |
| package.json needed?  | Yes                 | No          |


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