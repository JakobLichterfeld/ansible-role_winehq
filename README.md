# Ansible Role: WineHQ

[![CI](https://github.com/JakobLichterfeld/ansible-role-winehq/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/JakobLichterfeld/ansible-role-winehq/actions/workflows/ci.yml)
[![Publish role on Ansible Galaxy](https://github.com/JakobLichterfeld/ansible-role-winehq/actions/workflows/publish_role_on_ansible_galaxy.yml/badge.svg?branch=main)](https://github.com/JakobLichterfeld/ansible-role-winehq/actions/workflows/publish_role_on_ansible_galaxy.yml)

Install WineHQ via PPA repository.

- Add GPG repository key
- Add WineHQ repository
- Enable i386 support if needed
- Install WineHQ (on Ubuntu 24.04 staging version is installed by default, as there are no packages for the stable version)
- Install PlayOnLinux (optional)
- Install Winetricks (optional)

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

| Name           | Default Value   | Description                        |
| -------------- | --------------- | -----------------------------------|
| `winehq.install_playonlinux` | true | Whether to install PlayOnLinux |
| `winehq.install_winetricks` | true | Whether to install Winetricks |
| `winehq.use_devel` | false | Whether to use the devel version of WineHQ |
| `winehq.use_staging` | false | Whether to use the staging version of WineHQ |

## Dependencies

None.

## Example Playbook

```yaml
---
- hosts: all
  gather_facts: true
  become: true

  roles:
    - role: jakoblichterfeld.winehq

```

## License

MIT

## Author Information

This role was created in 2023 by [Jakob Lichterfeld](https://github.com/JakobLichterfeld).
