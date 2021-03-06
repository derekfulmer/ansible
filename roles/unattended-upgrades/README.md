# Unattended-upgrades
## Summary

Unattended Upgrades is an mechanism in Debian based systems that, when configured, enables an operator to schedule automatic updates of all installed packages. This is equivalent to telling your host `sudo apt update && sudo apt upgrade` at any time you desire and specify in the files below.

This playbook allows an operator to install the `unattended-upgrades` package and copy the following configuration files:
- `20auto-upgrades`
- `50unattended-upgrades`

## Command to test on Vagrant
```
ansible-playbook --connection=local --limit "127.0.0.1" unattended-upgrades.yml --check
```
