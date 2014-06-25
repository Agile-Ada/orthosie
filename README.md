License
=======

    Copyright 2013 Jack David Baucum

    This file is part of Orthosie.

    Orthosie is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    Orthosie is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with Orthosie.  If not, see <http://www.gnu.org/licenses/>.

Orthosie is licensed under the GPLv3. The details of this license can be viewed at http://gplv3.fsf.org/

About
=====
Orthosie is a point of sale system written in Python using the Django framework.
Orthosie supports Python 3 and Django 1.6.

Supported Systems
=================
Orthosie should work on any operating system and any hardware that can run python3 and the Django 1.6. It is only tested to work with Chrome/Chromium and Midori web browsers. Patches and pull requests to fix bugs in any other browsers are always welcome as long as they don't add any undo clutter to the codebase.

Install
=======
These instructions are for debian-based versions of GNU/Linux.

Require Packages
----------------
    sudo apt-get install python3 python3-setuptools git 

Django
------
    wget https://www.djangoproject.com/m/releases/1.6/Django-1.6.tar.gz
    tar xzvf Django-1.6.tar.gz
    cd Django-1.6.tar.gz
    sudo python3 setup.py install

Django-REST-Framework
---------------------
Orthosie uses Django REST Framework, which can be grabbed from http://django-rest-framework.org/

    git clone https://github.com/tomchristie/django-rest-framework.git
    cd django-rest-framework
    sudo python3 setup.py install

Orthosie
--------
    cd ~
    git clone https://github.com/maxolasersquad/orthosie.git

SQLite Database
---------------
Getting Orthosie running for the first time requires we setup the sqlite database file.
If you have a different database you want to use, refer to the django documentation at https://docs.djangoproject.com/en/1.6/ref/databases/

    cd orthosie
    python3 manage.py syncdb

Running
=======
To run the test server cd in to the orthosie directory and run the following.

    python3 manage.py runserver

At this point you can browse to http://127.0.0.1:8000/register/ to see the register.

This server should only be used for testing your setup and maybe even an initial configuration. For your production setup you should use nginx, Apache, or any other webserver of your choosing.

Nginx
-----
The following article explains setting up nginx on Ubuntu to connect to a django application.
http://grokcode.com/784/

Apache2
-------
The following article explains setting up Apache2 on Ubuntu to connect to a django application.
https://www.digitalocean.com/community/articles/using-mod_wsgi-to-serve-applications-on-ubuntu-12-04

Adding Inventory
================
You can modify existing inventory from http://127.0.0.1:8000/inventory/

Running the Register
====================
The register is located at http://127.0.0.1:8000/register/
You should be able to ring up this product. Note that during the ring the UPC checksum is needed for a ring to go through properly, so you will need to input '008274000061' for the ring to work.

Other Licenses
==============

## Font-Awesome
Licensed SIL OFL 1.1 and MIT. More information at http://fontawesome.io/license/

## Bootstrap
Licensed MIT. More information at https://github.com/twbs/bootstrap/blob/master/LICENSE

## jQuery
Licenses MIT. More information at https://jquery.org/license/
