<span style="color:green;">================================================================ </span>

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

<h2 id="what_is_the_difference_between_sync_and_async_file_methods" style="color:green">🔄 Difference Between **Sync** and **Async** File Methods</h2>

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

<h2 id="UNIQVAUE" style="color:green">TEXT_CONTENVT</h2>


<span style="color:green;">================================================================ </span>

<h2 id="UNIQVAUE" style="color:green">TEXT_CONTENVT</h2>


<span style="color:green;">================================================================ </span>

<h2 id="UNIQVAUE" style="color:green">TEXT_CONTENVT</h2>


<span style="color:green;">================================================================ </span>

<h2 id="UNIQVAUE" style="color:green">TEXT_CONTENVT</h2>


<span style="color:green;">================================================================ </span>

<h2 id="UNIQVAUE" style="color:green">TEXT_CONTENVT</h2>


<span style="color:green;">================================================================ </span>

<h2 id="UNIQVAUE" style="color:green">TEXT_CONTENVT</h2>



