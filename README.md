# Ansible Role: Nginx

Installs Nginx for RedHat/CentOS linux servers.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values:

    # The defaults provided by this role are specific to distribution.
    nginx_user: nginx
    nginx_worker_processes: 1
    nginx_error_log: error_log_path
    nginx_access_log: access_log_path
    nginx_pid: /var/run/nginx.pid
    nginx_worker_connections: 1024
    nginx_client_max_body_size: 8m


Set the above variable according to you


## Dependencies

None.

## Example Playbook (using default package)

    - hosts: localhost 
      roles:
        - nginx

## Example Playbook (install nginx)

For RHEL / CentOS:

    - hosts: localhost
      roles:
        - role: nginx
          when: "ansible_os_family == 'RedHat'"
          nginx_user: nginx
          nginx_worker_processes: 1
          nginx_error_log: /var/log/nginx/error.log
          nginx_access_log: /var/log/nginx/access.log
          nginx_pid: /var/run/nginx.pid
          nginx_worker_connections: 1024
          nginx_client_max_body_size: 8m

## To pass host ip or hostname from command line at run time use below coommand

ansible-playbook -i <hostname/ip>, site.yml -e "host=<hostname/ip>"

## License

MIT / BSD

## Author Information

www.opstree.com

blog.opstree.com
