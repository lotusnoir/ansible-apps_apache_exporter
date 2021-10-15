# ansible-apps_apache_exporter

## Description

[![Galaxy Role](https://img.shields.io/badge/galaxy-apps_apache_exporter-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_apache_exporter)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_apache_exporter.svg)](https://github.com/lotusnoir/ansible-apps_apache_exporter/releases/latest)
![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_apache_exporter?color=orange&style=flat)
[![downloads](https://img.shields.io/ansible/role/d/52300)](https://galaxy.ansible.com/lotusnoir/apps_apache_exporter)
![Ansible Quality Score](https://img.shields.io/ansible/quality/52300)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)

Deploy [apache_exporter](https://github.com/Lusitaniae/apache_exporter/) to expose apache metrics to prometheus.

## Requierements

You need to activate the status page on apache: http://localhost/server-status


## Role variables

| Name                            | Default Value  | Description                        |
| ------------------------------- | -------------- | -----------------------------------|
| `apache_exporter_version`       | 0.10.1          | apache_exporter version |
| `apache_exporter_temp_dir`      | /tmp           | temporary directory to uncompress package |
| `apache_exporter_install_dir`   | /usr/local/bin | directory to install binary |
| `apache_exporter_force_install` | false          | force install variable |
| `apache_exporter_port`          | 9117           | port to expose prometheus metrics |

## Examples

	---
	- hosts: apps_apache_exporter
	  become: yes
	  become_method: sudo
	  gather_facts: yes
	  roles:
	    - role: ansible-apps_apache_exporter
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}

## Prometheus rules

TODO

## Grafana dashboard

A sample dashboard is available here: [https://grafana.com/grafana/dashboards/13923](https://grafana.com/grafana/dashboards/13923)

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.
