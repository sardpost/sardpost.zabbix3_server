
Zabbix 3 Server Installation with Ansible
-----------------------------------------

Ansible role for installing Zabbix 3 server.
This role installs Zabbix 3 Server on systems running RHEL 7 or Centos 7.

Limitations: Only MySQL/Mariadb is supported. Support for PostgreSQL is planned in the next versions.

Copyright:
This role is derived from https://github.com/dj-wasabi/ansible-zabbix-server role http://werner-dijkerman.nl/

Features:
---------
- Support for Zabbix 3 Server for RHEL/CENTOS 7
- Support for MySQL/MariaDB database
- Ensuring SELinux context is kept when copying Zabbix and Apache conf files
- Add dynamic entry in /etc/hosts with zabbix_url variable (zabbix server name)

Info:
----
Some variables such as first_playbook_run can be set to True or False. When it's True
the task for adding an entry in /etc/hosts is run, and for configuring root password
for MySQL.
Additional variables such as zabbix_database_creation and zabbix_database_sqlload should
be set to True only during the first playbook run.

Requirements:
-------------
geerlingguy.apache role for Apache Httpd

Version:
--------
0.1

Author Information
------------------
Davide M. Puggioni

License
-------
GPLv3
