---
layout: post
title: "Background processes in django project with celery"
category:
tags: [programming, django, celery]

meta_description: Worker process with celery
---
This is something new we did in our django project. We wanted to archive the big media files and keep it somewhere in server. So whenever an user wants to download them, we could point to the archived files.

We chose to run worker process in background. And running the worker process in advance adds a viry reasonable UX advantage. There is [Celery Project][1] for this very thing.

From their own project:

> Celery is an asynchronous task queue/job queue based on distributed message passing. It is focused on real-time operation, but supports scheduling as well.

The project has really good guides to get started. And running background processes as above is very straight forward. For more details on how to use it with django project, refer this [First steps with Django][2]


[1]: http://celeryproject.org/
[2]: http://docs.celeryproject.org/en/latest/django/first-steps-with-django.html