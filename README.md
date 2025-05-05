# A dvd club web app

A simple web app with a front end of a single `html webpage` and a `js script` that communicates through a `python flask api` with the `MongoDB` database to read/store movies.

## Steps to deploy the application

### Pull images from both compose files

`docker-compose -f docker-compose-backend.yml pull`

`docker-compose -f docker-compose-frontend.yml pull`

### Create the flask app for mongodb

`docker-compose -f docker-compose-backend.yml build`

### Run the backend stack

`docker-compose -f docker-compose-backend.yml up`

The stack contains the `Mongo-explorer` service to visualize the collections and documents in the database. The explorer is available using the url: `localhost:8081`.

The flask app uses the url `localhost:8080/swagger` to provide a swagger UI for the available request endpoints with examples.

### Run the frontend http server

`docker-compose -f docker-compose-frontend.yml up`

The http server uses the default port (80) to access the web app through the `localhost` url. 

