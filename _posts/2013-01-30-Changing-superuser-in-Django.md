---
layout: post
title: "Changing superuser in Django app"
category:
tags: [Django]

meta_description: Changing superuser in Django via shell.
---
When a project is started, Django creates a superuser which has all the controls, similar to Unix superuser. Sometimes you might want to change the superuser in your Django app. At least, I do it time to time. 

First, let's fire the shell. I am hoping that you are using [iPython][1] - the awesome interactive python shell. It's a gem. 

`python manage.py shell`

This will open iPython if it is installed, otherwise normal shell.

And,  
`from django.contrib.auth.models import User`  
`su = User.objects.get(username='username@email.com')`  
`su.set_password('new_password')`  
`su.save()`  

We can replace the Email as well.

[1]: http://ipython.org/