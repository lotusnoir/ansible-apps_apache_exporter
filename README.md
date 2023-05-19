# ansible-apps_apache_exporter

[![Galaxy Role](https://img.shields.io/badge/galaxy-apps_apache_exporter-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_apache_exporter)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_apache_exporter.svg)](https://github.com/lotusnoir/ansible-apps_apache_exporter/releases/latest)
[![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_apache_exporter?color=orange&style=flat)](https://galaxy.ansible.com/lotusnoir/apps_apache_exporter)
[![downloads](https://img.shields.io/ansible/role/d/53226)](https://galaxy.ansible.com/lotusnoir/apps_apache_exporter)
[![Ansible Quality Score](https://img.shields.io/ansible/quality/53226)](https://galaxy.ansible.com/lotusnoir/apps_apache_exporter)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)

## Description

Deploy [apache_exporter](https://github.com/Lusitaniae/apache_exporter/) to expose apache metrics to prometheus.
## Requirements

You need to activate the status page on apache: http://localhost/server-status

## Role variables

See [variables](/defaults/main.yml) for more details.

## Examples

        ---
        - hosts: apps_apache_exporter
          become: true
          become_method: sudo
          gather_facts: true
          roles:
            - role: ansible-apps_apache_exporter

## Grafana Dashboard

You can find a grafana dashboard [here](https://grafana.com/grafana/dashboards/13923)

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.

## Author Information

- [Philippe LEAL](https://github.com/lotusnoir)
