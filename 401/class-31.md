# Django REST Framework & Docker
![Django](https://camo.githubusercontent.com/f20c8bc36d15016a57ca496f646181067a23e515c94484a4cf43c32e93752dc1/68747470733a2f2f692e696d6775722e636f6d2f735a5a674577712e6a7067)
A Beginner’s Guide to Docker

- With Docker it doesn’t matter if you are using a Mac, Windows, or Linux computer anymore. The entire development environment is isolated: programming language, software packages, databases, and more.

- With Docker we now longer have to mess around with virtual environments. We can faithfully reproduce a production environment locally. And Docker can be shared among team members so everyone is working on the same setup. Wins all around.

## Linux Containers

![Linux Containers](https://www.redhat.com/cms/managed-files/virtualization-vs-containers.png)

- Docker is really just Linux containers which are a type of virtualization.

- Virtualization has its roots at the beginning of computer science when large, expensive mainframe computers were the norm. How could multiple programmers use the same single machine? The answer was virtualization and specifically virtual machines which are complete copies of a computer system from the operating system on up.

- If you rent space on a cloud provider like AWS they are typically not providing you with a dedicated piece of hardware. Instead you are probably sharing a physical server with hundreds or even thousands of other clients.

- What’s the downside to a virtual machine? Size and speed. A typical guest operating system can easily take up 700MB of size. So if one physical server supports three virtual machines, that’s at least 2.1GB of disk space taken up along with separate needs for CPU and memory resources.

## Containers vs Virtual Environments

![cvsve](https://www.simplilearn.com/ice9/free_resources_article_thumb/docker-vm.JPG)

- If you are a Python programmer (like me) a common question at this point is, what about virtual environments? How do they differ from containers?

- Virtual environments are used to isolate Python software packages locally. We can create an isolated box for individual projects so one can use Python 2.7 and Django 1.5 while another can use Python 3.5 and Django 2.1 on the same computer. Virtual environments are great.

- But…virtual environments can only isolate Python packages. They still rely on a global, system-level installation of Python albeit they can refer to the proper version. So when we use Python 2.7 in a project, we’re pointing to an installation of Python 2.7 on the computer itself, not actually within the virtual environment.

- Also we can’t run a production database or other services within virtual environments so compared to Docker containers they are far more limited.

## Install Docker
- Docker Compose is an additional tool that is automatically included with Mac and Windows downloads of Docker. However if you are on Linux, you will need to add it manually. You can do this by running the command sudo pip install docker-compose after your Docker installation is complete.

- To confirm Docker installed correctly we can run our first command docker run hello-world

## Images and Containers
Images and containers are the two fundamental concepts to grasp when you start with Docker. An image is a snapshot in time of what a project contains. A container is a running instance of the image.

When we ran hello-world we used an official Docker image. We did not have to create the image ourself. But typically we will create custom images and we do so using a Dockerfile. We also will use docker-compose.yml files to run the containers.

## A baking analogy we can use here is as follows:
- A Dockerfile is the recipe for a cake
- An image is a snapshot of the recipe at a given time
- A docker-compose.yml says how to make the cake
-And the container is the actual, baked cake

## Conclusion
- Docker is a way to run Linux containers
- Containers are a lightweight alternative to Virtual Machines
- Dockerfile is a list of instructions for creating an image
- Images are made up of one or more layers
- Containers are a running instance of an image
- docker-compose.yml controls how to run the container
- Containers are stateless and ephemeral in nature. We can link the local filesystem via volumes but things become more - complex with databases


## Library Website and API
Django REST Framework works alongside the Django web framework to create web APIs. We cannot build a web API with only Django Rest Framework; it always must be added to a project after Django itself has been installed and configured.

The most important takeaway is that Django creates websites containing webpages, while Django REST Framework creates web APIs which are a collection of URL endpoints containing available HTTP verbs that return JSON.

To illustrate these concepts, we will build out a basic Library website with traditional Django and then extend it into a web API with Django REST Framework.

The files have the following roles:

- init.py is a Python way to treat a directory as a package; it is empty 
- asgi.py stands for Asynchronous Server Gateway Interface and is a new option in Django 3.0+
- settings.py contains all the configuration for our project
- urls.py controls the top-level URL routes
- wsgi.py stands for Web Server Gateway Interface and helps Django serve the eventual web pages
- manage.py executes various Django commands such as running the local web server or creating a new app.
- admin.py is a configuration file for the built-in Django Admin app
- apps.py is a configuration file for the app itself
- the migrations/ directory stores migrations files for database changes
- models.py is where we define our database models
- tests.py is for our app-specific tests
- views.py is where we handle the request/response logic for our web app
- A serializer : translates data into a format that is easy to consume over the internet, typically JSON, and is displayed at an API endpoint