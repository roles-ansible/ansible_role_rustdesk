[![Ansible Galaxy](https://ansible.l3d.space/svg/l3d.rustdesk.svg)](https://galaxy.ansible.com/ui/standalone/roles/l3d/rustdesk/)
[![MIT](https://ansible.l3d.space/svg/l3d.rustdesk_license.svg)](LICENSE)
[![Maintainance](https://ansible.l3d.space/svg/l3d.rustdesk_maintainance.svg)](https://ansible.l3d.space/#l3d.rustdesk)

 ansible_role_template
=======================
Ansible role to install a selfhosted rustdesk-server.

DOCS: https://rustdesk.com/docs/en/self-host/
Core Ports:
TCP 21115-21117
UDP 21116

## Variables:

```yml
---
rustdesk__version: 'latest'

rustdesk__user: 'rustdesk'
rustdesk__group: "{{ rustdesk__user }}"
rustdesk__home: '/var/lib/rustdesk'
rustdesk__user_home: "{{ rustdesk__home }}"
rustdesk__ignore_version_mismatch: false
rustdesk__require_key: true
rustdesk__relay_server_domain: "{{ ansible_fqdn }}"
rustdesk__relay_server_port: '21117'
rustdesk__signal_server_port: '21116'

rustdesk__hbbr_executable_path: '/usr/local/bin/hbbr'
rustdesk__hbbs_executable_path: '/usr/local/bin/hbbs'
rustdesk__rustdesk_utils_executable_path: '/usr/local/bin/rustdesk-utils'

# should we do a version check? (recomended)
submodules_versioncheck: false
```

# TODOs
+ Create more fancy DOCs
+ Create logos on ansible.l3d.space
