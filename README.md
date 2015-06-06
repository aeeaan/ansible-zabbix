Role Name
=========

A role for installing zabbix server or zabbix agent. Please note that at this time, the proxy install is just a placeholder. Also, this won't work if zabbix_frontend_install is true without zabbix_server_install also being true. Separate installs are not supported at this time. Only agent is installed by default.

Role Variables
--------------
| Variable			| Default						| Notes				|
| :---				| :---							| :---				|
| zabbix_server_install		| false							| 				|
| zabbix_frontend_install	| false							|				|
| zabbix_proxy_install		| false							|				|
| zabbix_agent_install		| true							|				|
| zabbix_server_ips		| 127.0.0.1						|				|
| zabbix_server_db_hostname	| "localhost"						|				|
| zabbix_server_db_port		| "3306"						|				|
| zabbix_server_db_name		| "zabbix"						|				|
| zabbix_server_db_user		| "zabbix"						|				|
| zabbix_server_db_pass		| "testzabbix"						|				|
| zabbix_server_db_schema_dir	| "/usr/share/doc/zabbix-server-mysql-2.4.3/create/"	|				|
| zabbix_frontend_require_ssl	| true

Dependencies
------------

- correcthorse.common
- correcthorse.httpd
- correcthorse.php
- correcthorse.mysql

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: correcthorse.zabbix }

License
-------

MIT

Author Information
------------------

* [Joshua Rusch](https://correct.horse/)