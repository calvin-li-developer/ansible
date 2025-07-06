# Role Name: ssh

## Description

This role uses the `ansible.posix.authorized_key` module to manage SSH keys in a user's `~/.ssh/authorized_keys` file. This allows for the dynamic addition and removal of SSH keys from a github user's `.keys` file.

## Requirements

This role is designed for Debian-based systems (e.g., Ubuntu).

## Role Variables

This role uses the following variables, defined in `defaults/main.yml`:

- `ssh_github_user`: The github username to fetch the ssh keys from.

```yaml
ssh_github_user: "username"
```

## Dependencies

This role has no external dependencies.

## Example Playbook

Here is an example of how to use this role in a playbook:

```yaml
- hosts: all
  roles:
    - role: ssh
      vars:
        ssh_github_user: "username"
```

## License

BSD