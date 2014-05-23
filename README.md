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
* python-dev (required by numpy)
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

In your local repository create a settings_local.py file which overwrites DEBUG to True (in development mode). 

```sh
touch settings_local.py
gedit settings_local.py
```
```python
DEBUG = True
```

Run server with the following command

```sh
./manage runserver 127.0.0.1:8000
```

