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

## Running server 🏎
```cmd
>> py manage.py runserver
```


## Handling migrations 🧩
```cmd
>> py manage.py makemigrations
>> py manage.py migrate
```

## Create adm access 👑
```cmd
>> py manage.py createsuperuser
```

# Settings ⚙
After creating your app you need to add it to `INSTALLED_APPS`

```python
 + ALLOWED_HOSTS = ['*']
```

```python
TEMPLATES = [
  {
    # ...
    + 'DIRS': ['templates'],
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
```cmd
>> STATIC_URL = 'static/'
```
List of directories where django will look for static files
```cmd
>> STATICFILES_DIRS = [os.path.join(BASE_DIR, 'templates/static/')]
```
![Exemple](https://github.com/raphavtorres/documentation/blob/main/global/images/global-static.png)

Absolute file system path where static files will be gathered for use during the deployment or production process
```cmd
>> STATIC_ROOT = BASE_DIR / 'static'
```

### Media
`MEDIA_ROOT` specified the directory it will be stored the media file uploads via your Django application
```cmd
>> MEDIA_ROOT = os.path.join(BASE_DIR, 'media')
```
`MEDIA_URL` specifies the URL prefix that will be used to access media files via the web browser
```cmd
>> MEDIA_URL = 'media/'
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

