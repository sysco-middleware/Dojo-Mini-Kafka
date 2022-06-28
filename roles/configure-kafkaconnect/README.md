Role Name
=========

configure-kafkaconnect
Configure stadalone kafka connect service (tests a simple Source & Sink)

Requirements
------------

Roles <br />
-install-JDK-role<br />
-kafka-install<br />
-configure-zookeeper<br />
-configure-kafka<br />


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

Dependencies
------------
Roles <br />
-install-JDK-role<br />
-kafka-install<br />
-configure-zookeeper<br />
-configure-kafka<br />


Example Playbook
----------------

Example:

    - hosts: servers
      roles:
         - configure-kafkaconnect

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
