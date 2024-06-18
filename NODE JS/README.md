## Q.1. What is Express.js and why is it used? How do you install Express.js in a Node.js project?

**Ans: Express.js is a fast, and minimalist web framework for Node.js, ideal for building web applications and APIs12. It simplifies handling HTTP requests and is part of the MERN stack.**

### To install Express.js in a Node.js project, you can use npm (Node Package Manager), which is bundled with Node.js. Here are the steps:-
- Navigate to your project directory in the terminal.
- Run the following command to initialize a new Node.js project 

```bash
 npm init -y
```

- Install Express.js by running the following command:
```bash
 npm install express
```

- Once installed, you can start using Express.js in your Node.js project by requiring it in your JavaScript files:

```bash
 const express = require('express');
 const app = express();
```

<hr>

## Q.2. How do you create a simple Express.js server?

### Ans 👇

- First, install Express using npm (Node Package Manager):

```bash
 npm install express
```
- Create an Express Application: Create an index.js file (or any other name you prefer) and add the following code:

```bash
 const express = require('express');
 const app = express();
```

- Define a route handler for the root path
```bash
 app.get('/', (req, res) => {
 res.send('Hi there');
});
```

- Start the server on port 3000

```bash
 app.listen(3000, () => {
 console.log('Server is listening on port 3000...');
});
```

- Run the Server: Open your terminal, navigate to the project directory, and run:

```bash
 node index.js
```

### 3. What is a RESTful API? How do you set up a basic Express.js server for a RESTful API?

**Ans:**

**What is a RESTful API?**

- A RESTful API (also known as a REST API or RESTful web API) adheres to the design principles of the representational state transfer (REST) architectural style.
- It allows different computer systems to communicate securely over the internet by following a set of rules for how that communication should take place.
- RESTful APIs use standardized formats (such as JSON or XML) for requests and responses, enabling seamless interaction between applications.

**Setting Up a Basic Express.js Server for a RESTful API:**

First, make sure you have Node.js installed on your system. Then, follow these steps to create a simple Express.js server for a RESTful API:

```javascript
// 1. Install Express.js (if not already done)
// Run: npm install express

// 2. Create an Express server
const express = require('express');
const app = express();
const port = 3000;

// 3. Define a route (e.g., for the root path '/')
app.get('/', (req, res) => {
    res.send('Hello, RESTful API!');
});

// 4. Start the server
app.listen(port, () => {
    console.log(`Server is listening at http://localhost:${port}`);
});
