ansible-role-colorls
=========

<p align="center">

<a href="https://github.com/iancleary/ansible-role-colorls/actions?query=workflow%3Aci" target="_blank">
    <img src="https://github.com/iancleary/ansible-role-colorls/workflows/CI/badge.svg" alt="CI workflow status">
</a>

<a href="https://github.com/iancleary/ansible-role-colorls/actions?query=workflow%3Arelease" target="_blank">
    <img src="https://github.com/iancleary/ansible-role-colorls/workflows/Release/badge.svg" alt="Release workflow status">
</a>

<a href="https://raw.githubusercontent.com/iancleary/ansible-role-colorls/main/LICENSE" target="_blank">
    <img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License">
</a>
</p>

This role installs the colorls ruby gem, its dependencies, and configures shell completion.

Requirements
------------

None

Role Variables
--------------

None


Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: servers
  user: unprivelaged
  roles:
    - role: iancleary.colorls
      become: true
      become_password: "{{ vault_become_password }}"
```

> Or you can remove become_password and use [--ask-become-pass](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_privilege_escalation.html)

Privelege escalation is needed to install ruby.

```yaml
- hosts: servers
  user: root
  roles:
    - role: iancleary.colorls
```

License
-------

[MIT](LICENSE)

Author Information
------------------

This role was created in 2023 by [Ian Cleary](https://iancleary.me).

Inspiration for the structure of this repo came from [Jeff Geerling](https://github.com/geerlingguy/ansible-role-nginx).
