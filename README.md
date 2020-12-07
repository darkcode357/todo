## Installation

`clone` the repository and use `pipenv` to create the virtual environment and install the dependencies. The instructions below assume you are using sqlite as your database, `~/dev` as your development directory, and pipenv as your environment manager. Modify as needed.

```
pip3 install --user git+https://github.com/pypa/pipenv.git
cd ~/dev
https://github.com/darkcode357/todo
cd todo
pipenv --python 3.6   # Initializes the virtual environment
pipenv install --dev  # Installs all dependencies
pipenv shell  # Activates the environment
```

Modify to match your local db credentials. In `local.py`:

```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': os.path.join(BASE_DIR, 'db.sqlite3'),
    }
}
```

Then:

`./manage.py migrate`

See additional instructions in the django-todo README.

