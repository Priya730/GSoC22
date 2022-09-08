# Week: August 22, 2022 - August 28, 2022
# Coding Period Week 10 Report
[![Generic badge](https://img.shields.io/badge/Status-Done-<>.svg)](https://shields.io/)
[![Generic badge](https://img.shields.io/badge/Last_Updated_(IST)-August_28,_2022-e10b95.svg)](https://shields.io/)

## TL;DR
Convert api to ORM

## Work:
PR review by mentor:
`The user endpoints should use the ORM to communicate with the database, consistent with the rest of the application.

Additionally the function decorators are not properly implemented on the endpoints. However, this regression was introduced in an external commit from another branch, and should be fixed there prior to merging.`

- I need to use ORM, significance: what if I change the name of table from user to something else, the code will not work. I therefore should use objects!
- Understand ORM in detail and implement alongside.
- user = session.query(User).filter(User.login_name == username).first()
- For update_user() I've currently used  if conditions like:

```if(email is not None):
      ...update email...
if(password is not None):
      ...update password...
```