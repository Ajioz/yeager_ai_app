# webapp

## getting started with the yeager_ai app

## Requirements

1. python 3.8 above
2. Postgres

## Installation and Setup

## create a postgres database named "project"

```# window user
psql -U postgres
create database project;
```

### create a virtual enviroment and activate

first change directory into yeager_ai

```#bash
cd yeager_ai
```

```# bash- Windows
python -m venv venv
# activate enviroment
. venv/Scripts/activate
```

````
```# Linux
sudo apt-get install python3-venv
python3 -m venv .venv
# activate enviroment
source .venv/bin/activate
````

```# macOS
python3 -m venv .venv
# activate enviroment
source .venv/bin/activate
```

### install requirement

```#bash
cd requirements
pip install -r base.txt
pip install -r local.txt
pip install dj-stripe slippers
```

Note: on installing slippers you need to add it to installed apps under the setting of the entry app point yeager_ai

### before running the app update your password to match your postgres user password

1. locate the base.py file in the config direction and update your password for the postgres user

### Apply Migration

```
python manage.py migrate
```

### Running the app

```#bash
python manage.py runserver
```
