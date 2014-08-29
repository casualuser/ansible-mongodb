# Golang role for Ansible

Installs the latest version of MongoDB from the 10gen PPA.

## Requirements

Tested on Ubuntu 12.04 Server.

## Example Playbook

    - hosts: 'servers'
      roles:
        - { role: 'ssilab.mongodb' }

# License

This playbook is provided 'as-is' under the conditions of the BSD license. No fitness for purpose is guaranteed or implied.