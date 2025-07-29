# Role Name: update

## Description

This role updates all packages on a server. For Debian-based systems, it is equivalent to running `apt update` and `apt dist-upgrade`.

## Requirements

This role is currently implemented for Debian-based systems (e.g., Ubuntu) that use the `apt` package manager.

## Role Variables

This role has no user-configurable variables.

## Dependencies

This role has no external dependencies.

## Example Playbook

Here is an example of how to use this role in a playbook:

```yaml
- hosts: all
  become: true
  roles:
    - update
```

## License

BSD