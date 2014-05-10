django-webmaster
================

A very basic tool to keep track of your domain names and servers.

Picture the scene: you own and/or manage multiple domain names, purchased from a number of different registrars. You use a few different DNS and web hosting providers and have multiple servers dotted around the globe. Keeping track of all that is a pain. If a server, or any other link in the above chain goes down, how can you quickly find what is hosted where? How many of your clients are affected? You can create a complex spreadsheet and employ various filters to do all that for you, but this is hopefully a little less painful.

Unlike most Django apps which are designed to add functionality to your project and speed up your development process, Django-Webmaster is a standalone tool which runs within the Django Admin site.

Documentation
-------------

Proper docs are to follow, but in short:

 - pip install django-webmaster
 - Add 'webmaster' to your INSTALLED_APPS in your settings.py
 - python manage.py syncdb (or python manage.py migrate on Django 1.7+)
 - Login in to the admin site (if you have a lot of domains, using [Grappelli][1] is highly recommended)
 - Add one or more entry to each of "DNS Provider", "Domain Registrar" and "Hosting Provider".
 - Add your first "Server" (details of a VPS for example) and "Domain Name" (e.g. `example.com`)
 - Finally, add your first "Subdomains" (e.g. `www.example.com`, `static.example.com`)

Once you'd added a few  usefulness of the project comes by using filtering and sorting in the "Domain Names" and "Subdomains" sections.

A disclaimer: this project is only as useful as the data you give it. The initial data-entry is a bind, but after that its pretty easy to keep it all up-to-date.

  [1]: http://grappelliproject.com/
