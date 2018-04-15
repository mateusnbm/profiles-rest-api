# Profiles REST API

REST API providing basic functionality for managing user profiles.

vagrant up
vagrant ssh
cd /vagrant

mkvirtualenv profiles_api --python=python3
deactivate
workon profiles_api

pip install -r requirements.txt

django-admin.py startproject profiles_project
cd profiles_project
python manage.py startapp profiles_api

pip freeze
pip freeze > requirements.txt

python manage.py runserver 0.0.0.0:8080

python manage.py makemigrations
python manage.py migrate
