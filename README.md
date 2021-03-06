\![alt text][pypi_version] ![alt text][licence_version]

# Django Telethon MultiSession

A Telethon session storage implementation backed for Django ORM to use telethon in django projects.

Tested with:
* Python 3.7+
* Django 2.2+

Use the following command to install using pip:
```
pip install django-telethon-multisession
```

## Usage example
Usage is very simple, just follow three simple steps below
### Add Django-Telethon-Session to your installed apps
First add django telethon session to your installed apps in your django project settings:

```python
INSTALLED_APPS = [
    ...,
    'django_telethon_multisession',
    ...
]
```

### Migrate the database
Then run `migrate` command to create migrations in database.

```shell script
python manage.py migrate
```

### Use custom session
Use the session in `django_telethon_multisession.sessions` to initialize telegram client:
```python
from django_telethon_multisession.sessions import DjangoMultiSession
client = TelegramClient(DjangoMultiSession("session_name"))
```

Feel free to send pull requests or report issues!

[pypi_version]: https://img.shields.io/pypi/v/pykson.svg "PYPI version"
[licence_version]: https://img.shields.io/badge/license-MIT%20v2-brightgreen.svg "MIT Licence"
