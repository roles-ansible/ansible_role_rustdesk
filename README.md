[![Ansible Galaxy](https://ansible.l3d.space/svg/roles-ansible.rustdesk.svg)](https://galaxy.ansible.com/ui/standalone/roles/roles-ansible/rustdesk/)
[![MIT](https://ansible.l3d.space/svg/roles-ansible.rustdesk_license.svg)](LICENSE)
[![Maintainance](https://ansible.l3d.space/svg/roles-ansible.rustdesk_maintainance.svg)](https://ansible.l3d.space/#roles-ansible.rustdesk)

 ansible role rustdesk
=======================
Ansible role to install a selfhosted rustdesk-server.

You can find more information about hosting rustdesk for yourself at [rustdesk.com/docs](https://rustdesk.com/docs/en/self-host/).

 Rustdesk Requirements
=======================
To kommunikate with rustdesk, you need to open these Ports on the rustdesk server:
+ TCP Ports: ``21115-21117``
+ UDP Ports: ``21116``

*Some of the Ports can be changed in the config*

## Ansible Role Variables

| Variable | Value | Description |
| --- | --- | --- |
| ``rustdesk__version`` | ``latest`` | Specify the wanted rustdesk release or install latest |
| ``rustdesk__user`` | ``rustdesk`` | Unix User Name |
| ``rustdesk__group`` | ``{{ rustdesk__user }}`` | Unix Group Name |
| ``rustdesk__home`` | ``/var/lib/rustdesk`` | Application Working Enviroment |
| ``rustdesk__user_home`` | ``{{ rustdesk__home }}`` | Unix Home |
| ``rustdesk__ignore_version_mismatch`` | ``false`` | Ignore the fact that hbbs and hbbr versions mismatch. *(not recomended)* |
| ``rustdesk__require_key`` | ``true`` | prohibit users without the key from establishing non-encrypted connections |
| ``rustdesk__relay_server_domain`` | ``{{ ansible_fqdn }}`` | What is the Domain/IP from your rustdesk relay server? |
| ``rustdesk__relay_server_port`` | ``21117`` | Rustdesk Relay Port |
| ``rustdesk__signal_server_port`` | ``21116`` | Rustdesk Signal Server Port |
| ``rustdesk__hbbr_executable_path`` | ``/usr/local/bin/hbbr`` | Rustdesk relay server executable |
| ``rustdesk__hbbs_executable_path`` | ``/usr/local/bin/hbbs`` | Rustdesk signal server executable |
| ``rustdesk__rustdesk_utils_executable_path`` | ``/usr/local/bin/rustdesk-utils`` | Rustdesk utils path executable |
| ``submodules_versioncheck`` | ``false`` | Run simple Versionscheck *(recomended)* |

 License
=========
+ This Ansible role is under [MIT License](LICENSE).
+ Please feel free to open a issue or pull-request.
