# Heroku-Web-Apps
Implementing Django in a dockerfile to manage various data related apps (projects) and web based apps (blog) and launching it on Heroku 

# Contents

+ Django Web App
    + [Motivation](#motivation)
    + [Docker](#dockerfile)
    + [Website](defunsm.ml)
    + Blog
    + Projects (Each being an App in Django)
        + Forest Productivity Metrics
        + Eve Online Market Price DashBoard
        + (Miscellanous other projects)

# Motivation
> **Problem Statement:** Integrating various web apps from various repos into one repo.

# Dockerfile

``` Dockerfile
# syntax=docker/dockerfile:1
FROM python:3
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1
WORKDIR /code
COPY requirements.txt /code/
RUN pip install -r requirements.txt
COPY . /code/
```


# Credits
https://docs.docker.com/desktop/windows/install/
https://docs.docker.com/samples/django/
https://docs.djangoproject.com/en/4.0/
https://12factor.net/