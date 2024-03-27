mariadb_docker
=========

Deploy MariaDB as a Docker container.

Requirements
------------

- docker engine with compose v2

Role Variables
--------------

```yaml
mariadb_version: MariaDB image version to be pulled from Docker Hub and deployed
mariadb_project_name: a string; goes into container name, container hostname and Docker volume name
mariadb_project_path: where to keep the Docker Compose YAML
mariadb_project_owner: host user that should own the project directory
mariadb_project_group: host group that should own the project directory
mariadb_root_pw_path: a secret; path to a YAML file containing MariaDB 'root' password 
mariadb_databases_path: a secret; path to a YAML file defining databases to be deployed on the MariaDB server
mariadb_users_path: a secret; path to a YAML file defining users to be configured on the MariaDB server
```

Note: check out the mock (unencrypted) "secrets" under `molecule/default/secrets` for reference on the expected format. 

Example Playbook
----------------

See `molecule/default/converge.yaml`.

License
-------

BSD

Author Information
------------------

corvus-migratorius@proton.me
