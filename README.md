Role Name
=========

`ssh-keygen-local-to-remotes`

Requirements
------------

`ansible-core`

Role Variables
--------------
`default.yml`
```yaml
ssh_keygen_options:
  key_size: 2048
  key_type: rsa
  passphrase: ''
```
Dependencies
------------


Example Playbook
----------------
- example.playbook
```yaml
  - name: Use Example
    hosts: ssh-key
    gather_facts: true
    roles:
      - ssh-keygen-local-to-remotes
```
- example.inventory
```yaml 
[ssh-key]
controller-1 ansible_host=192.168.24.11 
controller-2 ansible_host=192.168.24.12 
controller-3 ansible_host=192.168.24.13
db ansible_host=192.168.123.155
```
- example.using command
```bash
ansible-playbook -i $inventory_file -k $playbook.yml
```
License
-------

BSD

Author Information
------------------
`jaeyoung645@naver.com`
