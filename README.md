# VBox-Guest

[![Alma9-CI](https://github.com/philnewm/ansible-vbox-guest/actions/workflows/alma9-ci.yml/badge.svg)](https://github.com/philnewm/ansible-vbox-guest/actions/workflows/alma9-ci.yml) [![Rocky9-CI](https://github.com/philnewm/ansible-vbox-guest/actions/workflows/rocky9-ci.yml/badge.svg)](https://github.com/philnewm/ansible-vbox-guest/actions/workflows/rocky9-ci.yml) [![CentOS9-CI](https://github.com/philnewm/ansible-vbox-guest/actions/workflows/centos9-ci.yml/badge.svg)](https://github.com/philnewm/ansible-vbox-guest/actions/workflows/centos9-ci.yml) [![Debian12-CI](https://github.com/philnewm/ansible-vbox-guest/actions/workflows/debian12-ci.yml/badge.svg)](https://github.com/philnewm/ansible-vbox-guest/actions/workflows/debian12-ci.yml) [![Ubuntu22.04-CI](https://github.com/philnewm/ansible-vbox-guest/actions/workflows/ubuntu2204-ci.yml/badge.svg)](https://github.com/philnewm/ansible-vbox-guest/actions/workflows/ubuntu2204-ci.yml)

This role is largely inspired by the [vbox-guest role](https://github.com/ezamriy/ansible-role-vbox_guest) used in the [Almalinux cloud-images](https://github.com/AlmaLinux/cloud-images/) repo.
I modified it for my own [packer repo](https://github.com/philnewm/packer-templates).<br>
The focus is on including Debian and Ubuntu in this setup since it was originally created only for RedHat based distros.

This role includes a full vagrant based molecule testing setup at `extensions/molecule/default`.<br>
The molecule setup currently only includes debian as a vagrant box for testing.

## Structure

```code
📦 ansible-role-template
 ┣ 📂 defaults
 ┃ ┗ 📜 main.yml
 ┣ 📂 meta
 ┃ ┗ 📜 main.yml
 ┣ 📂 molecule
 ┃ ┗ 📂 default
 ┃   ┗ 📜, 📜, 📜, scenario_files
 ┣ 📂 tasks
 ┃ ┣ 📜 main.yml
 ┃ ┣ 📜 present.yml
 ┃ ┣ 📜 dependencies.yml
 ┃ ┣ 📜 absent.yml
 ┃ ┗ 📜 init.yml
 ┣ 📂 vars
 ┃ ┗ 📜 main.yml
 ┗ 🗒️ README.md
 ┗ 📓 requirements.txt

```

Describe and explain role structure.

## Requirements

This role doesn't depend on any additional ansible-galaxy roles

## Role Variables

* defaults/main.yml
  * first_var
  * sec_var
  * third_var
* vars/main.yml
  * first_var
  * sec_var
  * third_var

## Dependencies

This role doesn't depend on any additional ansible-galaxy roles

## Example Playbook

Add an example playbook

```yaml
---

tasks:
  - name: Include ansible-vbox-guest present
    ansible.builtin.include_role:
      name: ansible-vbox-guest
    vars:
      vbox_guest_state: present

...
```

## License

Add license - if any.
