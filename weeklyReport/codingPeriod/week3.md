# Week: 27 June to 3 July
# Coding Period Week 3 Report
[![Generic badge](https://img.shields.io/badge/Status-Done-<>.svg)](https://shields.io/)
[![Generic badge](https://img.shields.io/badge/Last_Updated_(IST)-July_3,_2022-e10b95.svg)](https://shields.io/)

## TL;DR
adduser(username) methods works for given argument username.

## Progress till now:
- add_user method takes username as argument as adds it to the table user.
Mentoring session notes: (1 July 2022)
 - Using sqlite at the moment will have to make changes to connect to the API endpoints. Possible solutions: import UserManager as um, make changes accordingly to the methods.
 - Suggestions received: 
    - look at the other arguments that might be important to add a user.
    - delete user command not necessary at this point of time.
    - update user on hold.
 - As per suggestion, will add email, password (+ password hashing), admin flag
## Possibilities of the task:
- Recheck the _multicommand.py methods
- After login user level permissions can include methods like um.getuserrepos()

## Questions and Next Steps:
- Access to augur databse (Soln: will be solved by the API endpoints, check branch [andrew_dev](https://github.com/chaoss/augur/tree/andrew-dev)
- [ ] Understand the api endpoints part
- [x] add admin flag
- [ ] add the user subcommand from the multicommand.py 
- [ ] next steps will be admin and user permissions
