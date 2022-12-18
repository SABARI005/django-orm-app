# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![WhatsApp Image 2022-12-18 at 21 09 05](https://user-images.githubusercontent.com/118660461/208306968-5a19ce1d-d590-4d51-aae4-9213882da6a9.jpg)

## DESIGN STEPS

### STEP 1:
Create a new django project using "django-admin startproject",get into the project's terminal and use "python3 manage.py startapp" command.
### STEP 2:
Define a model for the cricketers_details in the models.py and allow host access and add the app name under installed apps in settings.py
### STEP 3:
Register the models with the Django admin side.In admin.py under app folder,register the models with Django admin site.


## PROGRAM
```
from django.db import models
from django.contrib import admin
# Create your models here.
class cricketers_details(models.Model):
    cricketersname= models.CharField(max_length=100)
    age = models.IntegerField()
    jerseyno = models.IntegerField(primary_key = True)
    teamname = models.CharField(max_length=200)
    totalruns=models.IntegerField()


class cricketers_detailsAdmin(admin.ModelAdmin):
    list_display = ('cricketersname','age','jerseyno','teamname','totalruns')
```

## OUTPUT
###admin output

![WhatsApp Image 2022-12-18 at 21 09 06](https://user-images.githubusercontent.com/118660461/208306984-f36479ba-9237-43bd-9ba4-d81fb73c66ea.jpg)


## RESULT
the program is executed successfully
