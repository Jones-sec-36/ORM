# Ex02 Django ORM Web Application
## Date: 14-11-2024

## AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM

![386115358-54390974-079d-494c-bf7c-ef70d6561060](https://github.com/user-attachments/assets/93c55bda-b4e8-40ba-8b67-3f4cbb461841)

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM
models.py

from django.db import models
from django.contrib import admin
class Bank (models.Model):
    loan_id=models.IntegerField(primary_key=True)
    cust_acno=models.IntegerField()
    cust_name=models.CharField(max_length=100)
    loan_amt=models.FloatField()
    loan_type=models.CharField(max_length=100)
 
class BankAdmin(admin.ModelAdmin):
    list_display=('loan_id','loan_type','loan_amt','cust_acno')

admin.py

from django.contrib import admin
from .models import Bank,BankAdmin
admin.site.register(Bank,BankAdmin)

## OUTPUT

![Screenshot (1)](https://github.com/user-attachments/assets/e8d779e6-3601-4eb1-ba24-381fd78488a0)

## RESULT
Thus the program for creating a database using ORM hass been executed successfully
