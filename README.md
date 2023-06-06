## Django ORM Web Application
# AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
Include your ER diagram here

## DESIGN STEPS
# STEP 1:
In this folder use necessary commands to create the django project folder commands using django-admin startproj myproj. Then move into the folder myproj where manage.py file is located. Now give the commands python3 manage.py startapp myapp to create myapp. Then change the necessary settings in the settings.py. In settings.py add import os in the line where we need to import libraries. Then add your url in ALLOWED_HOSTS =[ ‘’ ] Then add ‘myapp’ in the configuration INSTALLED_APPS. Then add STATICFILES_DIRS=[ os.path.join(BASE_DIR,'static') ]

Look at the list of installed apps in settings.py: INSTALLED_APPS = [

# STEP 2:
To create admin account enter the following command to create a superuser:

python3 manage.py makemigrations python3 manage.py migrate

python3 manage.py createsuperuser

Add the username and email for the superuser as follows. Username (leave blank to use 'django'): admin Email address: admin@example.com The next prompt in the shell is for your password. Add a strong password and press the Enter key to confirm it once again: Password: Password (again): You should see the following message on your screen: Superuser created successfully.

# STEP 3:
Visit the admin app at http://<>:8000/admin and log in with the superuser account that you have created:

PROGRAM
```from django.db import models
from django.contrib import admin
class GitDatabase(models.Model):
    username_primary_key = models.CharField(max_length=30, help_text="User name must be unique", primary_key=True,unique=True)
    password = models.CharField(max_length=30)
    firstname = models.CharField(max_length=20)
    lastname = models.CharField(max_length=20)
    profile_photo = models.ImageField()
    email = models.EmailField(max_length=50,unique=True)
class GitAdmin(admin.ModelAdmin):
    list_display = ('username_primary_key', 'password', 'firstname', 'lastname','profile_photo','email')
  ```
  
  
  ### output
  ![image](https://github.com/KISHORPRIAN/django-orm-app/assets/124072773/e09eac43-22f6-45f2-8257-dd88cb4c7e03)



## RESULT

Thus a Django application is successfully developed to store and retrieve data from a database using Object Relational Mapping(ORM).
