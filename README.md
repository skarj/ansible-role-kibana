Kibana role
=========
[![Build Status](https://api.travis-ci.org/skarj/ansible-role-kibana.svg?branch=master)](https://travis-ci.org/skarj/ansible-role-kibana)

Ansible role for [kibana](https://www.elastic.co/products/kibana) 6.x installation.
Versions lower than 6 are not supported by this role.

Requirements
------------

* Ansible 2.5
* This role requires [hash_behaviour=merge](http://docs.ansible.com/ansible/latest/reference_appendices/config.html#default-hash-behaviour) for variables


Dependencies
------------

None


Role Variables
--------------

Default config variables are described in *defaults/main.yml*.
If you need an extended configuration you can specify it in the variables for each environment in section *kibana.config*.
Structure of section *kibana.config* repeats *kibana.yml*, you can insert any parameters described in official kibana [documentation](https://www.elastic.co/guide/en/kibana/current/settings.html)


Example Playbook
----------------

An example of how to use this role:

        - hosts: all
          roles:
            - role: ansible-role-kibana
              kibana:
                options:
                  server.port: 5601
                  elasticsearch.url: "192.168.200.20:9200"


License
-------

MIT


Author Information
------------------

Sergey Baranov <skaarj.sergey@gmail.com>
