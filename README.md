ACM Multimedia Challenge 
======================

This project contains the open source code developed by Klewel and Idiap and representing talk-level and segment-level recommendations in a graph. 


http://acmmm13.org/submissions/call-for-multimedia-grand-challenge-solutions/mediamixervideolectures-net-grand-challenge/

Acknowledgements
---------------------------

Aroles SNF
InEvent EU Project

Prerequisite
----------------

* python2.7
* python-pip

```sh
sudo aptitude install python2.7 python-dev python-pip
```

Run pip to resolve dependencies with command

```sh
sudo pip install -r requirements.txt
```


Setup
-------------

In your local repository create a settings_local.py file which overwrites DEBUG to True (in development mode) and add a secret key like in below example :

```sh
touch settings_local.py
gedit settings_local.py
```

with content :
```python
DEBUG = True
SECRET_KEY = "fdlet034msd09w4jfqjvl094ujopfaoo43jfa"
```

Initialize your static files :
```sh
./manage.py collectstatic
```

Run server with the following command
```sh
./manage runserver 127.0.0.1:8000
```

Setup production
----------------

In production if DEBUG don't need to be set, you have to specify allowed hosts in your settings_local.py (if not sepcified you will receive an error 400) like in below example :

```python
SECRET_KEY = "92jrlff24lujlkdj240plkjar4tgjasdf"
ALLOWED_HOSTS = [ "www.example.com" ]
```
