# Week: 11 July to 17 July
# Coding Period Week 5 Report
[![Generic badge](https://img.shields.io/badge/Status-Done-<>.svg)](https://shields.io/)
[![Generic badge](https://img.shields.io/badge/Last_Updated_(IST)-July_17,_2022-e10b95.svg)](https://shields.io/)

## TL;DR
adduser(username) methods works for given argument username and email.
# TODO:
- [x] avoid duplicates (Each user should have a unique username and email)
- [x] fix password hashing
- [x] Added generate password hash
- [x] changed bold output
# Possibilities:
- email argument option update
- validate email address
- use a different model for admin, will be easy to differentiate between user and admin
# Important: 
- [x] changes need to be made in multicommad.py for command to implement
# Problems:
- [x] bycrypt password (sqlalchemy.exc.IntegrityError: (sqlite3.IntegrityError) NOT NULL constraint failed: user.password_hash
[SQL: INSERT INTO user (username, email, password_hash, admin, public_id) VALUES (?, ?, ?, ?, ?)])
- email validation
# Ideas and possibilities:
- validate username 
```
username = field.data
        if len(username) < 3:
            raise ValidationError(
                _('Username must be at least 3 characters long'))
        valid_chars = 'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789-._'
        chars = list(username)
        for char in chars:
            if char not in valid_chars:
                raise ValidationError(
                    _("Username may only contain letters, numbers, '-', '.' and '_'"))
```
- validate password (Ensure that passwords have at least 6 characters with one lowercase letter, one uppercase letter and one number.)
    ```
        password = list(field.data)
        password_length = len(password)
        lowers = uppers = digits = 0
        for ch in password:
            if ch.islower(): lowers += 1
            if ch.isupper(): uppers += 1
            if ch.isdigit(): digits += 1

        is_valid = password_length >= 6 and lowers and uppers and digits
        if not is_valid:
            raise ValidationError(
                _('Password must have at least 6 characters with one lowercase letter, one uppercase letter and one number'))
    ```

# Questions:
- UserMixin benefits? will it help me in authorisation?
- Flask-Login instead of Flask-User grrr. What's the difference between the two. They seem almost identical. 

- Not able to find out the difference and decide which one to use.

- Plus, usermanager (flask-user) is giving me errors (a lot of them!)

# Random:
- Learnt more about good commit messages. ;)