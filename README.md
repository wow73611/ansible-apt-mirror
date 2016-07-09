About
=====

Deploy apt-mirror and nginx service with [Ansible](https://www.ansible.com/).


Requirements
=====

- OS: Ubuntu 14.04 (trusty)
- [Ansible >= 2.0](https://github.com/ansible/ansible)


Usage
=====

Deploy docker with hosts file (Make sure hosts file is you need)
```
ansible-playbook -i hosts playbook.yml
```

Run as other users or use sudo
```
ansible-playbook -i hosts playbook.yml \
-e "ansible_ssh_pass=secret ansible_sudo_pass=secret sudo=yes"
```

Open your browser and go to:
```
http://<HOST-IP>/ubuntu/
```

Ansible Variables
=====

* apt_mirror_base_path: Base path of apt-mirror
* nginx_root_directory: Root directory of web service
