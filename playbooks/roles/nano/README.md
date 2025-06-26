# Role Name: nano

## Description

This role installs and configures the Nano text editor. It performs the following actions:

- Installs the `nano` package.
- Deploys a `.nanorc` file to the user's home directory to enable syntax highlighting for Python, C, HTML, and YAML.

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
  roles:
    - nano
```

## License

BSD