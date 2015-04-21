ajgarlag.kibana4
================

Ansible role to install Kibana4.

[![Build Status](https://travis-ci.org/ajgarlag/ansible-kibana4.svg?branch=master)](https://travis-ci.org/ajgarlag/ansible-kibana4)

Role Variables
--------------

* **ajgarlag_kibana4_version**: Version of kibana4 to install (defaults to *4.0.2*)
* **ajgarlag_kibana4_autostart**: Boolean flag to control if the kibana4 server should be started when booting the host (defaults to *yes*).
* **ajgarlag_kibana4_settings**: Dict of parameters to write into the kibana4 config file, for example *{"elasticsearch_url": "http://127.0.0.1:9200"}*.

Dependencies
------------

* **ajgarlag.bootstrap**: Ansible role to perform some basic setup to execute other ansible roles.

Example Playbook
----------------

```yml
- hosts: all
  roles:
    - role: ajgarlag.kibana4
      ajgarlag_kibana4_settings:
        "elasticsearch_url": "http://127.0.0.1:9200"
```


License
-------

MIT

Author Information
------------------

Developed with ♥ by [Antonio J. García Lagar](http://aj.garcialagar.es).
