# Ex02 Django ORM Web Application

### Date: 10-10-2023

## AIM
To develop a Django application to store and retrieve data from a Football Players database using Object Relational Mapping(ORM).


## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub.

### STEP 2:
Create a new app in Django project.

### STEP 3:
Enter the code for admin.py and models.py.

### STEP 4:
Execute Django admin and create 10 Football players.

## PROGRAM

### models.py
```py
from django.db import models
from django.contrib import admin
class Player(models.Model):
    Player_Name=models.CharField(max_length=50)
    Jersy_No=models.IntegerField()
    Team=models.CharField(max_length=20)
    Height=models.IntegerField()
    Position=models.CharField(max_length=100)

class Player_Admin(admin.ModelAdmin):
    list_display=('Player_Name','Jersy_No','Team','Height','Position')

```

### admin.py
```py
from django.contrib import admin
from .models import Player,Player_Admin
admin.site.register(Player,Player_Admin)
```

## OUTPUT

![terminal](https://github.com/Anbuselvan04/ORM/assets/119410896/511221b2-5720-4fce-bc07-1f691fcabcd3)

![output](https://github.com/Anbuselvan04/ORM/assets/119410896/d303bcec-c4ea-47f9-a0c8-047f1d7115b8)

## RESULT
Thus the program for creating a database using ORM hass been executed successfully.
