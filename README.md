# zabbix-unifi
Zabbix Template to monitor UniFi Controller via web API. No additional libraries or scripts required.
## Usage
- create a readonly user on unifi controller
- create host with unifi controller IP
- add template

## macros
- {$UNIFI_PASSWORD} : password for the user that is used to login to the unifi controller
- {$UNIFI_USER} : username for the user that is used to login to the unifi controller
- {$UNIFI_PORT} : https port (normally 8443)
- {$UNIFI_UPDATEURL} : no need to modify. This one is used to pull the most recent controller version from unifi website

## monitored items
- current unifi controller version
- most recent unifi controller version
- guests online
- users online
- status
- items for each site:
 - number of current alarms
 - site description
 - unsupported device count
 - number of APs
  - adopted
  - disabled
  - disconnected
  - pending
## triggers
- alarms
- number of unsupported devices
- disconnected aps
- unifi version not up to date