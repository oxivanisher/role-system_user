system_user
===========

Configure OS users.

Role Variables
--------------

| Name              | Comment                                     | Default value                   |
|-------------------|---------------------------------------------|---------------------------------|
| system_user_users | A list of users to be ensured on the system | `[]` |

A element of the list of system users looks like this:

```yaml
  - name: johndoe
    comment: "John Doe"
    uid: 999
    password: "$6$PWSTRING"
    shell: /bin/bash
    groups:
      - adm
      - cdrom
      - sudo
      - dip
      - plugdev
      - lpadmin
      - lxd
      - sambashare
```


Example Playbook
----------------
```yaml
- name: Configure system users
  hosts: all
  collections:
    - oxivanisher.linux_base
  roles:
    - role: oxivanisher.linux_base.system_user
```

License
-------

BSD

Author Information
------------------

This role is part of the [oxivanisher.linux_base](https://galaxy.ansible.com/ui/repo/published/oxivanisher/linux_base/) collection, and the source for that is located on [github](https://github.com/oxivanisher/collection-linux_base).
