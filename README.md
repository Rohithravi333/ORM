# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![OUTPUT](./omr1.png)

## DESIGN STEPS

### STEP 1:
create a migration file that contains code for the database schema of a model
### STEP 2:
apply all the migration to the database
### STEP 3:
open admin.py nd type the following


## PROGRAM
```

admin.py

from django.contrib import admin
from .models import Employee,EmployeeAdmin
admin.site.register(Employee,EmployeeAdmin)

models.py

from django.db import models
from django.contrib import admin
class Employee (models.Model):
    eid=models.CharField(max_length=20,help_text="Employee ID")
    name=models.CharField(max_length=100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()

class EmployeeAdmin(admin.ModelAdmin):
    list_display=('eid','name','salary','age','email')
 
```

## OUTPUT

![OUTPUT](./omr.png)


## RESULT
THE PROGRAM HAS BEEN EXECUTED SUCCESSFULLY