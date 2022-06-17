Role Name
=========

configure-zookeeper  --  This role is meant to configure the zookeeper service on the standalone kafka basic installation

Requirements
------------

zookeeper-service.j2 template to be used to configure the zookeeper as systemd service in linux

Role Variables
--------------

>{{ KAFKA_ARCHIVE }} -- defines the name of the downloaded archive
>
>{{ HOME }} -- Location for kafka archive
>
>{{ BASE }} -- Location for kafka binary installation
>
>{{ KAFKA_USER }} -- User owning the kafka installation
>
>{{ KAFKA_GROUP }} -- Group owning the kafka installation
>
>{{ DATA_DIR }}   -- Data directory location

Dependencies
------------

Roles needed are<br />
install-JDK-role<br />
kafka-install<br />

Example Playbook
----------------

Example

    - hosts: servers
      roles:
         - configure-zookeeper

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
