# Ansible Collection - vandanasubbu.wavefront_proxy_collection

This Ansible collection comprises of roles that allows you to install and configure wavefront-proxy from your playbook.

To install the collection adjacent to your playbook:

```
ansible-galaxy collection install vandanasubbu.wavefront_proxy_collection
```

To use the collection in your playbook after installation

```
- hosts: localhost
  collections:
   - vandanasubbu.wavefront_proxy_collection
  tasks:
    - import_role:
        name: wavefront-proxy
      vars:
        wavefront_api_token: 'YOUR_WAVEFRONT_API_TOKEN'
        wavefront_api_url: 'YOUR_WAVEFRONT_URL'
```