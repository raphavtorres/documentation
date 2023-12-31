# Django Basic


## Setup environment 🏗

Creating virtual environment
```cmd
>> py -m venv <env_name>
>> <env_name>\Scripts\activate
>> pip freeze > requirements.txt
```

Installing Django
```cmd
>> pip install django
>> django-admin startproject <project_name> .
>> py manage.py startapp <app_name>
```

## Running server 🏃‍♀️
```cmd
>> py manage.py runserver
```

## Create adm access 👑
```cmd
>> py manage.py createsuperuser
```

# Settings ⚙
After creating your app you need to add it to `INSTALLED_APPS`

```python
ALLOWED_HOSTS = ['*']
```

```python
TEMPLATES = [
  {
    # ...
    'DIRS': ['templates'],
    # ...
  }
]
```
```python
LANGUAGE_CODE = 'en-us'
# LANGUAGE_CODE = 'pt-br'
```

```python
TIME_ZONE = 'America/Sao_Paulo'
```

### Static Files
Base URL prefix for static files served by your application
```python
STATIC_URL = 'static/'
```
List of directories where django will look for static files
```python
STATICFILES_DIRS = [os.path.join(BASE_DIR, 'global/static/')]
```
![Exemple](https://github.com/raphavtorres/documentation/blob/main/global/images/global-static.png)

Absolute file system path where static files will be gathered for use during the deployment or production process
```python
STATIC_ROOT = os.path.join(BASE_DIR, 'staticfiles')
```

### Media
`MEDIA_ROOT` specified the directory it will be stored the media file uploads via your Django application
```python
MEDIA_ROOT = os.path.join(BASE_DIR, 'media')
```
`MEDIA_URL` specifies the URL prefix that will be used to access media files via the web browser
```python
MEDIA_URL = 'media/'
```

# Models 🎲
After create or modify the models archive run: 
```cmd
>> py manage.py makemigrations
```
This command is used to create new migration files based on the changes you have made to your Django models

```cmd
>> py manage.py migrate
```
This command reads the migration files and executes the necessary SQL statements to bring your database schema up to date with the changes you've defined in your `models.`

# Tests 🏎 
```cmd
>> pip install model_mommy coverage
```
![Exemple](https://github.com/raphavtorres/documentation/blob/main/global/images/test_folders.png)
<br>

Create a `.coveragerc` in the root of your project
And paste this code, to omit files that shouldn't be tested
```text
[run]
source = .

omit = 
  */__init__.py
  */settings.py
  */manage.py
  */wsgi.py
  */apps.py
  */urls.py
  */admin.py
  */migrations/*
  */tests/*
```

Run tests and access report
```cmd
>> coverage run manage.py test
>> coverage report
```

Go to your `.gitignore` and paste `htmlcov/*`
```cmd
>> coverage html
```
Creates a report in html

You can run the report on the web
```cmd
>> cd htmlcov
>> python -m http.server
```

