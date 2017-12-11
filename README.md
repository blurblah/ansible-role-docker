# ansible-role-docker
This role supports only for Ubuntu 14.04 and 16.04 and tested on Ansible version 2.4.2

## Playbook sample #1
This playbook installs docker-ce latest version.
```yaml
- hosts: myhost
  become: yes
  roles:
    - docker
```

## Playbook sample #2
This playbook searches all 17.06 versions using apt-cache, choose latest one and install it.
```yaml
- hosts: myhost
  become: yes
  roles:
    - role: docker
      docker_version: 17.06
```