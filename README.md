# Django Channels Tutorial

This is a simple tutorial on how to use Django Channels to create a chat application. The tutorial is divided into several parts:

1. [Introduction to Django Channels](#introduction-to-django-channels)
2. [Setting up Django Channels](#setting-up-django-channels)
3. [Creating a Chat Application](#creating-a-chat-application)
4. [Running the Chat Application](#running-the-chat-application)

## Setup dev environment

1. Create a virtual environment: `conda create -n django-channels-tut-env -y python=3.10`
2. Activate the virtual environment: `conda activate django-channels-tut-env`
3. Install the required packages: `pip install -r requirements.txt`
4. Run the Django server: `python manage.py runserver`

## Introduction to Django Channels

Django Channels is a project that extends Django to handle WebSockets, chat protocols, IoT protocols, and more. It allows Django to handle asynchronous features like WebSockets and other protocols. Django Channels is built on top of the asynchronous features of Python 3.5+.

## Setting up Django Channels

### Installing Django Channels

To set up Django Channels, you need to install the `channels` package using pip:

```bash
pip install django channels[daphne]
```

### Create a new Django project

```bash
django-admin startproject chat_project
```

### Create a new Django app

Make sure you're in the same directory as `manage.py` and run the following command to create a new Django app:

```bash
python manage.py startapp chat
```

That’ll create a directory chat, which is laid out like this:

```text
chat/
    __init__.py
    admin.py
    apps.py
    migrations/
        __init__.py
    models.py
    tests.py
    views.py
```

For the purposes of this tutorial, we will only be working with `chat/views.py` and `chat/__init__.py`. So remove all other files from the chat directory.

After removing unnecessary files, the chat directory should look like:

```text
chat/
    __init__.py
    views.py
```

You also need to add `chat` to the `INSTALLED_APPS` in your Django settings file:

```python
INSTALLED_APPS = [
    ...
    'chat',
]
```

## References

- [Django Channels Tutorial Part 1](https://channels.readthedocs.io/en/latest/tutorial/part_1.html)
