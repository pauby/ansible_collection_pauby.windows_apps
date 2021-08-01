win_irfanview
=========

A role to manage the Irfanview collection of software:

- Irfanview
- Irfanview Shell Extension
- Irfanview Plugins

The rolw will install the rquired Chocolatey packages and set the file associations needed.

Requirements
------------

Requires:

* chocolatey.chocolatey collection (specifically chocolatey.chocolatey.win_chocolatey);
* ansible.windows collection (specifically win_regedit);

Role Variables
--------------

Has the following variables:

* install_plugins [boolean] - whether the plugins for Irfanview are installed (using the Chocolatey [`irfanviewallplugins`](https://community.chocolatey.org/packages/irfanviewplugins) package;
* install_shellextension [boolean] - whether the shell extension for Irfanview are installed (using the Chocolatey [`irfanvie-shellextension`](https://community.chocolatey.org/packages/irfanview-shellextension) package;
* registry_changes [list of dicts] - contains a list of the registry changes to make to set  the file associations. See `vars/main.yml`.

Dependencies
------------

None.

Example Playbook
----------------

```
- hosts: servers
  roles:
      - { role: pauby.windows_apps.win_irfanview, install_plugins: true }
```

License
-------

MIT

Author Information
------------------

Paul Broadwith - https://blog.pauby.com / https://github.com/pauby