## CRUD

In controllers/tasks.js, implemented logic for CRUD operations.

- createTask function awaits the creation of the task. Then once the task is created, sends 201 status and json response.
- getTask function retrieves the data identified by the ID.
- all the other logic just sends the strings with the operations made.

## Setting up DB with mongoose ODM

models/Task.js

- used mongoose to set up the schema/structure for tasks in MongoDB. then export this model as Task and used it in controllers to perform CRUD.

## Connecting MongoDB

```js
require("dotenv").config();
```

- set up MongoDB and exported string. put string inside .env (note: cannot be put on production), connected in connect.js through mongoose. then called it in app.js

## Routes

- logic for HTTP method. visit /localhost -> simple get request, handled localhost/id defined in main app.js to perform operations.

## Calling everything in app.js

- importing tasks route file and db connection. also, environment configuration with process.env. how to do that with process.env ->

1. load .env file with data
2. ```js
   require("dotenv").config();
   ```

loads environment variables from .env intro process.env 3) process.env.data -> now you can access data specified in .env file

### Middleware

- taking raw request and transforming it into JS object, which can then be accessed in route handlers

- routes -> simple greeting when accessed /hello endpoint
- all routes defined in tasks.js will be prefixed with /api/v1/tasks

### Start the port

created asynchronous function. connectDB returns promise, execution is delayed untill it responds with something (i mean success). if not return error, if success start the port.

## Mongoose Logic for error handling + how to create schemas in mongoose

```js
const TaskSchema = new mongoose.Schema({});
```

- creating a new Schema with mongoose.Schema assigning to variable TaskSchema
- exporting as Task, the model will be referred to as task that takes all of the properties of TaskSchema
