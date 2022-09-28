# Django - Install Soft Dashboard Theme

This free sample explains how to create from scratch a new Django project, add authentication and improve the UI by installing Soft Dahsboard, a modern BS5 design. 

<br />

# Create the project

> Create the directory 

```bash
$ mkdir my-django-project
$ cd my-django-project
```

<br />

> Install the dependencies

```bash
$ virtualenv env
$ source env/bin/activate
$ pip install Django
```

<br />

> Create the Django project

```bash
$ django-admin startproject core . 
```

<br />

> Set Up the database

```bash
$ python manage.py makemigrations
$ python manage.py migrate
```

<br />

> Start the app

```bash
$ python manage.py runserver
```

> Create a superuser

```bash
$ python manage.py createsuperuser
```

At this point we can access the `admin` section that uses a minimal style. 

<br />

## Install Soft UI Design

> Install the PyPi package

```bash
$ pip install django-admin-soft-dashboard
```

<br />

> Configure Django to use the new design

> Add `admin_soft` application to the `INSTALLED_APPS` setting of your Django project `settings.py` file (note it should be before `django.contrib.admin`):

```python
    INSTALLED_APPS = (
        ...
        'admin_soft.apps.AdminSoftDashboardConfig',
        'django.contrib.admin',
    )
```

<br />

> Start the app and access the new admin design

```bash
$ python manage.py runserver
```

<br />

## Add a new app

This section explains how to add a minimal app that handles ordinary users registration. 

> Create the new app

```bash
$ django-admin startapp authentication
```

> Update the app settings (`INSTALLED_APPS` section)

```python
# core/python.py (truncated content)
...
INSTALLED_APPS = [
    'admin_soft.apps.AdminSoftDashboardConfig',
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'authentication',
]
... 
```

<br />

---
Django, How to Install Soft Dashboard Theme - Open-source sample provided by [AppSeed](https://appseed.us)
