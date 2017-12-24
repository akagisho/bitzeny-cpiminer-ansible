# bitzeny-cpiminer-ansible

## Requirements

* CentOS 7.x

## Usage

Create Ansible inventory file.

```
$ ${EDITOR} inventories/production/hosts
[default]
mining.example.com ansible_user=root

[default:vars]
minerd_stratum_host=example.local
minerd_stratum_port=19333
minerd_stratum_user=user
minerd_stratum_pass=password
```

Run ansible playbook.

```
$ ansible-playbook -i inventories/production/hosts site.yml
```