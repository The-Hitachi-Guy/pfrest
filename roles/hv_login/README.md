Role Name
=========

Collects a sessionId and Token from array, in order to perform operations against array. 

Requirements
------------

An Hitachi Array with an PFrest interface.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

storage.json file

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - name: Login and Logout of Storage Array
      hosts: localhost
      vars_files:
        - storage.json
      vars:
        - myauthstring: "{{storage_username}}:{{storage_password}}"
      tasks:
        - name: Login to Storage Array
          import_role:
            name: hv_login
        - name: Logout of Storage Array
          import_role:
            name: hv_logout


License
-------

BSD


