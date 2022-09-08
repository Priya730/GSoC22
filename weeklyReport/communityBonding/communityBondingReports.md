Refer blog for updates:
* **May 21 - May 28 2022**
[Week1 Medium Blog](https://medium.com/@shivikapriya730/google-summer-of-code-community-bonding-week-1-e2f07644dc98)

* **May 29 - June 5, 2022**
- Setting up augur_view following the documentation.
- Read about access, authorisation, augur and augur schema.
- Read about SQL Alchemy better and the advantages of SQL Alchemy over SQL or standard database model.

* **June 6 - June 12, 2022**
- Created PR https://github.com/augurlabs/augur_view/pull/22 for service file error.
- Current Behaviour: On starting the service file the following error occurs:

```
Failed to start augur_view.service: Unit augur_view.service has a bad unit file setting. and the log shows:

Neither a valid executable name nor an absolute path
Unit configuration has fatal error, unit will not be started.

Solution and changes made:

Updating the service file adding absolute path of directory to ExecStart.
Corrected a typo 

```