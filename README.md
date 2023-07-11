[![Build Status](https://travis-ci.com/Mireiawen/ansible-role-locales.svg?branch=master)](https://travis-ci.com/Mireiawen/ansible-role-locales) [![Ansible Galaxy](https://img.shields.io/badge/Ansible%20Galaxy-mireiawen.locales-blueviolet)](https://galaxy.ansible.com/mireiawen/locales)
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FMireiawen%2Fansible-role-locales.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2FMireiawen%2Fansible-role-locales?ref=badge_shield)

# Locales
Installs the locales package and generates the desired locales.

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

[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FMireiawen%2Fansible-role-locales.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2FMireiawen%2Fansible-role-locales?ref=badge_large)