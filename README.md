# How To Install Django In Mac
src: https://appdividend.com/2018/03/28/how-to-install-django-in-mac/#Step_1_Install_Python_on_Mac


## 1) Set up virtualenv
```
virtualenv ~/virtualenv
```


## 2) Launch virtualenv
```
source ~/virtualenv/bin/activate
```

## 3) Requirements
src: https://gist.github.com/Siltaar/9441a525d3a580311035fa2f3f431baa

[`requirements.txt`](requirements.txt) file installs all the necessary `modules` for your project:


```
cd ~/virtualenv
sudo pip3 install -r ~/virtualenv/requirements.txt
```


## 4) Launch Django project
```
cd ~/virtualenv/rioanalytics
python3 ~/virtualenv/rioanalytics/manage.py runserver
```


## 5) Creating an admin user
src: https://docs.djangoproject.com/en/2.2/intro/tutorial02/
```
cd ~/virtualenv/rioanalytics
python3 ~/virtualenv/rioanalytics/manage.py createsuperuser
Username:
Email address:
Password:
```


## 6) Extract Sqlite Database
src: https://stackoverflow.com/questions/3034910/whats-the-best-way-to-migrate-a-django-db-from-sqlite-to-mysql
```
cd ~/virtualenv/rioanalytics
python3 ~/virtualenv/rioanalytics/manage.py dumpdata > ~/virtualenv/rioanalytics/datadump.json
```
