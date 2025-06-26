# Role Name: timezone

## Description

This role configures the system's timezone and NTP synchronization. It performs the following actions:

- **Sets the Timezone:** Configures the system to use the timezone specified in the `timezone_location` variable.
- **Configures NTP:** Deploys a configuration file for `systemd-timesyncd` to use Cloudflare's time server as a fallback NTP server.

## Requirements

This role is designed for Debian-based systems (e.g., Ubuntu).

## Role Variables

- `timezone_location`: The timezone to set for the system. The default value is `America/Toronto`.

## Dependencies

This role has no external dependencies.

## Example Playbook

Here is an example of how to use this role in a playbook, overriding the default timezone:

```yaml
- hosts: all
  become: true
  roles:
    - role: timezone
      vars:
        timezone_location: "America/New_York"
```

## License

BSD