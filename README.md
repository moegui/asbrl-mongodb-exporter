ASBRL-MONGODB-EXPORTER
=========

Deploy a MongoDB-Exporter as a Docker container.

Requirements
------------

- Need to be Docker engine installed.
- A MongoDB running to get Metrics from there.

Role Variables
--------------

- default_user: 'ubuntu'
- BUILD: 'v0.11.1'
- MONGO_URI: 'mongodb://localhost:27017'
- MONGO_USERNAME: ''
- MONGO_PASSWORD: ''

Dependencies
------------

None

Example Playbook
----------------


    - name: Deploy MongoDB Exporter
      include_role:
        name: asbrl-mongodb-exporter
      vars:
        MONGO_URI: "{{ MONGO_EXPORTER_URI }}"
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
