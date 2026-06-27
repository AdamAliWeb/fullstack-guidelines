# Node & Express.js

## References

- **[Node.js Documentation](https://nodejs.org/en)**
- **[Express.js Documentation](https://expressjs.com/en/)**

## Libraries

- nodemon - This will help to restart the server when you make any changes to the code.

- jsonwebtoken - This package helps in generating a JSON web token which we will use for authentication. A JSON web token (JWT) is a JSON object used to communicate information securely over the internet (between two parties). It can be used for information exchange and is typically used for authentication systems.

- express-session - This package will help us to maintain the authentication for the session.

- socket.io - This is a library that enables low-latency, bidirectional and event-based communication between a client and a server.

## Workflows

### Initial Express Structure

```js
const express = require("express");
const app = express();
const PORT = process.env.PORT || 3000;

// Middleware for parsing JSON
app.use(express.json());

// Routes (imported from routes folder)
const userRoutes = require("./routes/userRoutes");
app.use("/api/users", userRoutes);

// Basic error handling middleware
app.use((err, req, res, next) => {
  console.error(err.stack);
  res.status(500).send("Something broke!");
});

app.listen(PORT, () => {
  console.log(`Server is running on port ${PORT}`);
});
```
