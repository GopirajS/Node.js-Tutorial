
## 🚀 Backend / Server Frameworks

* [express](#express)

* [fastify](#fastify)

* [koa](#koa)

* [hapi](#hapi)

* [nestjs](#nestjs)


---

## 🔐 Authentication / Authorization

* [jsonwebtoken](#jsonwebtoken)

* [passport](#passport)

* [passport-jwt](#passport-jwt)

* [bcrypt](#bcrypt)

* [bcryptjs](#bcryptjs)

* [express-session](#express-session)


---

## 🛡️ Security / Protection

* helmet
* cors
* csurf
* express-rate-limit
* rate-limiter-flexible

---

## 🗄️ Database / ORM / ODM

* mongoose
* sequelize
* prisma
* typeorm
* knex
* objection

---

## ⚡ Real-Time / WebSocket

* socket.io
* ws
* uwebsockets.js

---

## 📡 HTTP / API Clients

* axios
* node-fetch
* got
* superagent

---

## 🧪 Testing

* jest
* mocha
* chai
* supertest
* vitest

---

## 🛠️ Utility Helpers

* lodash
* moment
* dayjs
* uuid
* nanoid
* dotenv

---

## 📁 File Upload / File System

* multer
* formidable
* fs-extra
* busboy

---

## 🧾 Validation

* joi
* yup
* express-validator
* zod

---

## 🔄 Job Queue / Background Tasks

* bull
* bullmq
* agenda
* bee-queue

---

## 🧵 Process / Clustering

* pm2
* nodemon
* concurrently
* cross-env

---

## 📦 Build / Bundlers

* webpack
* vite
* esbuild
* parcel

---

## 🧠 Logging / Monitoring

* winston
* pino
* morgan
* debug

---

## ☁️ Cloud / AWS / Storage

* aws-sdk
* @aws-sdk/client-s3
* multer-s3

---

## 🧩 GraphQL

* graphql
* apollo-server
* type-graphql

---

## 📱 CLI Tools

* commander
* yargs
* inquirer

---

## 🧠 Caching

* redis
* ioredis
* node-cache
* cache-manager

---

## 🔍 Search Engines

* elasticsearch
* @elastic/elasticsearch
* meilisearch
* algoliasearch

---

## 🧾 PDF / Document

* pdfkit
* puppeteer
* playwright
* html-pdf
* jspdf

---

## 🖼️ Image Processing

* sharp
* jimp
* gm
* canvas

---

## 🎥 Video / Audio

* fluent-ffmpeg
* ffmpeg-static
* node-opus
* ytdl-core

---

## 📤 Email / SMS

* nodemailer
* mailgun-js
* sendgrid
* twilio
* nexmo

---

## 🧪 Mock / Fake Data

* faker
* chance
* casual
* mockjs

---

## 🔄 Data Parsing

* csv-parser
* fast-csv
* xml2js
* js-yaml

---

## 🔐 Encryption / Crypto

* crypto-js
* node-forge
* argon2

---

## 📦 Compression / Archive

* compression
* zlib
* archiver

---

## 📡 Microservices

* moleculer
* seneca
* tsoa

---

## 🧩 Dependency Injection

* inversify
* awilix
* tsyringe

---

## 🧠 AI / Machine Learning

* tensorflow
* @tensorflow/tfjs-node
* brain.js
* natural

---

## 🧠 NLP / Text Analysis

* natural
* compromise
* sentiment

---

## 🌍 Internationalization (i18n)

* i18next
* node-polyglot
* react-intl

---

## 🧩 Template Engines

* ejs
* pug
* handlebars

---

## 🛡️ API Documentation

* swagger-ui-express
* swagger-jsdoc
* redoc

---

## 🔌 Hardware / System

* node-gyp
* serialport
* systeminformation

---

## 🧬 Blockchain / Web3

* web3
* ethers
* hardhat

---

## 🧪 Load / Performance Testing

* autocannon
* artillery
* k6


<span style="color:green;">================================================================ </span>

<h1 style="text-align:center;" >🚀 Backend / Server Frameworks</h1>

<h2 id="express" style="color:green"> Express.js (Most Popular & Simple) </h2>

### ❓ What is Express?

Express is a **minimal web framework for Node.js** used to build **APIs and web servers**.

### ❓ Why use Express?

* Very **simple & lightweight**
* Huge community
* Tons of middleware available
* Best for **beginners**

### ❓ How does it work?

You create routes (`GET`, `POST`, etc.) and handle requests & responses.

---

### 🧪 Sample Code (Express)

```js
// Import express package
const express = require('express');

// Create express app
const app = express();

// Create a route
app.get('/', (req, res) => {
    res.send('Hello from Express!');
});

// Start the server
app.listen(3000, () => {
    console.log('Server running on port 3000');
});
```

### 🧠 Code Explanation

* `require('express')` → loads Express
* `express()` → creates the app
* `app.get()` → handles GET requests
* `res.send()` → sends response to browser
* `app.listen()` → starts server

---

<h2 id="fastify" style="color:green"> Fastify (High Performance) </h2>

### ❓ What is Fastify?

Fastify is a **very fast and efficient Node.js framework**.

### ❓ Why use Fastify?

* 🚀 Extremely **high performance**
* Built-in **schema validation**
* Lower memory usage

### ❓ How does it work?

Similar to Express but optimized for speed.

---

### 🧪 Sample Code (Fastify)

```js
// Import fastify
const fastify = require('fastify')();

// Create route
fastify.get('/', async (request, reply) => {
    return { message: 'Hello from Fastify!' };
});

// Start server
fastify.listen({ port: 3000 }, () => {
    console.log('Fastify running on port 3000');
});
```

### 🧠 Code Explanation

* `require('fastify')()` → creates fastify app
* `fastify.get()` → define route
* `return {}` → automatically sends JSON
* `listen()` → starts server

---

<h2 id="koa" style="color:green">🌀 Koa (Modern & Minimal)</h2>


### ❓ What is Koa?

Koa is a **modern framework by the creators of Express**.

### ❓ Why use Koa?

* Cleaner async/await code
* Lightweight
* More control over middleware

### ❓ How does it work?

Everything is middleware-based and async.

---

### 🧪 Sample Code (Koa)

```js
// Import Koa
const Koa = require('koa');

// Create app
const app = new Koa();

// Middleware
app.use(async (ctx) => {
    ctx.body = 'Hello from Koa!';
});

// Start server
app.listen(3000);
```

### 🧠 Code Explanation

* `new Koa()` → create app
* `app.use()` → middleware
* `ctx.body` → response body
* `listen()` → start server

---

<h2 id="koa" style="color:green">🧱 Hapi (Enterprise Ready)</h2>

### ❓ What is Hapi?

Hapi is a **configuration-driven framework** for large apps.

### ❓ Why use Hapi?

* Strong **security**
* Built-in **validation**
* Great for **enterprise projects**

### ❓ How does it work?

Routes are defined with detailed configuration.

---

### 🧪 Sample Code (Hapi)

```js
// Import Hapi
const Hapi = require('@hapi/hapi');

// Create server
const server = Hapi.server({
    port: 3000,
});

// Add route
server.route({
    method: 'GET',
    path: '/',
    handler: () => {
        return 'Hello from Hapi!';
    }
});

// Start server
server.start();
```

### 🧠 Code Explanation

* `Hapi.server()` → create server
* `server.route()` → define route
* `handler()` → handles request
* `server.start()` → start server

---

<h2 id="koa" style="color:green">🧠 NestJS (Enterprise + TypeScript)</h2>

### ❓ What is NestJS?

NestJS is a **full-featured framework** built on Express/Fastify.

### ❓ Why use NestJS?

* Uses **TypeScript**
* Clean architecture (MVC)
* Dependency Injection
* Best for **large-scale apps**

### ❓ How does it work?

Uses **controllers, services, modules**.

---

### 🧪 Sample Code (NestJS Controller)

```ts
// Import Controller and Get
import { Controller, Get } from '@nestjs/common';

// Create controller
@Controller()
export class AppController {

  // Define route
  @Get()
  getHello(): string {
    return 'Hello from NestJS!';
  }
}
```

### 🧠 Code Explanation

* `@Controller()` → defines controller
* `@Get()` → handles GET request
* `getHello()` → returns response
* Nest automatically handles server setup

---

## 📊 Quick Comparison Table

| Framework | Best For            | Difficulty |
| --------- | ------------------- | ---------- |
| Express   | Beginners           | ⭐         |
| Fastify   | Performance         | ⭐⭐       |
| Koa       | Clean async code    | ⭐⭐       |
| Hapi      | Enterprise security | ⭐⭐⭐     |
| NestJS    | Large scalable apps | ⭐⭐⭐⭐   |

---

## ✅ Recommendation

* **New to Node?** → Express
* **Need speed?** → Fastify
* **Enterprise app?** → NestJS
* **Full control?** → Koa



<span style="color:green;">================================================================ </span>


<h1 style="text-align:center;" >🔐 Authentication / Authorization</h1>

<h2 id="jsonwebtoken" style="color:green"> 🔑 jsonwebtoken (JWT)</h2>

### ❓ What is jsonwebtoken?

`jsonwebtoken` is used to **create and verify JWT tokens** for authentication.

### ❓ Why use it?

* Stateless authentication
* No server-side session storage
* Works well with APIs & mobile apps

### ❓ How does it work?

1. User logs in
2. Server generates a token
3. Client sends token with every request

---

### 🧪 Sample Code (JWT)

```js
// Import jsonwebtoken
const jwt = require('jsonwebtoken');

// Secret key (keep it safe!)
const SECRET_KEY = 'my_secret_key';

// Create token
const token = jwt.sign(
    { userId: 1, role: 'admin' }, // payload
    SECRET_KEY,                  // secret
    { expiresIn: '1h' }           // token expiry
);

// Verify token
const decoded = jwt.verify(token, SECRET_KEY);

console.log(decoded);
```

### 🧠 Code Explanation

* `jwt.sign()` → creates token
* `jwt.verify()` → checks token validity
* Payload holds user info
* Token expires in 1 hour

---

<h2 id="jsonwebtoken" style="color:green"> 🧭 Passport.js (Authentication Engine)</h2>

### ❓ What is Passport?

Passport is an **authentication middleware** for Node.js.

### ❓ Why use Passport?

* Supports **many login strategies**
* Works with Google, Facebook, JWT, etc.
* Flexible and powerful

### ❓ How does it work?

Passport uses **strategies** to authenticate users.

---

### 🧪 Sample Code (Passport Local)

```js
const passport = require('passport');
const LocalStrategy = require('passport-local').Strategy;

// Define local strategy
passport.use(new LocalStrategy(
    (username, password, done) => {

        // Dummy user check
        if (username === 'admin' && password === '1234') {
            return done(null, { id: 1, username });
        }

        return done(null, false);
    }
));
```

### 🧠 Code Explanation

* `passport.use()` → registers strategy
* `LocalStrategy` → username/password login
* `done()` → success or failure callback

---

<h2 id="passport-jwt" style="color:green"> 🎫 passport-jwt (JWT + Passport)</h2>

### ❓ What is passport-jwt?

It is a **Passport strategy** for JWT authentication.

### ❓ Why use it?

* Combines JWT + Passport
* Protects routes easily
* Token-based security

### ❓ How does it work?

Reads JWT from request header and verifies it.

---

### 🧪 Sample Code (passport-jwt)

```js
const { Strategy, ExtractJwt } = require('passport-jwt');

const opts = {
    jwtFromRequest: ExtractJwt.fromAuthHeaderAsBearerToken(),
    secretOrKey: 'my_secret_key',
};

// JWT strategy
passport.use(new Strategy(opts, (jwtPayload, done) => {
    return done(null, jwtPayload);
}));
```

### 🧠 Code Explanation

* `ExtractJwt.fromAuthHeaderAsBearerToken()` → reads token
* `secretOrKey` → verifies token
* `jwtPayload` → decoded token data

---

<h2 id="passport-jwt" style="color:green"> 🔐 bcrypt (Password Hashing)</h2>

### ❓ What is bcrypt?

`bcrypt` hashes passwords so they **cannot be read**.

### ❓ Why use it?

* Protects user passwords
* Prevents data leaks
* Industry standard

### ❓ How does it work?

Password → Hash → Store → Compare during login

---

### 🧪 Sample Code (bcrypt)

```js
const bcrypt = require('bcrypt');

// Hash password
const password = 'mypassword';
const hashedPassword = bcrypt.hashSync(password, 10);

// Compare password
const isMatch = bcrypt.compareSync(password, hashedPassword);

console.log(isMatch); // true
```

### 🧠 Code Explanation

* `hashSync()` → encrypts password
* `10` → salt rounds (security level)
* `compareSync()` → checks password

---

<h2 id="bcryptjs" style="color:green"> 🔐 bcryptjs (Pure JS Alternative)</h2>

### ❓ What is bcryptjs?

A **JavaScript-only version** of bcrypt.

### ❓ Why use it?

* No native build
* Easier setup on Windows/shared hosting

### ❓ How does it work?

Same API as bcrypt but slightly slower.

---

### 🧪 Sample Code (bcryptjs)

```js
const bcrypt = require('bcryptjs');

// Hash password
const hash = bcrypt.hashSync('secret', 10);

// Compare
const valid = bcrypt.compareSync('secret', hash);

console.log(valid);
```

### 🧠 Code Explanation

* Same usage as bcrypt
* Easier installation
* Good for simple apps

---

<h2 id="express-session" style="color:green"> 🔐 express-session (Session-Based Auth)</h2>

### ❓ What is express-session?

Used to **store user session data** on the server.

### ❓ Why use it?

* Traditional login system
* Session stored in memory/db
* Works well with Passport

### ❓ How does it work?

Session ID stored in cookie, data on server.

---

### 🧪 Sample Code (express-session)

```js
const session = require('express-session');

// Use session middleware
app.use(session({
    secret: 'session_secret',
    resave: false,
    saveUninitialized: true,
}));
```

### 🧠 Code Explanation

* `secret` → encrypts session ID
* `resave` → prevents unnecessary saves
* `saveUninitialized` → saves new sessions

---

## 🔐 JWT vs Session (Quick View)

| Feature     | JWT    | Session  |
| ----------- | ------ | -------- |
| Storage     | Client | Server   |
| Scalability | High   | Medium   |
| Stateless   | Yes    | No       |
| Best for    | APIs   | Web apps |

---

## ✅ Best Practice Recommendation

* **API / Mobile App** → JWT + passport-jwt
* **Web App** → express-session + Passport
* **Password Security** → bcrypt


<span style="color:green;">================================================================ </span>




<span style="color:green;">================================================================ </span>
