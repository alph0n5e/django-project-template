# {{ project_name }}

[Django {{ django_version }}](https://docs.djangoproject.com/en/{{ docs_version }}/) project, running with [Python 3.7](https://docs.python.org/3/)

## Requirements
- Python 3.7
- Virtualenv (`pip3 install virtualenv`)

## Setup
Create a Python virtual environment:
```bash
$ virtualenv -p python3.7 env
$ source env/bin/activate
```

For development requirements:
```bash
(env)$ pip install -r requirements-dev.txt
```

For production requirements:
```bash
(env)$ pip install -r requirements.txt
```

## Running
### Database
This project uses PostgreSQL as its database engine.
For local development, the default configuration is specified in [dev.py]({{ project_name }}/conf/settings/dev.py#L5-L9)

Before starting the development server, make sure that:
- PostgreSQL is running,
- The database and its associated user (with password) exist and have the proper permissions.

### Development server:
For local development, you can use Django's built-in development server:
```bash
(env)$ cd {{ project_name }}/
(env)$ python manage.py runserver
```

Other `manage.py` commands, see:
```bash
(env)$ python manage.py --help
```

# About this template
This template is based on the project layout recommended by @pydanny and @audreyr in their ["Two Scoops of Django"](https://www.twoscoopspress.com/collections/everything/products/two-scoops-of-django-1-11) book, 
as well as my personal experience with Django so far.

This is only a lightweight Django project template layout. 

If you are looking for a more comprehensive setup, check out Cookiecutter templates such as [cookiecutter-django](https://github.com/pydanny/cookiecutter-django), or my own [django-cookiecutter-template](https://github.com/alph0n5e/django-cookiecutter-template). 

To use this template with the `startproject` django admin command:
```bash
django-admin startproject \
    --template https://github.com/alph0n5e/django-project-template.git \
    --extension py,txt,md
```
