# Ex02 Django ORM Web Application
## Date: 
14/11/2024
## AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM

![alt text](<WhatsApp Image 2024-11-14 at 14.16.41_460f26f3.jpg>)

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
"""
from django.db import models
from django.contrib import admin

class BankLoan(models.Model):
    loan_id=models.IntegerField(primary_key=True)
    loan_type=models.CharField(max_length=30)
    loan_amt=models.FloatField()
    cust_acno=models.IntegerField()
    cust_name=models.CharField(max_length=50)
    
class BankLoanAdmin(admin.ModelAdmin):
   list_display = ('loan_id','loan_type','loan_amt','cust_acno','cust_name')
from django.contrib import admin

from .models import BankLoan,BankLoanAdmin
admin.site.register(BankLoan,BankLoanAdmin)
"""
## OUTPUT


![alt text](<Screenshot (19).png>)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
