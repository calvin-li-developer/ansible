# Role Name: ssh

## Description

This role uses the `ansible.posix.authorized_key` module to manage SSH keys in a user's `~/.ssh/authorized_keys` file. This allows for the dynamic addition and removal of SSH keys.

## Requirements

This role is designed for Debian-based systems (e.g., Ubuntu).

## Role Variables

This role uses the following variables, defined in `defaults/main.yml`:

- `ssh_keys`: A list of public SSH keys to be added to the `authorized_keys` file.

```yaml
ssh_keys:
  - "ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIE... key1"
  - "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQD... user@host"
```

## Dependencies

This role has no external dependencies.

## Example Playbook

Here is an example of how to use this role in a playbook:

```yaml
- hosts: all
  roles:
    - role: ssh_key
      vars:
        ssh_keys:
          - "ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAI... key1"
          - "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACA... user@host"
```

## License

BSD