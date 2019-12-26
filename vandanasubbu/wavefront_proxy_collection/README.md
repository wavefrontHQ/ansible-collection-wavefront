# Ansible Collection - vandanasubbu.wavefront_proxy_collection

This Ansible collection comprises of roles that allows you to install and configure wavefront-proxy from your playbook.

To install the collection:

```
ansible-galaxy collection install vandanasubbu.wavefront_proxy_collection
```

To install the collection from the tarball:

```
ansible-galaxy collection install vandanasubbu-wavefront_proxy_collection-1.0.4.tar.gz
```

To use the collection in your playbook after installation

```
- hosts: localhost
  become: true
  collections:
   - vandanasubbu.wavefront_proxy_collection
  tasks:
    - import_role:
        name: wavefront-proxy
      vars:
        wavefront_api_token: 'YOUR_WAVEFRONT_API_TOKEN'
        wavefront_api_url: 'YOUR_WAVEFRONT_URL'
```