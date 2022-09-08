# Week: August 8, 2022 - August 14, 2022
# Coding Period Week 9 Report
[![Generic badge](https://img.shields.io/badge/Status-Done-<>.svg)](https://shields.io/)
[![Generic badge](https://img.shields.io/badge/Last_Updated_(IST)-August_14,_2022-e10b95.svg)](https://shields.io/)

## TL;DR
Busy week, lot of error solving, coding and testing involved! Read ahead to find out:

## Work Done:
- test api endpoints: 
To test it, need to instal augur. Then run `augur backend start --disable-collection` to start the api. Then call `http://localhost:5000/api/unstable/user/remove?user=Brandon` to remove the user Brandon
- I am not able to resolve this particular error message, it is related to bad engine connection...
```Exception during reset or similar
Traceback (most recent call last):
  File "/home/priya/.virtualenvs/augur_env/lib/python3.8/site-packages/sqlalchemy/pool/base.py", line 697, in _finalize_fairy
    fairy._reset(pool)
  File "/home/priya/.virtualenvs/augur_env/lib/python3.8/site-packages/sqlalchemy/pool/base.py", line 893, in _reset
    pool._dialect.do_rollback(self)
  File "/home/priya/.virtualenvs/augur_env/lib/python3.8/site-packages/sqlalchemy/engine/default.py", line 558, in do_rollback
    dbapi_connection.rollback()
psycopg2.OperationalError: SSL SYSCALL error: EOF detected 
```
- the method and ssl are in place, nothing wrong with that. Unsupported method was my bad.
- As far this message is concerned I encounter it when I try to make any changes, I think that's what Exception during reset also means
- for the error the simplest thing to do was to retest the api after making changes to the code.

## Problems faced:
- branch change and reorganising of file structure in augur-new got me confused. 

![image schema](project/assets/filestructure.png)

- faced problems because schema was not properly created upon installation of augur-new. solved by: `Creating a new database and calling augur db create-schema would be the easiest thing to do`
- solved installation errors 
- Update: 
Works now🥳
So I found out this... In application/cli/config-db.py there is a typo letter 's' on line 35.