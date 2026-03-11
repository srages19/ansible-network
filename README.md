# Network Ansible Playbooks

Ansible playbooks for Cisco IOS-XE and IOS-XR automation.

## Playbooks
- show_version.yml - Gather device software version
- config_push.yml - Push loopback interface configuration

## Requirements
- ansible-core
- cisco.ios collection
- cisco.iosxr collection

## Setup

1. Copy example files and fill in your values:
```
   cp inventory/hosts.ini.example inventory/hosts.ini
   cp vars/site_build.yml.example vars/site_build.yml
```

2. Create vault files for credentials:
```
   ansible-vault create group_vars/iosxr/iosxr_vault.yml
   ansible-vault create group_vars/iosxe/iosxe_vault.yml
   ansible-vault create group_vars/all/vault.yml
```

3. Create vault password file:
```
   echo "your_vault_password" > ~/.vault_pass
   chmod 600 ~/.vault_pass
```
