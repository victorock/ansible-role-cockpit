Ansible Role to Install Cockpit
=========

Ansible role to install Cockpit.

Role Variables
--------------

Variables are defined in `defaults/main.yml` and structured/encapsulated in `vars/`.

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `autorun` | `False`  | Boolean to define if the role "autorun" (`tasks/main.yml`). Useful when you want to have dependencies solved by galaxy (`meta/main.yml`) but don't want it to run automatically.  |
| `cockpit_plugins` | `[ 'ws', 'system', 'packagekit', 'dashboard', 'machines', 'networkmanager', 'sosreport' ]` | The list of cockpit plugins to install. |
| `cockpit_plugins_state` | `latest` | The state of the plugins. |

Examples
------------

Follow below different examples and ways to use this role.

>Playbook: Install Cockpit with default options.

```YAML
---
- name: "cockpit: Install cockpit"
  hosts: network_lab
  gather_facts: true
  become: true

  roles:
    - role: victorock.cockpit
      autorun: true

```

License
------------

GPLv3

Author
------------

Victor da Costa (@victorock)
