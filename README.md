[![Build Status](https://travis-ci.com/Mireiawen/ansible-role-locales.svg?branch=master)](https://travis-ci.com/Mireiawen/ansible-role-locales) [![Ansible Galaxy](https://img.shields.io/badge/Ansible%20Galaxy-mireiawen.locales-blueviolet)](https://galaxy.ansible.com/mireiawen/locales)


# Locales
Installs the locales package and generates the desired locales.

## Requirements
None.

## Role Variables
| Variable                | Type   | Default value     | Description                        |
|-------------------------|--------|-------------------|------------------------------------|
| `locales_package_name`  | string | `locales`         | The name of the locales package.   |
| `locales_package_state` | string | `latest`          | The status of the locales package. |
| `locales`               | array  | [ `en_US.UTF-8` ] | The locales to generate.           |

## Dependencies
None.

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
