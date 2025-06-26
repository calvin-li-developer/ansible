# Role: alias

This role configures custom command-line aliases for a user's shell environment.

## Role Variables

This role has no configurable variables.

## Tasks

- **Ensure .bashrc contains alias**: Deploys a `.bashrc` file from a template (`.bashrc.j2`). This file should contain the desired aliases.
- **Ensure .bashrc is sourced in .bash_profile**: Makes sure that the `.bashrc` file is loaded by `.bash_profile`, so the aliases are available in new login shells.

## Handlers

- **Reload bashrc**: This handler is triggered when the `.bashrc` or `.bash_profile` files are changed. It sources the `.bashrc` file to make the aliases immediately available in the current session.

## Example Playbook

Here is an example of how to use this role:

```yaml
- hosts: all
  roles:
    - alias
```

## Dependencies

This role has no dependencies.

## License

BSD