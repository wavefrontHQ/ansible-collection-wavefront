# Ansible Collection - wavefrontHQ.ansible-collection-wavefront

This Ansible collection comprises of roles that allows you to install and configure wavefront-proxy from your playbook.

Pre-requisites:
```
ansible version 2.9.* is required.
```

To install the collection:

```
ansible-galaxy collection install wavefront.ansible_collection_wavefront
```

To install the collection from the tarball:

```
ansible-galaxy collection install wavefront-ansible_collection_wavefront-1.3.0.tar.gz
```

To use the collection in your playbook and import wavefront-proxy after installation

```
- hosts: localhost
  become: true
  tasks:
    - import_role:
        name: wavefront.wavefront.wavefront_proxy
      vars:
        wavefront_api_token: 'YOUR_WAVEFRONT_API_TOKEN'
        wavefront_api_url: 'YOUR_WAVEFRONT_URL'
```

To use the collection in your playbook and import telegraf after installation

```
- hosts: localhost
  become: true
  tasks:
    - import_role:
        name: wavefront.wavefront.telegraf
      vars:
        telegraf_wavefront_proxy_address: 'YOUR_WAVEFRONT_PROXY_ADDRESS'
```
