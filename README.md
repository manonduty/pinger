# pinger

There are:
- script pinger.py that fetches ip address list from database, makes ping for each ip and save results to database.
- web application app.py for managing monitoring list and viewing monitoring results

# How to install and use<br>

First, for convinience, create virtual environment. Run following: <br>
$ virtualenv pinger <br>
$ cd pinger <br>
$ source bin/activate <br>
Than install pinger with following steps: <br>

1. clone repository: $ git clone https://github.com/manonduty/pinger
2. go to created directory "pinger": $ cd pinger/
3. run "pip install -r requirements.txt"
4. 
    it creates database pinger_db.sqlite3 (or with the name specified in settings.py)
5. add pinger.py to crontab: <br>
    $ crontab -e <br>
  set to execute pinger.py every minute
7. run web application to manage ip address list and view monitoring results: <br>
    $ python app.py

- At first running app.py or pinger.py will create database file in pinger directory
- At the upper part of the scripts app.py and pinger.py there are some variables that you may change<br>
E.x. name for database, path to ping utility in your Linux pc.
