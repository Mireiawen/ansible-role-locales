![Build Status](https://img.shields.io/gitlab/pipeline-status/mireiawenrose/ansible-roles/locales?branch=master&style=plastic) [![Ansible Galaxy](https://img.shields.io/badge/Ansible%20Galaxy-mireiawen.locales-blueviolet?style=plastic)](https://galaxy.ansible.com/mireiawen/locales)


# Locales
Installs the locales package and generates the desired locales.

## Requirements
Debian -based distribution.

## Role Variables
| Variable                | Type   | Default value     | Description                        |
|-------------------------|--------|-------------------|------------------------------------|
| `locales_package_name`  | string | `locales`         | The name of the locales package.   |
| `locales_package_state` | string | `latest`          | The status of the locales package. |
| `locales`               | array  | [ `en_US.UTF-8` ] | The locales to generate.           |

## Dependencies

* community.general

## Example Playbook
```
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
