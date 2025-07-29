# Role Name: unattended_upgrades

## Description

This role installs and configures `unattended-upgrades` to automatically install security updates. It performs the following actions:

- Installs the `unattended-upgrades` and `update-notifier-common` packages.
- Configures `unattended-upgrades` to:
    - Automatically install packages from security repositories.
    - Automatically remove unused kernel packages and dependencies.
    - Automatically reboot the system at 2:50 AM if a reboot is required after an upgrade.

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
    - unattended_upgrades
```

## License

BSD
