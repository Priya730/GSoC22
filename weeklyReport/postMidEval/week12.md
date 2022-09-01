# Week: 29 August to 2 September
# Coding Period Week 12 Report
[![Generic badge](https://img.shields.io/badge/Status-Done-<>.svg)](https://shields.io/)
[![Generic badge](https://img.shields.io/badge/Last_Updated_(IST)-September_1,_2022-e10b95.svg)](https://shields.io/)

## TL;DR
Corrected the function decorator for the api endpoints.

## Progress till now:
- The [PR](https://github.com/chaoss/augur/pull/1953) was reviewed by my mentors and I received feedbacks.
- The PR was not compiling because of the decorator `server.app.route`. This was through previous commits which I pulled and added the database code. 

- The regression was introduced in https://github.com/chaoss/augur/commit/90a6c88121cde1788bf13fc627bb8e9a7f38ee80

- In order to fix the decorators, I appended the call to `server.app.route` with a `@`