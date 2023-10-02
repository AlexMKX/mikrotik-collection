# Role mikrotik.upgrade 

used to upgrade mikrotik devices

## usage

```yaml
- name: Upgrade Mikrotik
  hosts: mikrotik
  gather_facts: no
  connection: network_cli
  serial: 1
  collections:
    - alexmkx.mikrotik
  tasks:
    - name: Upgrade Mikrotik
      include_role:
        name: upgrade
      vars:
        hostname: "{{ inventory_hostname }}"
        username: "{{ ansible_user }}"
        password: "{{ ansible_password }}"
```