[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Linkedin: Priya](https://img.shields.io/badge/-PriyaSrivastava-blue?style=flat-square&logo=Linkedin&logoColor=white&)](https://www.linkedin.com/in/priyasrivastava730/)
[![Twitter: shivikapriya](https://img.shields.io/twitter/follow/shivikapriya?style=social)](https://twitter.com/shivikapriya)
[![GitHub: Priya730](https://img.shields.io/github/followers/Priya730?label=Follow%20%40Priya730&style=social)](https://github.com/Priya730)
<br>

<h1 align="center"><a href="https://summerofcode.withgoogle.com/programs/2022/projects/YNXT2TFX">Build Access and Entitlements for Hosted version of Augur</a></h1>
<figure>
  <img src="project/chaoss-gsoc.png" align="center">
</figure>
<br>
<p align="center">Check out my <a href="">blog</a> or follow me on <a href="https://twitter.com/shivikapriya">Twitter</a> for more updates.</p>


<p align="center">
  <a href="project/Priya_Srivastava_GSoCproposal_CHAOSS.pdf"> Proposal </a>|
  <a href="meetings/"> Meeting Notes </a>| 
  <a href="description"> Abstract</a> |
  <a href="blogs/">Blogs</a> |
  <a href="#additional-info"> Links</a>
</p>

## CONTENTS
* [Student Developer Info](#student-developer-info-)
* [Project Details](#project-details-)
* [Work](#work-)
<!--* [Activity Reports](#activity-reports-)
* [Case study with CHAOSS](#case-study-with-chaoss-)
* [Implementation Steps](#implementation-steps-)
* [Future Scope](#future-scope-)
* [Learnings](#learnings-)-->

## Student Developer Info: [&uarr;](#contents)
  * Linkedin: [Priya Srivastava](https://www.linkedin.com/in/priyasrivastava730/)
  * Github: [@Priya730](https://github.com/Priya730)
  * Twitter: [@shivikapriya](https://twitter.com/shivikapriya)
  * Blog: [@shivikapriya](https://medium.com/shivikapriya)
  * Mail: [shivikapriya730@gmail.com](mailto://shivikapriya730@gmail.com)
  
## PROJECT DETAILS[&uarr;](#student-developer-info-)
### [Augur](https://github.com/chaoss/augur):
Augur is a software suite for collecting and measuring structured data about free and open-source software (FOSS) communities. We do this by gathering data about project repositories and normalizing that into our data model to provide useful metrics about your project’s health. 

### [augur_view]():

### [augur-new](https://github.com/chaoss/augur/tree/augur-new):


## WORK [&uarr;](#project-details-)
### OBJECTIVES:

#### Primary
- Develop login functionalities so that admins and users can access augur. Populate the tables with information from the user.

- Connect the login to the augur_data.chaoss_user table instead of the sqllite3 database.

- Implement the endpoints necessary for account creation and authentication on the backend.

- Work on the CLI components for creating admin and user accounts.
#### Secondary
- Augur enpoints to be deployed from augur-new. Install augur-new and test the schema creation with SQLAlchemy, and see if it at least creates a schema with all the data integrity protections we engineered into it.

### Objectives Accomplished:
1. #### Installation of augur_view:

2. #### 

## Deliverables
### What Was Done
During these three months I have completed all the essential objectives which includes

| \# | Objectives | PR/Commit/Link | Associated Deliverables | Status |
|----|-------------|----------------|---------|--------|
| 1 | Installation of augur_view | [Link](https://github.com/augurlabs/augur_view/pull/22) |  | Completed |
| 2 | Add user subcommand with username functionality | [Link](https://github.com/chaoss/augur/pull/1912/commits/8ad805770a2a87790b2aab7340021df2b4a71bff) |  | Completed |
| 3 | Add user with email | [Link](https://github.com/chaoss/augur/pull/1912/commits/2f21f567305bdf56dd6f8524ab587114139a5756) | Add user with unique email and username command | Completed |
| 4 | Add Password hashing for the user| [Link](https://github.com/chaoss/augur/pull/1912/commits/1e57f9a073ebcf651eb6b92fe0353d6053bf185f) | Password hashing added | Completed |
| 5 | augur user add <username> <email> subcommand | [PR Link](https://github.com/chaoss/augur/pull/1912) | CLI components for creating admin and user accounts. add_user method takes username as argument as adds it to the table user. | 🟣Completed |
| 6 | Added Create user endpoint | [Link](https://github.com/chaoss/augur/pull/1953/commits/c5a7d1d74a5a2e1c4ac52bd27de9d401f98eead5) | API endpoint for creating user as per user schema (does not use ORM) | Completed |
| 7 | Added Validate user endpoint  | [Link](https://github.com/chaoss/augur/pull/1953/commits/64741898326de4ce215fb18f4f5652a9e149d7a8) | API endpoint for validating user email, username and password(does not use ORM) | Completed |
| 8 | Added remove user endpoint  | [Link](https://github.com/chaoss/augur/pull/1953/commits/23a0cf3540fc93c1105956b4b00839b886e1aa48) | API endpoint for deleting user from database(does not use ORM) | Completed |
| 9 | Added update user endpoint  | [Link](https://github.com/chaoss/augur/pull/1953/commits/a9634068e5e2b0f9d62a15ebc68c699474050f3f) | API endpoint for updating user details like email, username and password.(does not use ORM) | Completed |
| 10 | User create endpoint ORM | [Link](https://github.com/chaoss/augur/pull/1953/commits/a4c049334efe86d678e99ffe09b947e43b9e07bb) | API endpoint for creating user using ORM | Completed |
| 11 | User validate endpoint ORM  | [Link](https://github.com/chaoss/augur/pull/1953/commits/ea5e72ff52b757ca836aa4a1a0b80b2c5d110252) | API endpoint for validating user using ORM | Completed |
| 12 | User remove endpoint ORM   | [Link](https://github.com/chaoss/augur/pull/1953/commits/557d966510924215ca43ff3d03873b580bcc3cc5) | API endpoint for remove user using ORM | Completed |
| 13 | User update endpoint ORM   | [Link](https://github.com/chaoss/augur/pull/1953/commits/2cf9afe432cc853e79f1ca68c9ba69e7d48ebbae) | API endpoint for updating user using ORM | Completed |
| 14 | --  | [Link]() |  | Completed |


## ACTIVITY REPORTS [&uarr;](#work-)

### Community Bonding - May 20th to June 12th, 2022 [&uarr;](#activity-reports-)
 |Week Number | Blog| Weekly Summary|
| ---   | --- | ---| 
**WEEK 0**|[Accepted for GSoC'22](*)| |
**WEEK 1**|[Community Bonding week 1](https://medium.com/@shivikapriya730/google-summer-of-code-community-bonding-week-1-e2f07644dc98) | [Weekly report](weeklyReport/communityBonding/Week1.md)|
**WEEK 2** | [Community Bonding week 2]()|  [Weekly report]()|
**WEEK 3** | [Community Bonding week 3]() |[Weekly report]()|

### Coding Period 1 - June 13th to July 11, 2022 [&uarr;](#activity-reports-)
|Week Number | Blog| Weekly Summary|
| ---   | --- | ---|
**WEEK 1** |[Coding Period 1 week 1]() |[Weekly report]()
**WEEK 2** |[Coding Period 1 week 2]() | [Weekly report]()
**WEEK 3** |[Coding Period 1 week 3]() | [Weekly report](weeklyReport/codingPeriod/week3.md)
**WEEK 4** | [Coding Period 1 week 4]() |[Weekly report]()

### Coding Period 2 - July  to July th, 2022 [&uarr;](#activity-reports-)
 |Week Number | Blog| Weekly Summary|
| ---   | --- | ---|
**WEEK 5** |[Coding Period 2 week 5]() |[Weekly report]()
**WEEK 6** |[Coding Period 2 week 6]() | [Weekly report]()
**WEEK 7** |[Coding Period 2 week 7]() | [Weekly report]()
**WEEK 8** | [Coding Period 2 week 8]() |[Weekly report]()

### Coding Period 3 - July  to Aug , 2022 [&uarr;](#activity-reports-)
|Week Number | Blog| Weekly Summary|
| ---   | --- | ---|
**WEEK 9** |[Coding Period 3 week 9]() |[Weekly report]()
**WEEK 10** |[Coding Period 3 week 10]() | [Weekly report]()
**WEEK 11** |[Coding Period 3 week 10]() | [Weekly report]()
**WEEK 12**|[Coding Period 3 week 11]() | [Weekly report](https://github.com/Priya730/GSoC22/blob/main/weeklyReport/postMidEval/week12.md)

<!--

## Project Abstract

### Mentors

## Project Updates

  -->
## Additional Info
<b>This repository will be regularly updated with blogs and meetings summaries during the project.</b>
    
- [GSoC'22 Project Proposal](project/Priya_Srivastava_GSoCproposal_CHAOSS.pdf)
- [Microtasks](https://github.com/Priya730/chaoss-micro-task)
- [Project Link](https://summerofcode.withgoogle.com/programs/2022/projects/YNXT2TFX)
