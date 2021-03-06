# Netplan (Configuring static IP address)

## Summary

This playbook will assist with assigning static IP address for Debian systems using netplan

After the static ip address has been written to the netplan yaml file, the command "netplan apply" will be executed. This will cause
a short SSH disruption from the Ansible control node to the target host because of the change from DHCP to static. To prevent the SSH connection
to drop, there is an 'async' and 'wait_for' Ansible module that will re-establish the SSH connection with the new static ip address.

Tested and compatible with:
- Ubuntu 20.04 (Focal Fossa)
