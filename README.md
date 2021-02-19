# Ansible Role: ansible-apps_apache_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_apache_exporter.svg?branch=master?style=flat)](https://travis-ci.com/lotusnoir/ansible-apps_apache_exporter)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)
[![Ansible Role](https://img.shields.io/badge/galaxy-apps_apache_exporter-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_apache_exporter)
![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_apache_exporter?color=orange&style=flat)
![Ansible Quality Score](https://img.shields.io/ansible/quality/52300)
[![downloads](https://img.shields.io/ansible/role/d/52300)](https://galaxy.ansible.com/lotusnoir/apps_apache_exporter)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_apache_exporter.svg)](https://github.com/lotusnoir/ansible-apps_apache_exporter/releases/)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_apache_exporter&metric=alert_status)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_apache_exporter)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_apache_exporter&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_apache_exporter)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_apache_exporter&metric=reliability_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_apache_exporter)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_apache_exporter&metric=security_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_apache_exporter)

Deploy [apache_exporter](https://github.com/danielqsj/apache_exporter/) to expose apache metrics to prometheus.

## Requierements

You need to be able to acces the web status page http://localhost/server-status


## Role variables

| Name                            | Default Value  | Description                        |
| ------------------------------- | -------------- | -----------------------------------|
| `apache_exporter_version`       | 0.8.0          | apache_exporter version |
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

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.
