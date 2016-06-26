[![Build Status](https://travis-ci.org/rahul0705/ansible-irssi.svg?branch=develop)](https://travis-ci.org/rahul0705/ansible-irssi)

Ansible Irssi
=========

Ansible role to install and configure Irssi

Requirements
------------

None

Role Variables
--------------

```yaml
irssi_user: irssi
irssi_group: irssi
irssi_user_home: /home/{{ irssi_user }}

irssi_directory_config: "{{ irssi_user_home }}/.irssi"
irssi_directory_scripts: "{{ irssi_directory_config }}/scripts"
```

Dependencies
------------

None

Example Playbook
----------------

1) Install Irssi with default settings

```yaml
- hosts: all
  roles:
    - role: irssi
```

2) Install Irssi with custom settings

```yaml
- hosts: all
  roles:
    - role: irssi
      irssi_user: rahul
      irssi_user_home: /opt/rahul
```

License
-------

MIT
