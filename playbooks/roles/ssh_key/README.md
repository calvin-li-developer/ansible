# Role Name: ssh_key

## Description

This role deploys a set of authorized SSH keys to a user's `~/.ssh/authorized_keys` file. This allows the specified public keys to be used for SSH authentication.

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
    - ssh_key
```

## License

BSD