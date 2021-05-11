Ansible Role: nextcloud exporter
=========

[![CI](https://github.com/Puller23/ansible-role-nextcloud_exporter/actions/workflows/ci.yml/badge.svg)](https://github.com/Puller23/ansible-role-nextcloud_exporter/actions/workflows/ci.yml)

Deploy prometheus [nextcloud exporter](https://github.com/xperimental/nextcloud-exporter) using ansible.

Requirements
------------

- Ansible >= 2.7

Role Variables
--------------

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) and are listed in the table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `nextcloud_exporter_version` | 0.4.0 | nextcloud exporter package version.|
| `nextcloud_exporter_install_dir` | "" | Allows to use local packages instead of ones distributed on github.|
| `nextcloud_exporter_listen_adress` | "0.0.0.0" | Address on which nextcloud exporter will listen |
| `nextcloud_exporter_listen_port` | 9205 | Port on which nextcloud exporter will listen |
| `nextcloud_exporter_metrics` | "metrics" | Path under which to expose metrics |
| `nextcloud_exporter_system_user` | "nextcloud_exp" | User for systemd service |
| `nextcloud_exporter_system_group` | "nextcloud_exp" | User for systemd service |


Dependencies
------------

none

Example Playbook
----------------

Use it in a playbook as follows:
```yaml
- hosts:
  roles:
    - puller23.nextcloud_exporter
```

License
-------

MIT

Author Information
------------------

This role was created in 2021 by Gregor Bartels.