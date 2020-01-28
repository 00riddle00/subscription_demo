
Manual setup guide
----------------

##### go to projects root dir (your choice)
`cd {{ path }}/`

##### set VENV variable
`export VENV=$(pwd)/env`

##### initialize virtual environment
- `virtualenv -p python3 $VENV`
or 
- `python3 -m venv $VENV`

##### install setuptools
`$VENV/bin/pip3 install --upgrade pip setuptools`

##### clone the source from git
`git clone https://github.com/00riddle00/subscription_demo.git app/`

##### go to projects dir
`cd app/`

##### install all the packages by the pyramid app
`$VENV/bin/python3 setup.py develop`

##### initialize database 
`$VENV/bin/initialize_subscriptions_db development.ini`

##### run development server
`$VENV/bin/pserve development.ini --reload`

##### view the project 
`http://localhost:6543`
