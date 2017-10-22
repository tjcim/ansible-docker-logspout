Role Name
=========

Runs a logspout container within docker

Requirements
------------

A papertrail account is required: https://papertrailapp.com/

Role Variables
--------------

papertrail_server and papertrail_port are required. These are provided from papertrail and are in the format:

    papertrail_server: logsX
    papertrail_port: XXXX

Dependencies
------------

I have not tested it without these two additional roles. The order should as listed below with `tjcim.ansible-docker-logspout` coming last.

* tjcim.ansible-vagrant-box
* tjcim.ansible-docker

Example Playbook
----------------

    ---
    - hosts: logspout
      roles:
        - {role: 'tjcim.ansible-docker-logspout', tags: 'logspout'}

License
-------

BSD

Author Information
------------------

Not provided
