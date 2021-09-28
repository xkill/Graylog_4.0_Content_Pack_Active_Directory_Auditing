# Active Directory Auditing Content Pack
It's an xkill update of the reighnman 's & aydnyldrm 's Active Directory Auditing Content Pack for Graylog 2.x and Graylog 3 
You can find original content pack at https://marketplace.graylog.org/addons/750b88ea-67f7-47b1-9a6c-cbbc828d9e25
Tested with winlogbeats under Graylog 4.1 and Windows 2019 AD.

This content pack provides several useful dashboards for auditing Active Directory events:
* DNS Object Summary - DNS Creations, Deletions
* Group Object Summary - Group Creations, Modifications, Deletions, Membership Changes
* User Object Summary - Account Creations, Deletions, Modifications, Lockouts, Unlocks
* Computer Object Summary - (in progress)
* Logon Summary - Failed Authentication Attempts, Interactive Logins

## Includes

* Input (GELF udp 5414)
* Failed Logon Stream (unconfigured)
* Dashboards 

## Requirements

* winlogbeats collecting windows logs, other log collectors will work but may require modifying the searches to match the different fields outputted by other collectors
* Domain Controller secuirty policy with the following enabled:
** Audit Account Logon Events
** Audit Account Managmenet
** Audit Logon Events
** Audit Object Access
** Audit Policy Change
** Audit System Events
* Leading Wildcard Searches enabled in graylog.conf:  allow_leading_wildcard_searches = true

Ensure that Input Beats has `Do not add Beats type as prefix` unchecked. So, the `winlogbeat_` is added to the fields.

## Screenshots

![Dashboard](http://www.ohjeah.net/wp-content/uploads/2015/09/ad_audit.png)
