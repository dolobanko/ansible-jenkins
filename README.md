# Readme

## Description

*ansible-jenkins* is an [Ansible](http://ansible.cc) role.
Use this role to install Jenkins and install/update plugins.

### Create a host file

```bash
$ vi ansible.host
```

with

```ini
[jenkins]
your-server-ip
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
### To confirm installation, go to you-server-ip:8080 and put secret key:

```bash
$ cat /var/lib/jenkins/secrets/initialAdminPassword
```
