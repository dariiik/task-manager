## CRUD

In controllers/tasks.js, implemented logic for CRUD operations.

- createTask function awaits the creation of the task. Then once the task is created, sends 201 status and json response.
- getTask function retrieves the data identified by the ID.
- all the other logic just sends the strings with the operations made.

## Setting up DB with mongoose ODM

models/Task.js

- used mongoose to set up the schema/structure for tasks in MongoDB. then export this model as Task and used it in controllers to perform CRUD.
