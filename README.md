vector-role
=========

Role for installation Vector on RHEL

Role Variables
--------------

| var | description |
| - | - |
| vector_version | Vector Version. Default: `0.27.0` |
| log_path | Logs that will be transferred to the Vector. Default: `/var/log/*.log` | 
| clickhouse_user | ClickHouse user for Vector. Default: `vector` |
| clickhouse_password | ClickHouse password for Vector. Default: `vector` |
| clickhouse_address | ClickHouse server address. Default: `http://localhost:8123` |

Dependencies
------------

[ansible-clickhouse](https://github.com/AlexeySetevoi/ansible-clickhouse.git)

Example Playbook
----------------

Example of using a role:

  ```yaml
  - hosts: servers
    roles:
       - { role: vector-role }
  ```

License
-------

MIT

Author Information
------------------

Ivan Manokhin
