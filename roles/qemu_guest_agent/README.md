# Role Name: qemu_guest_agent

## Description

This role installs the QEMU Guest Agent on virtual machines running on a QEMU/KVM hypervisor. The guest agent allows the hypervisor to perform actions on the guest, such as freezing and thawing the filesystem for consistent snapshots.

This role will only install the agent if it detects that the virtual machine is running on QEMU.

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
    - qemu_guest_agent
```

## License

BSD
