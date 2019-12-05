# Ansible <!-- this role name --> role

This is an [Ansible](http://www.ansible.com) role which installs/uninstalls Linux Name Service Cache Daemon (nscd)

## Requirements

[Ansible 2.7+](http://docs.ansible.com/ansible/latest/intro_installation.html)

## Role Variables

<!-- A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well. For example: -->

A list of all the default variables for this role is available in `defaults/main.yml`.

## Filters

<!-- A description of the filters provided by the role should go here. For example: -->


## Modules

<!-- A description of the modules provided by the role should go here. For example: -->

## Tests

<!-- A description of the tests provided by the role should go here. For example: -->

The role provides these tests:

- `thisrole_test1`: description of the test
- `thisrole_test2`: description of the test
- `thisrole_testN`: description of the test

## Dependencies

<!-- A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles. For example: -->

- [amtega.check_platform](https://galaxy.ansible.com/amtega/check_platform)
- [amtega.proxy_client](https://galaxy.ansible.com/amtega/proxy_client)
- [amtega.packages](https://galaxy.ansible.com/amtega/packages)

## Usage

<!-- Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too. For example: -->

This is an example playbook:

```yaml
---

- hosts: all
  roles:
    - role: amtega.nscd
        nscd_state: present
        nscd_config_param:
          - name: logfile
            value: /var/log/nscd.log
            state: present
          - name: "enable-cache"
            value: "hosts yes"
            state: present

```

## Testing

<!-- A description of how to run tests of the role if available. For example: -->

Tests are based on Vagrant/VirtualBox machines containers.

Once you have Vagrant and VirtualBox, you can run the tests with the following commands:

```shell
$ cd thisrole/tests
$ ansible-playbook maintest-vagrant.yml
```

## License

Copyright (C) 2019 AMTEGA - Xunta de Galicia

This role is free software: you can redistribute it and/or modify it under the terms of:

GNU General Public License version 3, or (at your option) any later version; or the European Union Public License, either Version 1.2 or – as soon they will be approved by the European Commission ­subsequent versions of the EUPL.

This role is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details or European Union Public License for more details.

## Author Information

- Carlos Chedas Fernandez
- <!-- author _name 2 -->.
- <!-- author _name N -->.
