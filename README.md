[![Build Status](https://travis-ci.org/pkorobeinikov/ansible-role-postgresql.svg?branch=master)](https://travis-ci.org/pkorobeinikov/ansible-role-postgresql)

ansible-role-postgresql
=======================

Postgresql installation.

Requirements
------------

You must provide your own `pg_hba.conf.j2` and `postgresql.conf.j2` templates.

Role Variables
--------------

* `postgresql_version` is a postgresql version number, e.g. `9.5`
* `postgresql_package_version` is an exact package version, e.g. `9.5.3-1.pgdg14.04+1`
* `postgresql_hba_template` is a path to `pg_hba.conf` template within current playbook.
* `postgresql_conf_template` is a path to `postgresql.conf` template within current playbook.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: pkorobeinikov.postgresql
          postgresql_version: 9.5
          postgresql_package_version: 9.5.3-1.pgdg14.04+1
          postgresql_hba_template: postgresql/pg_hba.conf.j2
          postgresql_conf_template: postgresql/postgresql.conf.j2

License
-------

BSD, MIT
