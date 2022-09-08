# Week: July 25, 2022 - July 31, 2022
# Coding Period Week 7 Report
[![Generic badge](https://img.shields.io/badge/Status-Done-<>.svg)](https://shields.io/)
[![Generic badge](https://img.shields.io/badge/Last_Updated_(IST)-July_31,_2022-e10b95.svg)](https://shields.io/)

## TL;DR

<b>Approach:</b>
<p>- I was supposed to create API endpoints for integration of login with backend. The API would generate token --> hit HTTPS --> validate user (example for validate). <br>
- This would ultimately use Postgres. So connect to Postgres instead of sqlite.<br>
- Frontend should talk to backend API <--> database.<br>
- User to repo to schema to have 4 endpoints: add, remove, update and validate (passing in hashkey (SSL))<br>
- The updated file structure as per augur-new required me to install augur-new.
<p align="center" style="font-size:25px"> <b> User schema </b> <p>
    
![schema](/project/assets/schema.jpeg)
