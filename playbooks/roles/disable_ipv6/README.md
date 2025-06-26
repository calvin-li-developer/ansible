# Role Name: disable_ipv6

## Description

This role disables IPv6 on Debian-based systems. It achieves this by adding `ipv6.disable=1` to the kernel boot parameters and blacklisting the `ipv6` kernel module.

## Requirements

This role is designed for Debian-based systems (e.g., Ubuntu).

## Role Variables

This role has no configurable variables.

## Dependencies

This role has no dependencies.

## Example Playbook

Here is an example of how to use this role:

```yaml
- hosts: all
  roles:
    - disable_ipv6
```
## Dependencies

This role has no dependencies.

## License

BSD