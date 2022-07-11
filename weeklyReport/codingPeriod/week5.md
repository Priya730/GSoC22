# Week: 11 July to 17 July
# Coding Period Week 5 Report
[![Generic badge](https://img.shields.io/badge/Status-In_Progress-<>.svg)](https://shields.io/)
[![Generic badge](https://img.shields.io/badge/Last_Updated_(IST)-July_11,_2022-e10b95.svg)](https://shields.io/)

## TL;DR
adduser(username) methods works for given argument username.
# TODO:
- [x] avoid duplicates (Each user should have a unique username and email)
- [] fix password hashing
- [] validate email address
- [] use a different model for admin, will be easy to differentiate between user and admin
# Problems:
- bycrypt password (sqlalchemy.exc.IntegrityError: (sqlite3.IntegrityError) NOT NULL constraint failed: user.password_hash
[SQL: INSERT INTO user (username, email, password_hash, admin, public_id) VALUES (?, ?, ?, ?, ?)])
- email validation
# Questions:
- UserMixin benefits? will it help me in authorisation?
# Random:
- Learnt more about good commit messages. ;)