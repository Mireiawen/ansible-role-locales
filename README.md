![Build Status](https://img.shields.io/gitlab/pipeline-status/mireiawenrose/ansible-roles/locales?branch=master&style=plastic) [![Ansible Galaxy](https://img.shields.io/badge/Ansible%20Galaxy-mireiawen.locales-blueviolet?style=plastic)](https://galaxy.ansible.com/mireiawen/locales)

# Locales
Installs the locales package and generates the desired locales on Debian -based systems.

## Requirements
Debian -based distribution.

## Role Variables
 Configuration key       | Description                        | Default value
-------------------------|------------------------------------|----------------------
 `locales_package_name`  | The name of the locales package    | `locales`
 `locales_package_state` | The status of the locales package  | `latest`
 `locales`               | The locales to generate            | [ `en_US.UTF-8` ]

## Dependencies
* community.general

## Example Playbook
```yaml
- hosts: "servers"
  roles:
  - role: "mireiawen.locales"
    vars:
      locales:
      - "en_US.UTF-8"
      - "fi_FI.UTF-8"
```

## License
MIT, see `LICENSE`
