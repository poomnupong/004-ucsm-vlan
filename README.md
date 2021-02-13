# ucsm-vlan-create

Ansible script to bulk create VLAN range on UCS Manager  
2019.10.18  

===

### Overview
UCS Manager GUI does not allow creating range of VLAN and this script aim to speed up the process.

This is effective in the case of UCSM-ACI integration with VMM integration where the range of dynamic VLAN need to be provisioned on the Fabric Interconnect.

Note: recent version of ACI offers UCSM integration and can take care of the dynamic VLAN integration.

### Prerequisite & environment setup
UCS Manager Ansible modules has some dependencies. I choose to install these within virtual environment. Tested on Ubuntu 20.04 server.

```bash
# install the pre-reqs
$ sudo apt install python3 python3-venv python3-pip

# setup virtual environment
$ python3 -m venv venv
$ source ./venv/bin/activate
# (use 'deactivate' when done)

# install ansible with pip.
# wheel is required to setup ansible or else pip will throw errors
(venv) $ pip install wheel
(venv) $ pip install ansible
(venv) $ pip install ucsmsdk
```

### Usage:
- edit UCS Manager credentials in inventory.yml
- edit vlan range in ucsm-vlancreate.yml
- run the playbook

```bash
ansible-playbook ucsm-vlancreate.yml
```
