# Binding Linux servers to the AD

## Summary
This project utilizes Ansible group_vars and roles to assist with running the bind-to-ad.yml playbook. After successfully executing this playbook, you will
be able to bind Linux servers to the domain.

The purpose for having group_vars is to automatically associate Linux servers to there respective OU group of either Test or Prod (see realmd.conf) based on how the host are
grouped in the Ansible inventory file (dev_vmware or prod_vmware).

The Ubuntu packages that made binding to the AD possible are:
- System Security Service Daemon (SSSD)
- Realmd

## Commands to test on Vagrant
ansible-playbook --connection=local --limit "127.0.0.1" -e realm_ou_env_object=Test bind-to-ad.yml --check
