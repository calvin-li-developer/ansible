# Role Name: docker

## Description

This role installs and configures Docker on Debian-based systems. It performs the following actions:

- Installs necessary dependencies.
- Adds Docker's official GPG key and APT repository.
- Installs the Docker engine, CLI, and related plugins (`containerd.io`, `docker-buildx-plugin`, `docker-compose-plugin`).
- Adds a specified user to the `docker` group to allow running Docker commands without `sudo`.
- Ensures the Docker service is started and enabled.
- Creates a `.docker` directory in the user's home directory.
- Deploys a basic `config.json` file to configure the Docker CLI.

## Requirements

This role is designed for Debian-based systems (e.g., Ubuntu).

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

| Variable | Default Value | Description |
|---|---|---|
| `docker_packages` | `['docker-ce', 'docker-ce-cli', 'containerd.io', 'docker-buildx-plugin', 'docker-compose-plugin']` | A list of Docker-related packages to install. |
| `docker_user` | `{{ ansible_user }}` | The user to be added to the `docker` group. |

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
