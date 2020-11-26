# Star Social App

Fullstack Django social media app implemented using Django 3 with MVT (Model-View-Template) architecture and CVBs (Class-Based-Views). The app is a community for fans of outer space. Users can create groups on various topics (eg. SpaceX, NASA, Pluto, etc.). Users can then create posts in the groups; they can also leave and join other groups. New users are able to signup, and can link user profiles with the @ symbol.

Hosted example: https://star-social-django-fullstack.herokuapp.com/

### Install

    $ pipenv install

### Setup

#### Migrations

    $ pipenv shell
    $ python manage.py migrate

### Run

    $ pipenv shell
    $ python manage.py runserver

### Deploy to Heroku

Create a Heroku app:

    $ heroku create <app-name>

Set up Heroku Remote Git:

    $ git remote set-url heroku <remote-heroku-git-url>

Push to Heroku for Deployment:

    $ git push heroku master

NOTE: make sure all changes are commit to git before running this command

Creating the PostgreSQL DB:

    $ heroku addons:create heroku-postgresql:hobby-dev --app=<app-name>

Apply Migrations to PostgreSQL DB:

    $ heroku run python manage.py migrate

Logs:

    $ heroku logs --tail
