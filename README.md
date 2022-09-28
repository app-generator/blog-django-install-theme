# Django - Install [Soft Dashboard Theme](https://github.com/app-generator/django-admin-soft-dashboard)

This free sample explains how to create from scratch a new Django project, add authentication and improve the UI by installing **[Soft Dashboard](https://github.com/app-generator/django-admin-soft-dashboard)**, a modern BS5 design from `Creative-Tim`. 

<br />

![Django, Install Soft Dashboard Theme - Index Page.](https://user-images.githubusercontent.com/51070104/192701821-946628cd-25ce-494f-a6e5-9a1b14c81fd4.jpg)

<br />

# ✨ Create the project

> 👉 **Create the directory** 

```bash
$ mkdir my-django-project
$ cd my-django-project
```

<br />

> 👉 **Install the dependencies**

```bash
$ virtualenv env
$ source env/bin/activate
$ pip install Django
```

<br />

> 👉 **Create the Django project**

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

> 👉 **Start the app**

```bash
$ python manage.py runserver
```

<br />

![Django, Install Soft Dashboard Theme - Default Django Page.](https://user-images.githubusercontent.com/51070104/192701963-dd017bb9-4958-44b6-b695-0195272dc9a8.jpg)

<br />

> 👉 **Create a superuser**

```bash
$ python manage.py createsuperuser
```

At this point we can access the `admin` section that uses a minimal style. 

<br />

![Django, Install Soft Dashboard Theme - Default Admin UI.](https://user-images.githubusercontent.com/51070104/192702068-2ecc1a2b-e9d2-478e-ac50-4b951eee2f0f.jpg)

<br />

## ✨ Install Soft UI Design

> 👉 **Install the PyPi package**

```bash
$ pip install django-admin-soft-dashboard
```

<br />

> 👉 **Configure Django to use the new design**

> Add `admin_soft` application to the `INSTALLED_APPS` setting of your Django project `settings.py` file (note it should be before `django.contrib.admin`):

```python
    INSTALLED_APPS = (
        ...
        'admin_soft.apps.AdminSoftDashboardConfig',
        'django.contrib.admin',
    )
```

<br />

> 👉 **Start the app and access the new admin design**

```bash
$ python manage.py runserver
```

<br />

![Django, Install Soft Dashboard Theme - Default Admin UI.](https://user-images.githubusercontent.com/51070104/192702182-d083ff5f-31f8-479d-aacd-4bc795bbd9ba.jpg)

<br />

## ✨ Add a new app

This section explains how to add a minimal app that handles ordinary users registration. 

> 👉 **Create the new app**

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
    'authentication',                # <-- NEW
]
... 
```

<br />

> 👉 **Start the project** and `access the new admin` design

```bash
$ python manage.py runserver
```

<br />

![Django, Install Soft Dashboard Theme - New Sign UI page.](https://user-images.githubusercontent.com/51070104/192702349-6133424d-e930-42f9-8b03-6e97b27e3993.jpg)

<br />

---
**[Django](https://appseed.us/apps/django/)**, How to Install [Soft Dashboard Theme](https://github.com/app-generator/django-admin-soft-dashboard) - Open-source sample provided by [AppSeed](https://appseed.us)
