# Ansible Collection - ericsysmin.wavefront

This Ansible collection comprises of roles that allows you to install and configure wavefront-proxy from your playbook.

Pre-requisites:

```
ansible >= 2.9 is required.
```

To install the collection:

```
ansible-galaxy collection install ericsysmin.wavefront
```

To use the collection in your playbook and import wavefront-proxy after installation

```yaml
- hosts: localhost
  become: true
  tasks:
    - import_role:
        name: ericsysmin.wavefront.wavefront_proxy
      vars:
        wavefront_api_token: "YOUR_WAVEFRONT_API_TOKEN"
        wavefront_api_url: "YOUR_WAVEFRONT_URL"
```

To use the collection in your playbook and import telegraf after installation

```yaml
- hosts: localhost
  become: true
  tasks:
    - import_role:
        name: ericsysmin.wavefront.telegraf
      vars:
        proxy_address: "YOUR_WAVEFRONT_PROXY_ADDRESS"
```
