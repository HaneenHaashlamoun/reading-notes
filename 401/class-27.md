# Django Models

![model](https://res.cloudinary.com/practicaldev/image/fetch/s--lVrX4JdY--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/abvbys3c58tmswhw6vbj.jpg)

## Models: 
are the structure of stored data, because  Django web applications access and manage data through Python objects referred to as models.

• When designing your models it makes sense to have separate models for every "object"
(a group of related information). In this case, the obvious objects are books, book instances, and authors.

## The basics:

• Each **model** is a Python class that subclasses django.db.models.Model.
• Each **attribute** of the model represents a database field.
• With all of this, Django gives you an automatically-generated database-access API; see Making queries.

## Model definition
example :
This example model defines a Person, which has a first_name and last_name:

first_name and last_name are fields of the model. Each field is specified as a class attribute, and each attribute maps to a database column

```
from django.db import models

class Person(models.Model):
    first_name = models.CharField(max_length=30)
    last_name = models.CharField(max_length=30)  
```
       
## Fields
A model can have an arbitrary number of fields, of any type — each one represents a column of data that we want to store in one of our
database tables. Each database record (row) will consist of one of each field value. Let's look at the example:

```
my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')
```
## Field types : 

Each field in your model should be an instance of the appropriate Field class. Django uses the field class types to determine a few things:

• The column type, which tells the database what kind of data to store (e.g. INTEGER, VARCHAR, TEXT).

• The default HTML widget to use when rendering a form field `(e.g. <input type="text">, <select>).`
  
• The minimal validation requirements, used in Django’s admin and in automatically-generated forms. 
         
## Django admin site :  

![admin](https://djangobook.com/wp-content/uploads/admin_login.png)

 • The Django admin application can use your models to automatically build a site area that you can use 
  to create, view, update, and delete records. 
  
  • The admin application can also be useful for managing data in production, depending on the type of website.
  
## Registering models 

 ```
 from django.contrib import admin
# Register your models here.
 ```
 
 ![admin](https://assets.digitalocean.com/articles/eng_python/django/django-admin-models-added.png)
 Creating a superuser
 ```
 python3 manage.py createsuperuser
 ```