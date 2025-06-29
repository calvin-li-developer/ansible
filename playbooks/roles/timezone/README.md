# Role Name: timezone

## Description

This role configures the system's timezone and Network Time Protocol (NTP) synchronization. It ensures the system's clock is accurate and set to the correct timezone.

The role performs the following actions:

- **Sets the System Timezone:** Configures the system to use the timezone specified in the `timezone_location` variable. This is handled by the `community.general.timezone` module.

- **Configures NTP Synchronization:** Deploys a configuration file for `systemd-timesyncd` to use Cloudflare's time server (`time.cloudflare.com`) as a fallback NTP server. This enhances time synchronization reliability.

- **Restarts Time Synchronization Daemon:** If the `systemd-timesyncd` configuration is updated, the `systemd-timesyncd` daemon is restarted to apply the changes immediately.

## Requirements

This role is designed for Debian-based systems (e.g., Ubuntu) that use `systemd-timesyncd` for time synchronization.

## Role Variables

- `timezone_location`: The timezone to set for the system. The default value is `America/Toronto`. A list of available timezones can be found by running `timedatectl list-timezones` on the target machine.

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

## Handlers

- `Restart timesyncd daemon`: This handler restarts the `systemd-timesyncd` service to apply any changes to its configuration file.

## License

BSD