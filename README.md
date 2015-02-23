ansible-role-epel
=========

Ansible role to setup EPEL repository on RHEL based system.

Requirements
------------

Ansible

Role Variables
--------------

| Name | Description | Value |
| :------ | :-------------- | :------ |
| epel_rpm_download_dir | Directory where to stored the downloaded rpm file on local host | /tmp |
| epel_rpm_state | State of the rpm on remote system | present |
| epel_rpm_file_url | URL where to download the rpm file from | Depends on '{{ ansible_os_family }}{{ ansible_distribution_major_version }}.{{ ansible_architecture }}.yml' |
| epel_rpm_file_name | Name of the rpm file to download | '{{ ansible_os_family }}{{ ansible_distribution_major_version }}.{{ ansible_architecture }}.yml' |
Dependencies
------------


Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: epel }

License
-------

BSD

Author Information
------------------

email: ntbc@gmx.net
