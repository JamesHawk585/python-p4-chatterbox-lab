# To Do List: 

You'll be responsible for:

- [] Creating a model and migrations.
- [] Setting up the necessary routes to handle requests.
- [] Performing CRUD actions with SQLAlchemy.
- [] Sending the necessary JSON data in the responses.

### Model
Start by generating a `Message` model and the necessary migration code to create
messages with the following attributes:

- [x] "body": String.
- [x] "username": String.
- [x] "created_at": DateTime.
- [x] "updated_at": DateTime.

After creating the model and migrations, run the migrations and use the provided
`seed.py` file to seed the database:

```console
$ flask db revision --autogenerate -m'your message'
$ flask db upgrade
$ python seed.py
```

### Routes

Build out the following routes to handle the necessary CRUD actions:

- `GET /messages`: returns an array of all messages as JSON, ordered by
  `created_at` in ascending order.
- `POST /messages`: creates a new message with a `body` and `username` from
  params, and returns the newly created post as JSON.
- `PATCH /messages/<int:id>`: updates the `body` of the message using params,
  and returns the updated message as JSON.
- `DELETE /messages/<int:id>`: deletes the message from the database.

***