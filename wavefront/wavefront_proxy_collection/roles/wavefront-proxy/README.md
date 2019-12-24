Wavefront Ansible Role
=========

Ansible Role to deploy the Wavefront Proxy agent.


Platforms
---------

* Amazon Linux
* CentOS
* RedHat
* Ubuntu

Role Variables
--------------
The following variables are available for override.
```
wavefront_api_token: :         # Required. Your API Key
```

Install
----------------
Using ansible galaxy, best for ad-hoc command situations:

    $ ansible-galaxy install wavefront.wavefront-ansible

To install into your playbook roles, use `-p ROLES_PATH` or `--path=ROLES_PATH`

    $ ansible-galaxy install wavefront.wavefront-ansible -p /your/project/root/roles

Check out: [Advanced Control over Role Requirements Files](http://docs.ansible.com/galaxy.html#advanced-control-over-role-requirements-files)


Examples
----------------
1) Install Wavefront Proxy agent. This is the most basic configuration
```
- hosts: all
  roles:
    - { role: wavefront.wavefront-ansible, wavefront_api_token: XXXXXXXXXXXXX}
```

Dependencies
------------

None

License
-------

Apache 2.0

Author Information
------------------
Use github issues for bugs in this repo.
