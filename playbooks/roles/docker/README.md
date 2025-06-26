# Role Name: docker

## Description

This role installs and configures Docker on Debian-based systems. It performs the following actions:

- Installs necessary dependencies.
- Adds Docker's official GPG key and APT repository.
- Installs the Docker engine, CLI, and related plugins (`containerd.io`, `docker-buildx-plugin`, `docker-compose-plugin`).
- Adds the `ansible_user` to the `docker` group to allow running Docker commands without `sudo`.
- Creates a `.docker` directory in the user's home directory.
- Deploys a basic `config.json` file to configure the Docker CLI.

## Requirements

This role is designed for Debian-based systems (e.g., Ubuntu).

## Role Variables

This role has no user-configurable variables in `defaults/main.yml`.

## Dependencies

This role has no external dependencies.

## Example Playbook

Here is an example of how to use this role in a playbook:

```yaml
- hosts: all
  become: true
  roles:
    - docker
```

## License

BSD
