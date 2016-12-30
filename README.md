Ansible MariaDB Role
====================

An ansible role for installing and configuring MariaDB client / server

Role Variables
--------------

```yaml
mariadb_server_install: define if you wish to install mariadb server
mariadb_server_pkg_version: define the mariadb server version
mariadb_server_pkg_state: installed
mariadb_client_install: define if you wish to install mariadb client
mariadb_client_pkg_version: define the mariadb client version
mariadb_client_pkg_state: installed
mariadb_service_state: define the mariadb service state
mariadb_service_enabled: define if the mariadb service needs to be enabled
mariadb_root_password: define the root password
mariadb_root_config: holds a dictionary with all config parameters. See the defaults for an example
mariadb_replication_user: list of replication users, containing name and password
mariadb_role: define the role of the mysql instance ( master / slave ). Or omit when using standalone.
mariadb_replication_master: define the replication master host. Omit when using standalone
```

Example Playbook
-------------------------

```yaml
- hosts: servers
  roles:
     - { role: MichaelRigart.mariadb, become: true }
```

License
-------

GPLv3

Author Information
------------------

Michaël Rigart <michael@netronix.be>
