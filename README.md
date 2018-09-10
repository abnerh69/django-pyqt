# pyqt5-django-orm
Starter project and directory structure to use PyQt5 with Django 2 ORM for *nix systems
Tested wil PyQt5.11 and Django 2.1

Not that you need PyQt5 and Django to be already installed
#Installation
>Clone the repo then run:
`sudo ./setup.py`

## Usage
##### Start new project using

`pyqt5-admin --startproject proj_name destination`


Project Structure:

```.
├── apps  -> where django apps go
├── forms -> where Qt *.ui files go
├── viewManagers -> your views controllers go here
├── views -> where pyuic5 generated *.py files go
├── __main__.py -> start point for your application
├── manage.py 
├── settings.py

```
#### Django Commands
##### Create a new django app inside the apps directory

`python3 manage.py.py --startapp appName`

##### Add appName to INSTALLED_APPS in settings.py

`INSTALLED_APPS = ["apps.appName",]`

##### To Migrate your models
`python3 manage.py --migrate [app1, app2, ...]`

Note that leaving apps blank will try to migrate all apps

#### PyQt5 Commands

##### Convert `*.ui` files to `.py` files using `pyuic5` assuming pyuic5 is on path

`python3 manage.py --uic [file1.ui, file2.ui]`

Note that leaving files blank will compile all UI files inside forms directory
#### Using Pyinstaller 
`python3 manage.py --deploy`

#### Start coding !
Now you can start using your model inside your application
