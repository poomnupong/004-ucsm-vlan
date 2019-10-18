004-ucsm-vlan
Ansible script to bulk create VLAN range on UCS Manager
2019.10.18
Poom Nupong (poomsawas@gmail.com)
===

## Overview
UCS Manager GUI does not allow creating range of VLAN and this script aim to speed up the process.

This is effective in the case of UCSM-ACI integration with VMM integration where the range of dynamic VLAN need to be provisioned on the Fabric Interconnect.

Note: recent version of ACI offers UCSM integration and can take care of the dynamic VLAN integration.

## Usage:
- edit UCS Manager credentials in inventory.yml
- edit vlan range in ucsm-vlancreate.yml
- run the playbook

# ansible-playbook ucsm-vlancreate.yml