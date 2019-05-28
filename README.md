Role Name
=========

Role for restoring the database data

Requirements
------------

Role Variables
--------------

userdba: The owner of the application database
db: The name of the database
target_file: The sql file to upload to the server
appdir: The location to upload the file, must be accessible to the userdba

Dependencies
------------

Example Playbook
----------------

    - hosts: servers
      roles:
        - {
            role: oscbco.restore_database,
            userdba: "{{ global_userdba }}",
            db: "{{ global_db }}",
            target_file: oscbco.sql,
            appdir: "{{ global_appdir }}"
          }

License
-------

MIT

Author Information
------------------

oscbco.me
