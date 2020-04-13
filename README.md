# Apache on Ubuntu 18.04

This playbook will install the Apache 2 web server on an Ubuntu 18.04 machine, as explained in the guide on [How to Use Ansible to Install and Configure Apache on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-use-ansible-to-install-and-set-up-apache-on-ubuntu-18-04).

## Settings

- `app_user`: a remote non-root user on the Ansible host that will own the application files.
- `http_host`: your domain name.
- `http_conf`: the name of the configuration file that will be created within Apache.
- `http_port`: HTTP port, default is 80.
- `disable_default`: whether or not to disable the default Apache website. When set to true, your new virtualhost should be used as default website. Default is true.


## Running this Playbook

Quick Steps:

### 1. Customize Options

```yml
#playbook.yml
---
app_user: "app_user"
http_host: "domain"
http_conf: "domain.conf"
http_port: "80"
disable_default: true
```

### 2. Run the Playbook

```command
ansible-playbook -l [target] -i [inventory file] -u [remote user] playbook.yml
```
