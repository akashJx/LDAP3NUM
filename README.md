# LDAP3NUM

**LDAP3NUM is modified version of [ADenum](https://github.com/SecuProject/ADenum)**

**Why I made this?**
- For easing the process of LDAP enumeration in OSCP exam and general pentesting.
- [ADenum](https://github.com/SecuProject/ADenum) has automatic features of **_AS-REP Roastable, Kerberoastable, Password cracking with john (krb5tgs and krb5asrep)_** which can be classified as restricted tool for OSCP exam. (I checked with offsec for this)
- In LDAP3NUM, I totally removed all the codes automatic exploitation.

## Requirements
- Impacket (https://github.com/SecureAuthCorp/impacket)
- John (https://github.com/openwall/john)
- Python 3 
- If you are using **debian** or **ubuntu**:
	```bash
	sudo apt-get install libsasl2-dev python-dev libldap2-dev libssl-dev
	```
- If you are using  **kali**:
	```bash
	sudo apt-get install libsasl2-dev python2-dev libldap2-dev libssl-dev
	```
- pip3:
	```bash
  virtualenv -p python3 tempenv; source ./tempenv/bin/activate;
	pip3 install -r requirements.txt
	```

### Tested on
- Kali Linux 2021.3 (PWK VM)
- PG-Practice Hutch box (In Progress)
  
## Features and Functionality 
### LDAP:

- Enum Domain Admin users
- Enum Domain Controllers
- Enum Domain users with Password Not Expire
- Enum Domain users with old password
- Enum Domain users with interesting description
- Enum Domain users with not the default encryption
- Enum Domain users with Protecting Privileged Domain Accounts

## Microsoft Advanced Threat Analytics

ATA detects two suspicious events but does **not** trigger an **alert**:
- The connection with the protocol LDAP without SSL
- The Kerberoastable attack 

As shown in this screenshot:

![ATAdetection](https://user-images.githubusercontent.com/26841401/174618534-ebbf640d-e61b-4d4d-8028-fb48eaa0b848.png)

## Source 
Main Inspiration:
- https://github.com/SecuProject/ADenum

Documentation:
- https://labs.f-secure.com/blog/attack-detection-fundamentals-discovery-and-lateral-movement-lab-1/
- https://theitbros.com/ldap-query-examples-active-directory/
- https://docs.microsoft.com/en-us/advanced-threat-analytics/what-is-ata

Impacket:
- https://github.com/SecureAuthCorp/impacket/blob/master/examples/GetNPUsers.py
- https://github.com/SecureAuthCorp/impacket/blob/master/examples/GetUserSPNs.py


## Legal Disclaimer:

    This project is made for educational and ethical testing purposes only. Usage of this software for attacking targets without prior mutual consent is illegal. 
    It is the end user's responsibility to obey all applicable local, state and federal laws. 
    Developers assume no liability and are not responsible for any misuse or damage caused by this program.

---

**My Discord :** akashx#4733
DM to discuss about this tool / about improvements. 

---
