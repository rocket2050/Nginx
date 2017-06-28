centos7-nginx
=========

A brief description of the role goes here.

Requirements
------------

none

Role Variables
--------------

nginx_user: nginx
nginx_worker_processes: 1
nginx_error_log: /var/log/nginx/error.log
nginx_access_log: /var/log/nginx/access.log
nginx_pid: /var/run/nginx.pid
nginx_worker_connections: 1024
nginx_client_max_body_size: 8m


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------
www.opstree.com

blog.opstree.com

# Nginx
