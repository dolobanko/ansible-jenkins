# Readme

## Description

*ansible-jenkins* is an [Ansible](http://ansible.cc) role.
Use this role to install Jenkins and install/update plugins.

### Create a host file

Following example make ansible aware of the Vagrant box reachable on localhost port 2222.

```bash
$ vi ansible.host
```

with

```ini
[jenkins]
127.0.0.1 
```

```

### Run the playbook


First create a playbook including the jenkins role, naming it jenkins.yml.

```yml
- name: Jenkins
  hosts: jenkins
  roles:
    - ansible-jenkins
```


```bash
$ ansible-playbook -i ansible.host jenkins.yml
```
