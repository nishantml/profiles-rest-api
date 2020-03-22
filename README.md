# Profiles REST API

Profiles REST API course code.

- Setup up Vagrant development serer

`` vagrant init ubuntu/bionic64 ``

- above command will initialise our project with the new vigrant file

``vagrant up // to start the vagrant server for our project  ``

``vagrant ssh   // to connect to the vagrant server ``
- By default local system file is not sync on our development virtual server and as we know our code is on local server and vagrant work by creating a synchronised directory on our vagrant server.


`` cd vagrant // this commend will show you all local file which is on server``  

- Now how we can create python virtual environment so we can install all the dependencies such as python and the django rest framework
- we will will create virtual environment on vagrant server
`` python -m venv ~/env //this will create new virtual environment for our project `` 
- above is the set of files and this is the dir where it installs all the dependencies when we install them with the python package manager
- we need to activate and deactivate the virtual environment. So when you activated on virtual environment then all of the dependencies that you run in the Python application will be pulled from the virtual environment instead of the base os
``source ~/env/bin/activate // this will activate the python environment`` 
``deactivate // to deactivate the virtual environment`` 
- In the we are using to packages 
    1. Django
    2. Django Rest Framework

- to manage all the dependencies we will use requirment.txt and we will put all the packages in it and the to install type the command 

``pip install -r requirements.txt // this will install all the packages ``

- Now after setting up all our environment we can create project 

``django-admin.py startproject project_name . ``

- . is specifying the path where we want to create the project dir
> Inside Django project we can create different application i.e one project can consists of one or more sub applications within the in projects.

``python manage.py startapp profiles_api`` 
- TO run and test our application type below command

``python manage.py runserver 0.0.0.0:8000``

``python manage.py makemigrations app_name`` // to create a migration file using django cli

`` python manage.py migrate`` //this will run all the migrations in our projects 

- to access the admin panel http://127.0.0.1:8000/admin/ type superuser cred 

- We have added serializer to a view which allow us (it is the features from the django rest framework) to easily convert data input into Python objects and vice versa its kind a similar to the django form. 
