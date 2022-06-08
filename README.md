# Installation


- Clone **IPASSIO** repository
- Install Python
- Create and activate virtualenv
```
python3 -m venv <virtual-env-name>

source <virtual-env-name>/bin/activate # For linux

<virtual-env-name>\Scripts\activate # For windows

```

- Install requirements

```
# First install the requirements as mentioned in requirements.txt file

pip3 install -r requirements.txt

# Install django-payu==0.5 separately

pip3 install django-payu==0.5

# Install newer version of django again

pip3 install django==3.2.11

# This is because the latest version of django-payu is specified to work only with django <= 2.0.2 . This is a known problem and needs fix
```

- Setup DB Credentials in *IpassioNeo/settings.py*

```
# For postgres

DATABASES = {
  'default': {
      'ENGINE': 'django.db.backends.postgresql',
      'NAME': '<db-name>',
      'USER': '<user-name>',
      'PASSWORD': '<password>',
      'HOST': '<host-running-db>',
      'PORT': '5432',
  }
}
```

- Generate migrations and migrate to database

```

python manage.py makemigrations

python manage.py migrate

```

- Create a superuser

```
python manage.py createsuperuser

# When asked, pass 'True' in 'Admin:' field
```

- Run Django server locally

```
python manage.py runserver

# By default it runs on port 8080. That can be changed by passing the port after runserver command

python manage.py runserver 7000
```

## DEBUGGING

- In settings.py, make sure there are no trailing backward slashes inside ```os.path.join(BASE_DIR, 'path')``` as Windows systems don't use backward slashes. Keep the word as it is without any slashes and ```join()``` method will take care of the correct slash behavior.



## [Detailed Documentation](https://github.com/Rohit-Personal-Userfacet/twilio-django/tree/main/docs)
## [Twilio Conversations](./chats/flow.md)
