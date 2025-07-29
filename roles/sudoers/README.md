# Role Name: sudoers

## Description

This role configures passwordless `sudo` access for the `ansible_user`. It creates a file in `/etc/sudoers.d/` that allows the user to run all commands with `sudo` without being prompted for a password.

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
    - sudoers
```

## License

BSD