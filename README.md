# MongoDB role for Ansible

Installs the latest version of MongoDB from the 10gen PPA.

## Requirements

Tested on Ubuntu 12.04 Server.

## Role Variables

The default variables are as follows:

    mongodb_backup_cron_filename: 'mongodb_backup'
    mongodb_backup_cron_name:     'Back up MongoDB databases'
    mongodb_backup_frequency:     'daily'
    mongodb_backup_hour_of_day:   3
    mongodb_backup_lifetime_days: 14
    mongodb_backup_file_prefix:   'mongodb_backup'
    mongodb_backup_dir:           '/var/backup/mongodb_backup'
    mongodb_backup_script_path:   '/etc/mongodb_backup/mongodb_backup.sh'

## Example Playbook

    - hosts: 'servers'
      roles:
        - role: 'ssilab.mongodb'
          mongodb_backup_frequency:     'monthly'
          mongodb_backup_hour_of_day:   4
          mongodb_backup_lifetime_days: 30
          mongodb_backup_file_prefix:   'my_app_backup_name'
          mongodb_backup_dir:           '{{ my_user_home }}/backups'

# License

This playbook is provided 'as-is' under the conditions of the BSD license. No fitness for purpose is guaranteed or implied.