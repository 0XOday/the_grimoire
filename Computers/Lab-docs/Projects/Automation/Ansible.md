```
---
- name: Configure bridge interfaces for bare metal hosts
  hosts: bare-metal-compute
  become: yes
  tasks:
    - name: Configure DNS for mgmt iface
      community.general.nmcli:
        conn_name: '{{ mgmt_iface }}'
        type: ethernet
        dns4:
          - 192.168.97.150
        state: present
    - name: Initial updates
      dnf:
        name: '*'
        state: latest
    - name: Install dependencies
      dnf:
        name:
          - git
          - python3-devel
          - libffi-devel
          - gcc
          - openssl-devel
          - python3-libselinux
          - iscsi-initiator-utils
    - name: Start iscsid
      ansible.builtin.systemd_service:
        state: started
        enabled: true
        name: iscsid
    - name: Disable SELinux
      ansible.posix.selinux:
        state: disabled
    - name: Configure passwd-less sudo
      lineinfile:
        path: /etc/sudoers
        state: present
        regexp: '^wheel'
        line: '%wheel ALL=(ALL) NOPASSWD: ALL'
        validate: 'visudo -cf %s'
    - name: Configure root bridge SAN v300
      community.general.nmcli:
        type: bridge
        conn_name: br-v300
        method4: manual
        ip4: '{{ san_ip }}/24'
        method6: disabled
        state: present
    - name: Attach SAN iface to bridge
      community.general.nmcli:
        type: ethernet
        conn_name: '{{ san_iface }}'
        slave_type: bridge
        master: br-v300
        state: present
    - name: Create VLAN403
      community.general.nmcli:
        type: vlan
        conn_name: vlan403
        vlandev: '{{ root_interface }}'
        vlanid: 403
        state: present
    - name: Create VLAN402
      community.general.nmcli:
        type: vlan
        conn_name: vlan402
        vlandev: '{{ root_interface }}'
        vlanid: 402
        state: present
```