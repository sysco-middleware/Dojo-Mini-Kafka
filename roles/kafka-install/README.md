Role Name
=========

kafka-install
This role helps in installing kafka binaries and configure.

Requirements
------------

Kafka binary archive need to be downloaded and placed in files directory under this role.

Role Variables
--------------

Use the variable.yml to define the variables


>{{ KAFKA_ARCHIVE }} -- defines the name of the downloaded archive
>
>{{ HOME }}          -- Location for kafka archive
>
>{{ BASE }}          -- Location for kafka binary installation
>
>{{ KAFKA_USER }}    -- User owning the kafka installation
>
>{{ KAFKA_GROUP }}   -- Group owning the kafka installation


Dependencies
------------

No Dependencies

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - kafka-install

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).