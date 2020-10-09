#  Rails in Docker Quickstart

Ruby 2.7.1

Clone this repo. `cd` into the directory.

Run your new rails command like so:

    docker-compose run web rails new . --force --no-deps --database=postgresql --webpack=stimulus

Watch docker compose create your new Rails app.

Rebuild the docker image:

    docker-compose build

In `config/database.yml` add a host key to point to `db`:

    encoding: unicode
    host: db

As `db` is the name of the DB container in docker compose.

Boot the app:

    docker-compose up

Create the database:

    docker-compose run web rake db:create

You're getting the message on how to run rails and rake commands in docker compose now.
