# Ansible Infrastructure Playbooks 

Useful Ansible Playbooks for setting up Ubuntu servers and provisioning Proxmox VM.

- Proxmox Playbook (Future Implementation)
- Ubuntu 24.04 Playbook (✔️)
    - alias
    - disable_ipv6
    - docker
    - hardening
    - qemu_guest_agent
    - ssh
    - sudoers
    - timezone
    - unattended_upgrades
    - update

## Pre-requisites

- [uv](https://docs.astral.sh/uv/install/) package manager must be installed.

## Usage

This project uses [uv](https://docs.astral.sh/uv/getting-started/) as a Python package and project manager.

### Linting

To run `ansible-lint`, use the following command:

```bash
uv run ansible-lint
```

### Running Playbooks

To execute a playbook, for example the `ubuntu.yml` playbook, use the following command:

```bash
uv run ansible-playbook playbooks/ubuntu.yml
```