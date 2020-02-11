# tilix

[Tilix][tilix] is an advanced GTK3 tiling terminal emulator that follows the
GNOME Human Interface Guidelines. This Ansible role installs and configures
Tilix on Ubuntu system (Ubuntu, Mint and so on).

This role based on role [ansible-role-tilix](https://github.com/ghyde/ansible-role-tilix/)

## Role Variables

### defaults/main.yml

|name|description|type|default|
|---|---|---|---|
|tilix_preferences_backup_file|Path to backup file of Tilix preferences|file path|/tmp/tilix_preferences.{{ ansible_date_time.epoch }}|

## Example Playbook

```yaml
- hosts: workstations
  tasks:
  - import_role:
      name: ansible-role-tilix
```

## Post-Install Requirements

none

## Update Preferences File

To update this role with your current Tilix preferences, run the following
command:

```bash
dconf dump /com/gexperts/Tilix/ > files/preferences
```

## License

[MIT](LICENSE)

[tilix]: https://gnunn1.github.io/tilix-web/
[ansible-role-tilix]: https://github.com/ghyde/ansible-role-tilix/ (the original role)
