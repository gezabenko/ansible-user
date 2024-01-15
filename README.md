Ansible - User
=========

Ansible role for user management

Requirements
------------

NA

Role Variables
--------------

Only one variable need (`name`) and implemented the next parameters:

```yaml
user:
  backup:
    comment: 'Backup user'
    create_home: 'true'
    expires: '-1'
    groups: 'backup, ssh_user'
    home: '/opt/backup'
    local: 'false'
    move_home: 'false'
    non_unique: 'false'
    password: '!'
    remove: 'false'
    shell: '/bin/bash'
    state: 'present'
    system: 'true'
    uid: '9999'
    umask: '077'
    update_password: 'always'
    authorized_key:
      key: 'ssh-rsa ...
```

Dependencies
------------

- [ansible.builtin.user](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/user_module.html#ansible-collections-ansible-builtin-user-module)
- [ansible.postfix.authorized_key](https://docs.ansible.com/ansible/latest/collections/ansible/posix/authorized_key_module.html)

Example Playbook
----------------

```yaml
    - hosts: servers
      roles:
         - { role: user, tags: [ user ] }
```

License
-------

GPLv3

