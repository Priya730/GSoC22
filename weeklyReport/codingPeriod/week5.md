# Week: 11 July to 17 July
# Coding Period Week 5 Report
[![Generic badge](https://img.shields.io/badge/Status-Done-<>.svg)](https://shields.io/)
[![Generic badge](https://img.shields.io/badge/Last_Updated_(IST)-July_17,_2022-e10b95.svg)](https://shields.io/)

## TL;DR
adduser(username) methods works for given argument username and email. Solved the error with _multicommand.py! 
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
- Also, for the command to be implemented, changes need to be made in the get_command method of  _multicommand.py, but I am not able to understand the way module variable works right now (see comment)

![logging error](/project/assets/loggingerror.png)

- So what is happening is, the module you are importing (in this case util.py and user.py) have a ModuleNotFoundError somewhere, and this error is getting thrown, but it is getting caught by the exception clause on line 31 and nothing is being printed. To work on debugging this I simply replaced the pass in the exception block with print(f"Error: {e}"). Another good, and in my opinion, better way to debug this is to run both user.py and util.py with python3 user.py and python3 util.py. This will throw any error that may will be thrown when trying to import the module on line 28

- So the problem was due to circular imports.  application.py has these imports: import logging
from logging import FileHandler, Formatter
And cli/logging.py was causing circular import error

-it was named logging.py since the python library is called logging. 
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
<blockquote class="twitter-tweet"><p lang="en" dir="ltr">solved the bug after struggling with it for a long time. happy now😌 <a href="https://t.co/MzR9YH1D3I">pic.twitter.com/MzR9YH1D3I</a></p>&mdash; Priya Srivastava (@shivikapriya) <a href="https://twitter.com/shivikapriya/status/1546902055620554754?ref_src=twsrc%5Etfw">July 12, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>