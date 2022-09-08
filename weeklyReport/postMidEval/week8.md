# Week: 1 August to 7 August
# Coding Period Week 8 Report
[![Generic badge](https://img.shields.io/badge/Status-Done-<>.svg)](https://shields.io/)
[![Generic badge](https://img.shields.io/badge/Last_Updated_(IST)-August_7,_2022-e10b95.svg)](https://shields.io/)

## TL;DR
Create 4 api endpoints for augur-new:
-  create user
-  delete user
-  modify user
-  validate user

I have been using flask-sqlalchemy instead of sqlalchemy; Btw I did not know the shortcomings of using flask_sqlalchemy, good to find out and learn something new😄
as far as I understand converting to sqlalchemy will be small changes but apart from that can we not use the User class already defined in the augur_operations?

## ToDo:
- [Understand API endpoint implementation](https://auth0.com/developers/hub/code-samples/api/flask-python/basic-role-based-access-control)
- Add database commands
- complete the methods for CRUD
- test the endpoints

## Work Done:
- use request instead of response for arguments
- understand User schema
- understand and use engine to connect to the db
- delete user endpoint pseudocode
- sqlalchemy conversion as suggested by Andrew, he also added an admin boolean to the User class defined in the augur_operation_models:

```python
'''
Augur commands for adding regular users or administrative users
Add Regular user command: augur user add <username> <email>
Add Admin command: augur user add <username> <email> --admin 
'''

import os
import click
from werkzeug.security import generate_password_hash
sfrom uuid import uuid4
from sqlalchemy.orm import Session
from augur.applicaton.db.engine import create_database_engine


logger = logging.getLogger(__name__)

#user subcommand
@click.group('user', short_help='Support for adding regular users or administrative users')
def cli():
    pass
@cli.command('add', short_help="Add a new user")
@click.argument("username")
@click.argument("email")
@click.argument("firstname")
@click.argument("lastname")
@click.option(
    "--phone-number", default=None, help="User phone number"
)
@click.option(
    "--admin", is_flag=True, default=False, help="New user has administrator role"
)
@click.password_option(help="Set password")
def add_user(username, email, firstname, lastname, phone_number, admin, password):
    """Add a new user to the database with email address = EMAIL."""

    engine = create_database_engine()
    session = Session(engine)

    if session.query(User).filter(User.login_name == username).first() is not None:
        return click.echo("username already taken")

    if session.query(User).filter(User.email == email).first() is not None:
        return click.echo("email already signed-up")

    user = session.query(User).filter(User.login_name == username).first()
    if not user:
        password = generate_password_hash(password)
        new_user = User(login_name=username, login_hashword=password, email=email, text_phone=phone_number, first_name=firstname, last_name=lastname, admin=admin)
        db.session.add(new_user)
        db.session.commit()
        user_type = "admin user" if admin else "user"
        message = f"Successfully added new {user_type}: {new_user}"
        click.secho(message, bold=True)
        return 0
```

## Random: 
<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Late night debugging sessions👩‍💻 <a href="https://t.co/aOd2S9kE9D">pic.twitter.com/aOd2S9kE9D</a></p>&mdash; Priya Srivastava (@shivikapriya) <a href="https://twitter.com/shivikapriya/status/1555283486705012737?ref_src=twsrc%5Etfw">August 4, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
