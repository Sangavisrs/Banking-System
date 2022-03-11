# Online Banking System V2.0.2

This is an Online Banking Concept created using Django Web Framework.


## Features

* Create Bank Account
* Deposit & Withdraw Money
* Bank Account Type Support
* Interest calculation depending on the Bank Account type
* Using date we can check transaction report 
* We can check balance after every transaction in the Transaction Report
* Calculate Monthly Interest Using Celery Scheduled tasks
* More efficient & user-friendly

## Project Installation

To setup a local development environment:

Create a virtual environment in which to install Python pip packages. With [virtualenv](https://pypi.python.org/pypi/virtualenv),
```bash
virtualenv venv            # create a virtualenv
source venv/bin/activate   # activate the Python virtualenv 
```

or with [virtualenvwrapper](http://virtualenvwrapper.readthedocs.org/en/latest/),
```bash
mkvirtualenv -p python3 {{project_name}}   # create and activate environment
workon {{project_name}}   # reactivate existing environment
```

cd banking-system
```

Install development dependencies,
```bash
pip install -r requirements.txt
```

Migrate Database,
```bash
python manage.py migrate
```

Run the web application locally,
```bash
python manage.py runserver # 127.0.0.1:8000
```

Create Superuser,
```bash
python manage.py createsuperuser
```

Run Celery
(Different Terminal Window with Virtual Environment Activated)
```bash
celery -A banking_system worker -l info

celery -A banking_system beat -l info
```
