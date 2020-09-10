ASBRL-MONGODB-EXPORTER
=========

Deploy a MongoDB-Exporter (percona) as a Docker container.

Requirements
------------

- Need to be Docker engine installed.
- A MongoDB running to get Metrics from there.

Role Variables
--------------

- default_user: 'ubuntu'
- BUILD: 'v0.11.1'
- MONGO_HOST: 'localhost'
- MONGO_PORT: 27017
- MONGO_USERNAME: ''
- MONGO_PASSWORD: ''

Dependencies
------------

https://github.com/percona/mongodb_exporter

Example Playbook
----------------


    - name: Deploy MongoDB Exporter
      include_role:
        name: asbrl-mongodb-exporter
      vars:
        MONGO_HOST: "{{ MONGO_HOST }}"
        MONGO_USERNAME: "{{ MONGO_ROOT_USERNAME }}"
        MONGO_PASSWORD: "{{ MONGO_ROOT_PASSWORD }}"
      tags:
        - mongo-exporter

License
-------

BSD

Author Information
------------------

Moegui.com
