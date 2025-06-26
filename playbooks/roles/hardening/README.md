# Role Name: hardening

## Description

This role hardens the SSH configuration of a server based on recommendations from [sshaudit.com](https://sshaudit.com). It performs the following actions:

- **Disables Password Authentication:** Sets `PasswordAuthentication no` to prevent password-based logins.
- **Strengthens Encryption:** Configures a strong set of ciphers, key exchange algorithms, and MACs to enhance security.

These changes are applied by creating configuration files in `/etc/ssh/sshd_config.d/`, which will restart the SSH daemon.

## Requirements

This role is designed for Debian-based systems (e.g., Ubuntu) with OpenSSH installed.

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
    - hardening
```

## License

BSD