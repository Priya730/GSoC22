# Week: 18 July to 24 July
# Coding Period Week 6 Report
[![Generic badge](https://img.shields.io/badge/Status-In_Progress-<>.svg)](https://shields.io/)
[![Generic badge](https://img.shields.io/badge/Last_Updated_(IST)-July_17,_2022-e10b95.svg)](https://shields.io/)

## TL;DR
PR ready to merge, sent for review.
University begins on 25 July, this week was not very productive due to travel and reallocation.

## ToDo:
- Do i need role based authorisation?
- [Understand API endpoint implementation](https://auth0.com/developers/hub/code-samples/api/flask-python/basic-role-based-access-control)

## [Flask-Permission](https://github.com/raddevon/flask-permissions)
```
# Import Flask, Flask-SQLAlchemy, and maybe Flask-Login
from flask import Flask
from flask.ext.login import LoginManager, current_user
from flask.ext.sqlalchemy import SQLAlchemy

# Import the Permissions object
from flask.ext.permissions.core import Permissions

db = SQLAlchemy()

app = Flask(__name__)
app.config.from_object('config')

db.init_app(app)
with app.test_request_context():
    db.create_all()

# Flask-Login
login_manager = LoginManager()
login_manager.init_app(app)

# Now, initialize a Permissions object. 
perms = Permissions(app, db, current_user)
```