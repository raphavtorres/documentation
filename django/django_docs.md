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

# Settings
### Static Files in the directory root

```cmd
>> import os
>> STATIC_URL = 'static/'
>> STATICFILES_DIRS = [os.path.join(BASE_DIR, 'templates/static/')]
>> STATIC_ROOT = BASE_DIR / 'static'
```

### Media
MEDIA_ROOT specified the directory it will be stored the media file uploads via your Django application
```cmd
>> MEDIA_ROOT = os.path.join(BASE_DIR, 'media')
```
MEDIA_URL specifies the URL prefix that will be used to access media files via the web browser
```cmd
>> MEDIA_URL = 'media/'
```



